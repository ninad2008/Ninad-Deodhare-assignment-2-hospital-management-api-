# Hospital Management REST API

A Node.js and Express RESTful API with MongoDB database integration and Passport.js authentication for managing hospitals and user accounts.

## 📌 Project Features

- **User Authentication**: Secure user registration and login endpoints using `passport` and `passport-local`.
- **Hospital Management (CRUD)**: Create, Read, Update, and Delete operations for hospital records.
- **Available Beds Filter**: Dedicated endpoint to query hospitals with available beds (`availableBeds > 0`).
- **MongoDB Connection**: Database connection managed via Mongoose.

---

## 🛠️ Tech Stack

- **Backend**: Node.js, Express.js
- **Database**: MongoDB, Mongoose
- **Authentication**: Passport.js (`passport-local` strategy)

---

## 🗄️ Database Entities

### 1. User Entity
- `username`: String (required, unique)
- `email`: String (required, unique)
- `password`: String (required)

### 2. Hospital Entity
- `name`: String (required)
- `city`: String (required)
- `totalBeds`: Number (required)
- `availableBeds`: Number (required)

---

## 🚀 API Endpoints

### 🔐 Authentication Routes
| Method | Endpoint | Description | Access |
| :--- | :--- | :--- | :--- |
| `POST` | `/register` | Register a new user | Public |
| `POST` | `/login` | Authenticate user credentials | Public |
| `GET` | `/` | User welcome profile | Authenticated |

### 🏥 Hospital Routes
| Method | Endpoint | Description | Access |
| :--- | :--- | :--- | :--- |
| `GET` | `/hospitals` | Get list of all hospitals | Authenticated |
| `GET` | `/hospitals/available` | Get hospitals with available beds (`> 0`) | Authenticated |
| `POST` | `/hospitals` | Add a new hospital | Authenticated |
| `GET` | `/hospitals/:id` | Get details of a single hospital by ID | Authenticated |
| `PUT` | `/hospitals/:id` | Update hospital details by ID | Authenticated |
| `DELETE` | `/hospitals/:id` | Delete a hospital by ID | Authenticated |

---

## 💻 How to Run Locally

1. **Clone the repository**:
   ```bash
   git clone https://github.com/ninad2008/Ninad-Deodhare-assignment-2-hospital-management-api-.git
   cd Ninad-Deodhare-assignment-2-hospital-management-api-/backend
   ```

2. **Install dependencies**:
   ```bash
   npm install
   ```

3. **Start MongoDB**:
   Ensure local MongoDB server is running on `mongodb://localhost:27017/hospitalDB` (or launch via MongoDB Compass).

4. **Start the server**:
   ```bash
   node server.js
   ```

5. Server will start at `http://localhost:4000`.

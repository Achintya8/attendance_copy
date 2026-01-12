# How to Run the Attendance App in VS Code

## Prerequisites
Ensure you have the following installed on your system:
- **Java Development Kit (JDK) 17** or higher.
- **Maven** (for building the backend).
- **Node.js** (v18 or higher) and **npm**.
- **Visual Studio Code** with the **Extension Pack for Java** installed.

## Project Structure
- `backend/`: Spring Boot application.
- `frontend/`: React application (Vite).

## Setup Instructions

### 1. Backend Setup
1. Open the `backend` folder in VS Code or a terminal.
2. Install dependencies and build the project:
   ```bash
   mvn clean install
   ```
   *Note: If tests fail, you can skip them with `mvn clean install -DskipTests`.*

### 2. Frontend Setup
1. Open the `frontend` folder in a terminal.
2. Install dependencies:
   ```bash
   npm install
   ```

## Running the Application

### Option A: Using VS Code Extensions (Recommended)
1. **Backend**:
   - Open the `backend/src/main/java/com/college/attendance/AttendanceApplication.java` file.
   - Click "Run" or "Debug" appearing above the `main` method, or press `F5`.
   - Alternatively, use the **Java Projects** view in the sidebar to run the application.
2. **Frontend**:
   - Open a terminal in VS Code (`Ctrl + ~`).
   - Navigate to the frontend directory: `cd frontend`.
   - Run the development server:
     ```bash
     npm run dev
     ```

### Option B: Using Terminal
1. **Start Backend**:
   ```bash
   cd backend
   mvn spring-boot:run
   ```
2. **Start Frontend** (in a new terminal tab):
   ```bash
   cd frontend
   npm run dev
   ```

## Accessing the App
- **Frontend**: [http://localhost:5173](http://localhost:5173)
- **Backend API**: [http://localhost:8080](http://localhost:8080)

## Troubleshooting
- **Port Conflicts**: Ensure ports 8080 (backend) and 5173 (frontend) are free.
- **Database**: The app uses an H2 in-memory database by default. Data is reset on restart unless configured otherwise.
- **Login Issues**: If you cannot log in, check the backend logs for seeded user credentials (usually printed at startup).

# BlogForge - AI Powered Debt Relief & Financial Recovery Platform

This is the master directory for the **BlogForge** platform. This README serves as a guide on where the code exists, how to set it up, how to run it locally, and how to execute the test suite.

---

## 📂 Codebase Location

The complete, active source code for the platform is located inside the [5. Project Development Phase](file:///c:/Users/madda/OneDrive/Desktop/My-Projects/smartbridge/5.%20Project%20Development%20Phase/) directory. It is split into two components:

1.  **Backend (API Server)**: [5. Project Development Phase/backend](file:///c:/Users/madda/OneDrive/Desktop/My-Projects/smartbridge/5.%20Project%20Development%20Phase/backend/)
    *   Built with FastAPI, SQLite, SQLAlchemy ORM, Pydantic, and Google Gemini API.
2.  **Frontend (UI Client)**: [5. Project Development Phase/frontend](file:///c:/Users/madda/OneDrive/Desktop/My-Projects/smartbridge/5.%20Project%20Development%20Phase/frontend/)
    *   Built with React.js (Vite) and custom Vanilla CSS.

---

## 🛠️ Prerequisites

Ensure you have the following installed on your system:
*   [Python 3.10 or higher](https://www.python.org/downloads/)
*   [Node.js (v18 or higher) and npm](https://nodejs.org/)

---

## 🚀 Setup & Execution Guide

Follow these steps to run both the frontend and backend servers.

### 1. Run the Backend Server

1.  Open your terminal and navigate to the backend folder:
    ```powershell
    cd "5. Project Development Phase/backend"
    ```

2.  Create a virtual environment (optional but recommended):
    ```powershell
    python -m venv venv
    ```

3.  Activate the virtual environment:
    *   **Windows (PowerShell)**:
        ```powershell
        .\venv\Scripts\Activate.ps1
        ```
    *   **Windows (CMD)**:
        ```cmd
        .\venv\Scripts\activate.bat
        ```
    *   **macOS / Linux**:
        ```bash
        source venv/bin/activate
        ```

4.  Install the required Python dependencies:
    ```powershell
    pip install -r requirements.txt
    ```

5.  Configure your environment variables by creating a `.env` file (an example template `.env.example` is provided):
    ```env
    GEMINI_API_KEY=your_actual_gemini_api_key_here
    ```
    *(Note: If the key is not provided, the server will automatically fall back to a high-fidelity local mockup generator for hardship letter creation to prevent crashes).*

6.  Start the FastAPI development server:
    ```powershell
    python run.py
    ```
    The backend API will start running on **[http://127.0.0.1:8000](http://127.0.0.1:8000)**.

---

### 2. Run the Frontend Server

1.  Open a new terminal window and navigate to the frontend folder:
    ```powershell
    cd "5. Project Development Phase/frontend"
    ```

2.  Install the Node.js packages:
    ```powershell
    npm install
    ```

3.  Start the Vite frontend development server:
    ```powershell
    npm run dev
    ```
    The frontend UI will start running on **[http://localhost:5173/](http://localhost:5173/)**.

---

## 🧪 Testing Guide

This section explains how to run verification tests for both components of the platform.

### 1. Backend Automated Unit Tests (Pytest)

The backend includes a suite of unit tests verifying the mathematical boundaries and logic of the financial calculation engine.

1.  Navigate to the backend directory and ensure your virtual environment is active:
    ```powershell
    cd "5. Project Development Phase/backend"
    ```
2.  Run the tests using `pytest`:
    ```powershell
    python -m pytest tests
    ```
    This runs verification assertions on the stress meter DTI/EMI calculators, surplus income analysis, and target settlement predictions.

---

### 2. Frontend Build Verification & Linting

Verify that there are no compilation errors or formatting alerts in the React app:

1.  Navigate to the frontend directory:
    ```powershell
    cd "5. Project Development Phase/frontend"
    ```
2.  Run the production bundler to check for compiler sanity:
    ```powershell
    npm run build
    ```
3.  Run the code linter (using Oxlint) to inspect source cleanliness:
    ```powershell
    npm run lint
    ```

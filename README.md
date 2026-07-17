# SafeShare - Zero-Knowledge Secure File Sharing

SafeShare is a high-security, Zero-Knowledge file-sharing application designed to protect user data. Files are fully encrypted directly in the user's browser before upload, ensuring that sensitive information remains entirely private.

## 🚀 Core Features

* **Zero-Knowledge Encryption:** Files are encrypted client-side using Web Crypto parameters. The secret decryption key is appended as a URL hash fragment (`#`) and is never transmitted to or stored on the server.
* **Serverless Cloud Architecture:** Powered by a robust FastAPI backend connected directly to MongoDB Atlas utilizing BSON binary storage to maintain absolute cryptographic payload integrity.
* **Cross-Origin Accessibility:** Configured with production CORS alignments to seamlessly support client interactions across desktop and mobile devices.
* **Granular Access Controls:** Features built-in parameters for burn-after-reading execution and real-time administrator approval workflows.

## 🛠️ Architecture & Tech Stack

* **Frontend:** Standard Web Cryptography API, Native JavaScript DOM Interaction Engine
* **Backend:** Python, FastAPI, Uvicorn
* **Database:** MongoDB Atlas (BSON Binary Storage Model)

## 📦 Local Setup & Execution

### 1. Backend Setup
1. Install dependencies: `pip install fastapi uvicorn pymongo python-multipart`
2. Configure your MongoDB Atlas connection string inside `main.py`.
3. Launch the production server:
   ```bash
   uvicorn main:app --reload

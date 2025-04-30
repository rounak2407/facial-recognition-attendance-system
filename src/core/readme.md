
### 📁 `src/core/` Folder – Core Logic Scripts

This folder contains the core functionality for the Facial Recognition Attendance System. Each script has a dedicated purpose for managing the pipeline from image capture to attendance recognition and storage.

---

### 🔹 `face_register.py`

- **Purpose**: Captures 100 grayscale face images per user.
- **How It Works**: Uses OpenCV and Haar cascade to detect and save faces in `dataset/users/ID_Name/`.
- **Note**: Automatically creates folders and checks for duplicates. Prompts user before overwriting existing data.

---

### 🔹 `face_trainer.py`

- **Purpose**: Trains the LBPH recognizer on registered faces.
- **How It Works**: Loads images from user folders, extracts grayscale data, and saves the trained model to `models/trainer.yml`.

---

### 🔹 `face_recognition.py`

- **Purpose**: Performs real-time facial recognition via webcam.
- **How It Works**: Loads `trainer.yml` and Haar cascade, matches detected faces against trained IDs, and logs attendance with timestamp.

---

### 🔹 `convertToExcel.py`

- **Purpose**: Converts daily attendance logs into an Excel sheet.
- **How It Works**: Reads `.csv` files from the `Attendance/` folder and exports `.xlsx` versions for easier readability and record keeping.

---


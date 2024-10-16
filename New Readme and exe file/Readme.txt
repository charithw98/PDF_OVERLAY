# **PDF Overlay Project**

This project is a PDF processing application that allows users to overlay content onto PDF files, extract data from Excel sheets, and manage document encryption using various utilities. This guide will provide detailed steps on how to set up, install, and create a `.exe` file for Windows.

## **Table of Contents**
- [System Requirements](#system-requirements)
- [Installation Guide](#installation-guide)
- [Creating a `.exe` File](#creating-a-exe-file)
- [Running the Application](#running-the-application)
- [Dependencies](#dependencies)
- [Troubleshooting](#troubleshooting)

---

## **System Requirements**

To run this project and create an executable, the following system requirements must be met:

- **Operating System**: Windows 10 or higher
- **Python**: Version 3.7 or higher
- **Pip**: Python package manager installed (comes with Python)
- **Disk Space**: At least 200 MB of free disk space
- **RAM**: Minimum of 4 GB
- **Software**:
  - [Python](https://www.python.org/downloads/)
  - [Visual Studio Code](https://code.visualstudio.com/)

---

## **Installation Guide**

### **Step 1: Clone the Project**

First, download the project files by cloning the GitHub repository.

1. Open Command Prompt and navigate to the folder where you want to clone the project:
   ```bash
   cd path\to\your\desired\folder
   ```

2. Run the following Git command to clone the project repository:
   ```bash
   git clone https://github.com/yourusername/PDF_OVERLAY.git
   ```

3. Navigate to the project folder:
   ```bash
   cd PDF_OVERLAY
   ```

### **Step 2: Install Python and Pip**

1. Download and install [Python](https://www.python.org/downloads/windows/). Ensure you check the option to **Add Python to PATH** during the installation.

2. Open Command Prompt and check if Python and `pip` are installed correctly:
   ```bash
   python --version
   pip --version
   ```

### **Step 3: Install Project Dependencies**

In the project folder, run the following command to install the required libraries:
```bash
pip install -r requirements.txt
```

If there is no `requirements.txt` file, you can install each dependency manually:
```bash
pip install openpyxl
pip install msoffcrypto-tool
```

---

## **Creating a `.exe` File**

To create an executable (.exe) file for the project, follow these steps:

### **Step 1: Install PyInstaller**

1. Open Command Prompt and navigate to the project directory:
   ```bash
   cd path\to\PDF_OVERLAY
   ```

2. Install **PyInstaller** using `pip`:
   ```bash
   pip install pyinstaller
   ```

### **Step 2: Create the Executable**

1. Run the following command in the project directory to create a single `.exe` file:
   ```bash
   pyinstaller --onefile src/main.py
   ```

2. After running the command, PyInstaller will create a `dist` folder inside the project directory. This folder contains the executable `.exe` file.

### **Step 3: Run the Executable**

Navigate to the `dist` folder, and you’ll find the generated executable. You can run it by double-clicking the `.exe` file or from the command line:
```bash
.\dist\main.exe
```

---

## **Running the Application**

After creating the `.exe` file, you can run the application directly without installing Python.

If you are running the Python project directly (without an `.exe`), follow these steps:

1. Open Command Prompt and navigate to the project folder.
2. Run the main Python script:
   ```bash
   python src/main.py
   ```

---

## **Dependencies**

The project uses several Python libraries. If you're developing or running the project, ensure these dependencies are installed:

- `tkinter`: For GUI elements.
- `openpyxl`: For working with Excel files.
- `msoffcrypto`: For handling encrypted Microsoft Office files.
- `PyInstaller`: For creating executable files (used during the build process).

To install the dependencies manually:
```bash
pip install tkinter openpyxl msoffcrypto-tool
```

---

## **Troubleshooting**

1. **`pip` is not recognized**: Ensure Python and `pip` are correctly added to your system's PATH. You can verify by running `python --version` and `pip --version` in Command Prompt.

2. **Missing modules error**: If you encounter a `ModuleNotFoundError`, run:
   ```bash
   pip install <missing_module_name>
   ```

3. **Error during `.exe` creation**: Ensure all dependencies are installed. If PyInstaller fails, make sure your Python scripts are running correctly before attempting to compile them.

---

## **License**

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

Feel free to edit this README as per your project requirements. Let me know if you need any further clarifications or adjustments!

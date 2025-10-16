# Setting Up UV Python Environment

## Project Setup

### 1. Create Project Folder Structure

Navigate to your desired location and create your project folder:
```powershell
mkdir your-project-name
cd your-project-name
```

Create subfolders for organization:
```powershell
mkdir code, data, documents, deliverables
```

---

## UV Installation

### 2. Check if UV is Installed
```bash
uv --version
```

### 3. Install UV (if not installed)

For Windows:
```powershell
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

### 4. Add UV to PATH (PowerShell)

After installation, add UV to your PATH:
```powershell
$env:Path = "C:\Users\YourUsername\.local\bin;$env:Path"
```

Verify installation:
```bash
uv --version
```

---

## Environment Setup

### 5. Initialize UV Project

Set up your project with a specific Python version (e.g., Python 3.10):
```bash
uv init --python 3.10
```

### 6. Create Virtual Environment
```bash
uv venv
```

### 7. Activate Virtual Environment
```powershell
.venv\Scripts\Activate
```

You should see `(.venv)` appear in your terminal prompt.

---

## Installing Packages

### 8. Install Required Packages

Example with Polars and Jupyter:
```bash
uv pip install polars jupyter
```

### 9. Verify Installation
```bash
uv pip list
```

---

## Quick Reference

### Activating Environment (Future Sessions)
```powershell
$env:Path = "C:\Users\YourUsername\.local\bin;$env:Path"
.venv\Scripts\Activate
```

### Installing Additional Packages
```bash
uv pip install package-name
```

### Starting Jupyter Notebook
```bash
jupyter notebook
```

### Deactivating Environment
```bash
deactivate
```
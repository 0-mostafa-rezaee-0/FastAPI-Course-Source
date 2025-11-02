<h1 align="center">FastAPI Course - Project 001</h1>

### 1. To set up a virtual environment
```bash
# 1. Create a virtual environment (creates a new directory called .venv)
cd 001
virtualenv .venv

# 2. Activate the virtual environment (On Linux/macOS)
source .venv/bin/activate

# 3. Install dependencies from requirements.txt
pip install -r requirements.txt

# 4. Verify installation
pip list

# To deactivate the virtual environment when done:
deactivate
```

### 2. To install FastAPI
```bash
pip install "fastapi[standard]"
```

### 3. First FastAPI code
```
# Create a file `main.py` with:

from fastapi import FastAPI

app = FastAPI()

@app.get("/")
def read_root():
    return {"Hello": "World"}
```

### 4. To Run the Application
```bash
fastapi dev main.py
```

### 5. Access the Application

Once the server is running, you can access:
- **API**: http://localhost:8000
- **Interactive API Documentation (Swagger UI)**: http://localhost:8000/docs
- **Alternative API Documentation (ReDoc)**: http://localhost:8000/redoc

**Note for WSL2 Users**: WSL2 automatically forwards ports from Windows to the Linux environment. The server logs will show port 8000 (the port inside WSL2), but when you click on the links in the terminal output, Windows automatically opens the correct forwarded port (e.g., `http://localhost:8001`) in your browser. If you manually type the URL in your browser, use the forwarded port number instead of 8000.

## 6. Project Structure

- `main.py`: Main FastAPI application file
- `requirements.txt`: Python package dependencies
- `README.md`: Project documentation (this file)
- `.venv/`: Virtual environment directory (created after setup, should be added to `.gitignore`)

## 5. Notes

- Always activate your virtual environment before working on the project
- The `.venv` directory should not be committed to version control (it's typically excluded in `.gitignore`)
- If you add new dependencies, update `requirements.txt` using: `pip freeze > requirements.txt`


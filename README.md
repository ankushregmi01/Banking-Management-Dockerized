# Banking-Management-Dockerized
A Banking Management system with Dockerization 
# Banking Management System

This is a **Banking Management System** built using **Django**. It allows users to manage banking operations efficiently. This project supports both local development and Dockerized deployment.

---

## 🚀 Getting Started

### **1. Run Locally**

#### **Prerequisites**
- Python (>=3.8)
- pip
- Virtual Environment (recommended)

#### **Setup and Run**
```sh
# Clone the repository
git clone https://github.com/your-username/banking-management-system.git
cd banking-management-system

# Create and activate virtual environment
python -m venv env
source env/bin/activate  # On Windows use: env\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Apply migrations
python manage.py migrate

# Create superuser (optional)
python manage.py createsuperuser

# Start the server
python manage.py runserver
```
By default, the server runs at: **http://127.0.0.1:8000/**

---

### **2. Run with Docker**

#### **Prerequisites**
- Docker

#### **Steps to Run in Docker**
```sh
# Build the Docker image
docker build -t banking-system .

# Run the container
docker run -p 8000:8000 banking-system
```
Now, access the app at **http://127.0.0.1:8000/**

---

## 🛠️ Dockerfile
If you haven't added a `Dockerfile`, use the following:

```dockerfile
# Use official Python image
FROM python:3.10

# Set working directory
WORKDIR /app

# Copy project files
COPY . /app/

# Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Expose the port
EXPOSE 8000

# Run the application
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
```

---

## 🎯 Features
- User authentication
- Account management
- Transaction history
- Secure banking operations




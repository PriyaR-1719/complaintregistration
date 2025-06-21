# complaintregistration

🛠 Complaint Registration System
A web-based application for internal staff to securely log in and register system-related complaints. This project integrates Flask, MySQL/SQLite, and HTML/CSS for a full-stack development experience.

📌 Features
🔐 Staff Login System (with MySQL database)
📝 Complaint Submission Form (using SQLite database)
💡 Tracks details such as:

System ID
Department
Issue Type
Model Name & Year
Network Details (IP, MAC)
Remarks

🖼️ UI Preview
Clean and responsive HTML/CSS form
Login page with validation and authentication
Complaint submission form with detailed fields

🏗️ Technologies Used
Frontend	Backend	Database
HTML, CSS, JS	Python (Flask)	MySQL (Login) & SQLite (Complaints)

🗂️ Project Structure
graphql

complaint-registration/
│
├── static/
│   └── styles.css            # Optional separate CSS file
│
├── templates/
│   ├── login.html            # Login form
│   ├── complaint.html        # Complaint submission form
│
├── app.py                    # Flask app for complaint handling
├── login_api.py              # Flask app for login authentication
├── complaints.db             # SQLite DB (auto-created)
├── requirements.txt          # Python dependencies
└── README.md                 # Project documentation
⚙️ Installation & Setup
🔧 Requirements
Python 3.x
MySQL Server (for login system)
Flask
MySQL Connector
Flask-CORS
Flask-SQLAlchemy

🔌 Install Dependencies
bash

pip install flask flask_sqlalchemy flask_cors mysql-connector-python
🚀 Running the Application
1. Login API (MySQL)
Update your login_api.py MySQL connection:
python
db_config = {
    "host": "localhost",
    "user": "your_username",
    "password": "your_password",
    "database": "company_db"
}
Run the login service:

bash
Copy
Edit
python login_api.py
2. Complaint System (SQLite)
Run the Flask complaint system:

bash

python app.py
📬 API Endpoints
Endpoint	Method	Description
/login	POST	Validates staff login
/submit_complaint	POST	Registers a new complaint

🗃️ MySQL Table Structure (Login)


CREATE TABLE staff (
  staff_id VARCHAR(20),
  username VARCHAR(50),
  password VARCHAR(50)
);

🔒 Security Notes
Passwords should ideally be hashed before storing.
CORS is enabled only for development; restrict in production.
Always validate and sanitize inputs before database insertion.

📄 License
This project is for educational and internal use only. No commercial license is granted.

👨‍💻 Author
Priya R.
Full Stack Development Intern at BEL
BCA Graduate – 2025
Linkedin: linkedin.com/in/priya-r-52433b358
GitHub: github.com/PriyaR-1719

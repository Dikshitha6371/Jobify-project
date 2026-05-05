Jobify - Job Portal Website
A complete, production-ready job portal web application built with Django, featuring role-based access control, job management, and application tracking.

🎯 Features
For Job Seekers
✅ User registration and authentication
✅ Complete profile management
✅ Resume upload (PDF, DOC, DOCX)
✅ Browse and search jobs with filters
✅ Apply for jobs
✅ Track application status
✅ View applicant history
For Employers
✅ Company profile management
✅ Post new job listings
✅ Edit and delete job postings
✅ View applications for each job
✅ Shortlist/Reject candidates
✅ Dashboard with statistics
Admin Features
✅ Django Admin Panel
✅ Manage users, jobs, applications
✅ System statistics
✅ Approve/Block users
🛠️ Technology Stack
Backend: Django 4.2.7 (Python Web Framework)
Frontend: HTML5, CSS3, JavaScript, Bootstrap 5
Database: SQLite (default) / MySQL
Authentication: Django's built-in authentication system
File Upload: Pillow for image processing
📁 Project Structure
jobify/
├── jobify_project/           # Django project configuration
│   ├── settings.py           # Project settings
│   ├── urls.py               # URL configuration
│   ├── wsgi.py               # WSGI configuration
│   └── asgi.py               # ASGI configuration
├── jobs/                     # Main application
│   ├── models.py             # Database models
│   ├── views.py              # View functions
│   ├── forms.py              # Django forms
│   ├── urls.py               # App URL patterns
│   ├── admin.py              # Admin interface
│   ├── templates/            # HTML templates
│   │   └── jobs/
│   │       ├── base.html
│   │       ├── home.html
│   │       ├── login.html
│   │       ├── register.html
│   │       ├── job_list.html
│   │       ├── job_detail.html
│   │       ├── job_seeker_dashboard.html
│   │       ├── employer_dashboard.html
│   │       ├── post_job.html
│   │       └── more...
│   └── migrations/           # Database migrations
├── static/                   # Static files
│   ├── css/style.css
│   └── js/script.js
├── media/                    # User uploads
├── manage.py                 # Django command utility
├── requirements.txt          # Python dependencies
└── README.md                 # This file
Setup Instructions
Prerequisites
Python 3.8 or higher
pip (Python package manager)
Virtual environment tool (venv)
Step 1: Clone or Extract Project
d d:\nextgen_4.0\project\jobify
Step 2: Create Virtual Environment
On Windows:
python -m venv venv
venv\Scripts\activate
On macOS/Linux:
python3 -m venv venv
source venv/bin/activate
Step 3: Install Dependencies
pip install -r requirements.txt
Step 4: Database Setup
python manage.py makemigrations
python manage.py migrate
Step 5: Create Superuser (Admin)
python manage.py createsuperuser
Step 6: Load Sample Data (Optional)
python load_sample_data.py
Step 7: Run Development Server
python manage.py runserver
Visit http://127.0.0.1:8000/ in your browser.
📊 Usage Guide
User Registration
Visit the homepage
Click "Register" and choose your role (Job Seeker or Employer)
Fill in the registration form
Login with your credentials
Job Seeker Workflow
Complete your profile (upload resume, add skills)
Browse jobs using search and filters
View job details and apply
Track your applications in the dashboard
Employer Workflow
Complete company profile
Post new jobs with detailed requirements
Review applications in your dashboard
Shortlist or reject candidates
🔧 Configuration
Database Configuration
Edit jobify_project/settings.py to change database settings:
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',  # For MySQL
        'NAME': 'jobify_db',
        'USER': 'your_username',
        'PASSWORD': 'your_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
Email Configuration
For password reset and notifications, configure email in settings.py:
EMAIL_BACKEND = 'django.core.mail.backends.smtp.EmailBackend'
EMAIL_HOST = 'smtp.gmail.com'
EMAIL_PORT = 587
EMAIL_USE_TLS = True
EMAIL_HOST_USER = 'your_email@gmail.com'
EMAIL_HOST_PASSWORD = 'your_app_password'
📈 Deployment
Production Deployment Checklist
✅ Change DEBUG = False in settings.py
✅ Set SECRET_KEY to a secure random string
✅ Configure production database
✅ Set up static files serving
✅ Configure ALLOWED_HOSTS
✅ Set up HTTPS
✅ Use production WSGI server (Gunicorn, uWSGI)
Example with Gunicorn
pip install gunicorn
gunicorn jobify_project.wsgi:application --bind 0.0.0.0:8000
🤝 Contributing
Fork the repository
Create a feature branch
Make your changes
Test thoroughly
Submit a pull request
📄 License
This project is open source and available under the MIT License.

📞 Support
For support or questions, please create an issue in the repository or contact the development team.

Happy Job Hunting! 🎉

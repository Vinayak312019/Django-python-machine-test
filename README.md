# Django-python-machine-test
👋 Hi, I'm Vinayak Sharma
I'm an IT engineering graduate from A.P. Shah Institute of Technology.
This project is a demonstration of my understanding of Django REST Framework, where I’ve built a clean and secure backend system to manage users, clients, and projects — including authentication, relationships, and RESTful design.

🔖 Project Overview
This is a Django REST API that supports:

✅ User management (via Django's built-in auth)

✅ Client: A company or organization

✅ Project: A task or project assigned to clients and users

Includes token-based login using Django REST Framework's auth token system.

⚙️ Setup Instructions
1️⃣ Clone the repository
bash
git clone https://github.com/your-username/client-project-api.git
cd client-project-api
2️⃣ Create and activate a virtual environment
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
3️⃣ Install dependencies
pip install django djangorestframework djangorestframework-authtoken
4️⃣ Run migrations
python manage.py migrate
5️⃣ Create superuser (admin access)
python manage.py createsuperuser
6️⃣ Start the development server
python manage.py runserver
🔐 Authentication
Use Django REST Framework's token-based login system.

Endpoint:

POST /api-token-auth/
Body:

json
{
  "username": "your_username",
  "password": "your_password"
}
Response:

json

{
  "token": "your_token_here"
}
Use this token in headers:

makefile

Authorization: Token your_token_here
📮 API Endpoints
🔹 Clients
Method	Endpoint	Description
GET	/api/clients/	List all clients
POST	/api/clients/	Create a new client
GET	/api/clients/<id>/	Retrieve a single client + projects
PUT	/api/clients/<id>/	Update a client
DELETE	/api/clients/<id>/	Delete a client

🔹 Projects
Method	Endpoint	Description
POST	/api/clients/<client_id>/projects/	Create a project for a specific client
GET	/api/my-projects/	List projects assigned to the current user

🔹 Auth
Method	Endpoint	Description
POST	/api-token-auth/	Get login token

🧑‍💻 Admin Panel
Visit: http://localhost:8000/admin/

Log in with your superuser account

Manage users, clients, and projects from the UI

📌 Models Summary
Client
client_name

created_by (User FK)

created_at, updated_at

Project
project_name

client (FK to Client)

users (Many-to-Many with User)

created_by (User FK)

created_at

✅ What I Learned / Implemented
Django REST Framework basics and generic views

Token Authentication for secure API access

Nested serializers and model relationships

RESTful routing and clean code organization

✨ About Me
I’m Vinayak Sharma, an enthusiastic IT engineer from A.P. Shah Institute of Technology, passionate about backend development, APIs, and building practical applications using Python and Django

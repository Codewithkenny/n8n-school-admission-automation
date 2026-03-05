📌 Project Title

n8n School Admission Automation System

📖 Project Description

This project is an automation workflow built with n8n and PostgreSQL to streamline the student admission process for schools.

The system receives admission applications through a webhook endpoint, stores applicant information in a PostgreSQL database, generates a unique application ID, and prepares the data for further automated processes such as notifications and admission tracking.

The workflow demonstrates how automation tools can be used to replace manual admission processing, reduce administrative workload, and improve data management in educational institutions.

This project is designed as a real-world automation portfolio project, showcasing how modern workflow automation platforms can integrate APIs, databases, and business logic.


Technologies Used

n8n – Workflow automation and orchestration

PostgreSQL – Database for storing applicants and applications

Docker – Containerized deployment

Postman – Testing webhook endpoints

JavaScript – Data processing inside n8n Code node

🚀 Features

Webhook endpoint for receiving admission applications

Secure API authentication

Automatic applicant data storage in PostgreSQL

Unique application ID generation

Modular workflow architecture for easy extension

Containerized deployment using Docker

📊 Workflow Overview
Admission Form / API Request
           │
           ▼
        Webhook
           │
           ▼
   Insert Applicant (PostgreSQL)
           │
           ▼
 Generate Application ID
           │
           ▼
 Insert Application Record
           │
           ▼
 Future Automations (Email / Notifications)
🗄 Database Structure
Applicants Table

Stores personal information about the student and parent.

Example fields:

id
full_name
email
phone
date_of_birth
parent_name
parent_phone
created_at
Applications Table

Stores admission application records.

Example fields:

application_id
applicant_id
class_applied
admission_year
application_status
created_at
🐳 Running the Project
1️⃣ Clone the repository
git clone https://github.com/YOUR_USERNAME/n8n-school-admission-automation.git
cd n8n-school-admission-automation
2️⃣ Create environment variables

Create .env

POSTGRES_PASSWORD=yourpassword
N8N_BASIC_AUTH_PASSWORD=yourpassword
3️⃣ Start containers
docker compose up -d
4️⃣ Open n8n
http://localhost:5678

Login with:

username: admin
password: (value from .env)
🔌 Example Webhook Request

Example POST request to submit an application:

POST http://localhost:5678/webhook-test/admissions/new

Example JSON:

{
  "full_name": "John Doe",
  "email": "parent@example.com",
  "phone": "+2348012345678",
  "parent_name": "Jane Doe",
  "parent_phone": "+2348098765432",
  "class_applied": "JSS 1",
  "admission_year": 2026
}
🎯 Project Purpose

This project demonstrates how workflow automation can solve real operational problems in schools by:

Reducing manual data entry

Improving record management

Automating admission workflows

Integrating multiple systems through APIs

It also serves as a portfolio project for automation engineering, workflow automation, and backend integration roles.

🔮 Future Improvements

Email notifications to parents

WhatsApp admission alerts

Admin dashboard

Admission status tracking

File uploads for documents


📝 License

This project is licensed under the MIT License – see the LICENSE
 file for details.

MIT License

Copyright (c) 2026 Your Name

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

Payment integration

👨‍💻 Author

Automation workflow project built as a hands-on learning project in workflow automation and backend integration.

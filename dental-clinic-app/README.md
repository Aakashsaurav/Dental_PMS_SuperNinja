# Dental Clinic Management & Patient Engagement WebApp

A modular full-stack web application that manages patient data, clinic operations, and patient engagement for a dental practice.

## Features

- **Authentication & Authorization**: Secure login system with role-based access control (Admin, Doctor, Receptionist) 
- **Patient Management**: Add, edit, and delete patient records with detailed information
- **Appointments & Scheduling**: Book appointments with calendar integration and automatic reminders
- **Prescriptions & Invoices**: Create and print digital prescriptions and invoices
- **Clinical Records**: Tooth chart UI with case notes and file uploads
- **AI Integration**: Connect with multiple AI providers for diagnosis support, prescription validation, and more
- **Messaging & Engagement**: Send automated WhatsApp reminders, SMS, and emails
- **Admin Features**: Expense management, user management, and AI-generated insights

## Tech Stack

### Backend
- **Framework**: FastAPI (Python)
- **Database**: PostgreSQL with SQLite fallback
- **Authentication**: JWT with role-based access control
- **File Storage**: Local, S3, or Firebase (configurable)
- **AI Integration**: OpenAI, Anthropic Claude (configurable)
- **PDF Generation**: WeasyPrint and ReportLab

### Frontend
- **Framework**: React with TypeScript
- **UI Library**: Material-UI and Tailwind CSS
- **State Management**: React Query
- **Forms**: Formik with Yup validation
- **Routing**: React Router
- **Charts**: Chart.js with React-Chartjs-2

## Getting Started

### Prerequisites
- Docker and Docker Compose
- Node.js 18+ (for local development)
- Python 3.11+ (for local development)

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/dental-clinic-app.git
   cd dental-clinic-app
   ```

2. Start the application using Docker Compose:
   ```bash
   docker-compose up -d
   ```

3. Access the application:
   - Frontend: http://localhost:3000
   - Backend API: http://localhost:8000
   - API Documentation: http://localhost:8000/docs

### Default Admin Credentials
- Email: admin@example.com
- Password: admin

## Development Setup

### Backend

1. Navigate to the backend directory:
   ```bash
   cd backend
   ```

2. Create a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Create a `.env` file with the following content:
   ```
   POSTGRES_SERVER=localhost
   POSTGRES_USER=postgres
   POSTGRES_PASSWORD=postgres
   POSTGRES_DB=dental_clinic
   ```

5. Run the application:
   ```bash
   python run.py
   ```

### Frontend

1. Navigate to the frontend directory:
   ```bash
   cd frontend
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file with the following content:
   ```
   REACT_APP_API_URL=http://localhost:8000/api/v1
   ```

4. Run the application:
   ```bash
   npm start
   ```

## Deployment

The application can be deployed using Docker Compose for a production environment:

```bash
docker-compose -f docker-compose.yml up -d
```

## License

This project is licensed under the MIT License - see the LICENSE file for details.

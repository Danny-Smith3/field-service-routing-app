# Field Service Routing App

A full-stack SaaS platform for scheduling, dispatching, and optimizing field service operations.  
Built for teams that need to assign, track, and route technicians efficiently — with modern web technologies.

---

## Tech Stack

### **Frontend**
- **React.js** (TypeScript)
- **Vite** (for fast local development)
- **Tailwind CSS** (UI styling)
- **React Query** for API state management
- **React Router** for page navigation
- **Vercel** for deployment (early development)

### **Backend**
- **Node.js** + **Express**
- **PostgreSQL** (via AWS RDS)
- **Redis** (AWS ElastiCache) for caching and async task queues
- **JWT Authentication** with bcrypt
- **AWS Elastic Beanstalk** for deployment
- **CloudWatch** for logging and monitoring

### **Infrastructure**
- **S3** for file storage (e.g., work order attachments)
- **GitHub Actions** for CI/CD
- **AWS Parameter Store (SSM)** for secrets management

---

## Core Features (MVP)

- **User Authentication** (Register, Login, JWT-based sessions)
- **Job Scheduling** – create and assign jobs to technicians
- **Route Optimization** – plan efficient routes for daily schedules
- **Team Dashboard** – visualize field assignments on a map
- **Real-Time Updates** – live job status tracking (using WebSockets or polling)
- **Job History & Notes** – technicians can upload notes/photos per task

---

## Project Structure

```bash
field-service-routing-app/
│
├── backend/
│   ├── src/
│   │   ├── api/
│   │   ├── models/
│   │   ├── services/
│   │   ├── utils/
│   │   └── index.ts
│   ├── tests/
│   ├── Dockerfile
│   └── package.json
│
├── frontend/
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── hooks/
│   │   ├── services/
│   │   └── App.tsx
│   ├── public/
│   ├── package.json
│   └── vite.config.ts
│
├── .github/
│   └── workflows/
│       └── deploy.yml
│
├── docker-compose.yml
├── README.md
└── LICENSE

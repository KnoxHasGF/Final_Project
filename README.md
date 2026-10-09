# PetCare

PetCare is a full-stack pet health and appointment management system. Pet owners can manage multiple pets, store pet-specific health records, browse veterinarians, and manage appointments from a responsive web application.

## Live application

https://full-stack-crud-app-9z54.vercel.app/

## Features

- Visitor Home page with public doctor and appointment information
- User registration, sign in, and sign out
- Add and manage multiple pets
- Create pet-specific vaccination, treatment, allergy, medication, and observation records
- Switch between pets when viewing or adding health records
- Browse veterinarian profiles
- Create and manage appointments
- Responsive desktop and mobile navigation
- Admin management for users, doctors, and time slots

## Technology

- React and Vite frontend
- Next.js REST API backend
- MongoDB database
- JavaScript and CSS
- Vercel deployment

## Project structure

```text
Full-Stack-CRUD-App/
├── react-frontend/   # React and Vite frontend
├── next-backend/     # Next.js REST API and MongoDB integration
├── PetCare-Project-Proposal.docx
└── README.md
```

## Run locally

### Backend

```bash
cd next-backend
npm install
cp .env.local.example .env.local
npm run dev
```

Set `MONGODB_URI`, `DB_NAME`, `SESSION_SECRET`, and `CORS_ORIGIN` in `.env.local`.

### Frontend

```bash
cd react-frontend
npm install
npm run dev
```

The frontend runs at `http://localhost:5173` and uses `http://localhost:3000` as the default API URL. To change it, set:

```env
VITE_API_BASE_URL=http://localhost:3000
```

Never commit `.env.local` files or database credentials.

## Main API routes

| Resource | Collection route | Required create fields |
| --- | --- | --- |
| Pets | `/api/pets` | `name`, `species` |
| Health records | `/api/health-records` | `petId`, `type`, `title`, `recordDate` |
| Appointments | `/api/appointments` | `petId`, `clinicName`, `startsAt`, `reason` |
| Doctors | `/api/doctors` | `name`, `clinicName`, `specialty` |

Each resource supports `GET`, `POST`, `PUT`, and `DELETE` operations. Health records and appointments can be filtered with `?petId=...`.

## Authentication routes

- `POST /api/auth/sign-up`
- `POST /api/auth/sign-in`
- `GET /api/auth/session`
- `DELETE /api/auth/session`

## Team

- Nyein Chan Htet Naing
- Myat Phone Paye
- Lin Myat Thu

## ## Application Screenshots

### 1. Sign In
<img width="1908" height="906" alt="image" src="https://github.com/user-attachments/assets/0426bc3d-5221-48e4-b267-19048bb3e392" />

### 2. Sign Up
<img width="1889" height="917" alt="image" src="https://github.com/user-attachments/assets/a7d52404-5379-459d-82bc-c673aa97124d" />

### 3. Add a Pet
<img width="1909" height="917" alt="image" src="https://github.com/user-attachments/assets/1ce9ffb1-8d6a-4ec0-ba6c-1f613ca96310" />

### 4. Choose a Doctor
<img width="1911" height="913" alt="image" src="https://github.com/user-attachments/assets/27c19d08-de9c-47e9-b324-0ad050ce1514" />

### 5. Select Appointment Date and Time
<img width="1886" height="914" alt="image" src="https://github.com/user-attachments/assets/68f03a52-6ebe-435b-9001-775f1cdd7df6" />

### 6. Appointment Schedule
<img width="1918" height="916" alt="image" src="https://github.com/user-attachments/assets/d3647c15-0959-4e82-b591-fdae96eb9dfb" />

### 7. Pet Health Records
<img width="1907" height="913" alt="image" src="https://github.com/user-attachments/assets/aab26cad-00ba-4e19-bdfe-da83cc65beb1" />

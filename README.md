<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=30&duration=3500&pause=900&color=06B6D4&center=true&vCenter=true&width=720&height=80&lines=Rentiva;Find%2C+list+and+manage+rental+properties;A+full-stack+real+estate+platform" alt="Rentiva" />

### 🏠 A full-stack property rental marketplace for tenants & managers

![Next.js](https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=nextdotjs&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![Express](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-2D3748?style=for-the-badge&logo=prisma&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonwebservices&logoColor=white)
![Mapbox](https://img.shields.io/badge/Mapbox-000000?style=for-the-badge&logo=mapbox&logoColor=white)

<a href="https://rentiva-cyan.vercel.app">
  <img src="https://img.shields.io/badge/Live_Demo-rentiva--cyan.vercel.app-06B6D4?style=for-the-badge&logo=vercel&logoColor=white" alt="Live Demo" />
</a>

</div>

---

## 🧭 Overview

**Rentiva** is a full-stack real estate rental platform with two distinct experiences: **tenants** can search for properties on an interactive map, filter listings, favorite homes, and submit rental applications — while **managers** can list properties, upload photos, and review incoming applications. It's a monorepo with a Next.js front end and an Express + Prisma API.

## ✨ Features

### 👤 For Tenants
- 🔍 **Map-based search** — explore listings on an interactive Mapbox map
- 🎛️ **Advanced filters** — price, beds, baths, amenities, and more
- ❤️ **Favorites** — save properties you love
- 📝 **Applications** — apply to rent directly from a listing
- 🏡 **Residences dashboard** — track your current and past leases

### 🧑‍💼 For Managers
- ➕ **List properties** — create listings with photo uploads
- 🗂️ **Property management** — edit and manage your portfolio
- 📨 **Application review** — accept or decline tenant applications
- ⚙️ **Settings** — manage your profile and preferences

### 🔐 Platform
- Role-based authentication via **AWS Cognito**
- Property images stored in **AWS S3**
- Geospatial search powered by PostgreSQL + Prisma

## 🛠️ Tech Stack

| Side | Technologies |
| --- | --- |
| **Frontend** | Next.js (App Router), TypeScript, Redux Toolkit, AWS Amplify, Mapbox GL, FilePond, Framer Motion, Tailwind CSS, shadcn/ui |
| **Backend** | Express, TypeScript, Prisma ORM, PostgreSQL, AWS S3, JWT |

## 📁 Project Structure

```
rentiva/
├── client/   # Next.js front end
│   └── src/app/
│       ├── (auth)/          # Authentication
│       ├── (dashboard)/     # Manager & tenant dashboards
│       └── (nondashboard)/  # Landing page & property search
└── server/   # Express + Prisma API
    └── src/
        ├── controllers/     # Property, tenant, manager, lease, application
        ├── routes/          # API routes
        └── middleware/      # Auth middleware
```

## 🚀 Getting Started

### Prerequisites

- Node.js 18+ and npm
- A PostgreSQL database
- AWS account (Cognito + S3) and a Mapbox access token

### 1. Backend

```bash
cd server
npm install

# configure server/.env (see below)
npx prisma generate
npx prisma migrate dev
npm run seed        # optional: load sample data
npm run dev
```

### 2. Frontend

```bash
cd client
npm install

# configure client/.env (see below)
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) in your browser.

### Environment Variables

> *Confirm the exact variable names against the source before deploying.*

**`server/.env`**
```env
PORT=3001
DATABASE_URL="postgresql://..."
AWS_ACCESS_KEY_ID=""
AWS_SECRET_ACCESS_KEY=""
S3_BUCKET_NAME=""
```

**`client/.env`**
```env
NEXT_PUBLIC_API_BASE_URL="http://localhost:3001"
NEXT_PUBLIC_AWS_COGNITO_USER_POOL_ID=""
NEXT_PUBLIC_AWS_COGNITO_USER_POOL_CLIENT_ID=""
NEXT_PUBLIC_MAPBOX_ACCESS_TOKEN=""
```

<div align="center">

---

Built with 🩵 by [**Keshav Kumar**](https://github.com/Keshavkumar04)

</div>

# Novus-Code - Cloud-Native Online IDE

Novus-Code is a cloud-native Online Integrated Development Environment (IDE) that enables users to write, manage, and execute code directly from the browser. It provides isolated development environments, real-time terminal interaction, and persistent cloud storage for projects.

## Features

- Advanced code editor powered by **Monaco Editor** with syntax highlighting and code completion.
- Interactive browser-based terminal using **xterm.js**.
- Dynamic provisioning of isolated user environments through **Kubernetes**.
- Real-time file synchronization and terminal streaming using **Socket.io**.
- Persistent project storage integrated with **AWS S3**.
- Secure user authentication and scalable backend architecture.

## Architecture

The project consists of three services:

### Frontend

- Built with **React**, **Vite**, and **TailwindCSS**.
- Hosts the Monaco Editor, terminal interface, and file explorer.

### Backend API

- Developed using **Node.js**, **Express**, and **TypeScript**.
- Handles authentication, file management, and database operations.
- Streams terminal output and file updates via **WebSockets**.

### Kubernetes Controller

- Dedicated service using **@kubernetes/client-node**.
- Responsible for creating and managing isolated user-specific pods.

## Tech Stack

| Layer | Technologies |
|---|---|
| Frontend | React, Vite, TailwindCSS, Monaco Editor, xterm.js |
| Backend | Node.js, Express, TypeScript, Socket.io |
| Database | PostgreSQL, Drizzle ORM |
| Infrastructure | Kubernetes, Docker, AWS S3 |
| Validation | Zod |

## Getting Started

### Prerequisites

- Node.js (v18+)
- PostgreSQL
- Kubernetes Cluster (Minikube or Docker Desktop)
- AWS S3 Credentials

### Installation

```bash
git clone https://github.com/<username>/novus-code.git
cd novus-code
```

Install dependencies for each service:

```bash
cd front-end
npm install
npm run dev
```

```bash
cd code
npm install
npm run dev
```

```bash
cd k8s
npm install
npm run dev
```

Configure the required environment variables before starting the backend services.

# Cloud-Native Online Judge Platform

A scalable online judge inspired by LeetCode and HackerRank that enables users to write, compile, and execute code securely in isolated environments with real-time feedback and asynchronous execution pipelines.

## 🚀 Features

* Advanced code editor powered by **Monaco Editor** with syntax highlighting and autocompletion.
* Interactive browser-based terminal using **xterm.js**.
* Secure multi-language code compilation and execution.
* Real-time output streaming using **WebSockets (Socket.io)**.
* Asynchronous execution pipelines backed by **Redis**.
* Persistent storage for submissions and user data using **PostgreSQL**.
* Automated CI/CD workflows using **GitHub Actions**.

## 🏗 Architecture

The project consists of three services:

### Frontend

* Built with **React**, **Vite**, and **TailwindCSS**.
* Hosts the Monaco Editor, terminal interface, and submission dashboard.

### Backend API

* Developed using **Node.js**, **Express**, and **TypeScript**.
* Handles authentication, submission management, and database operations.
* Streams execution logs and results through **WebSockets**.

### Execution Workers

* Consume jobs from **Redis** queues.
* Compile and execute user code securely.
* Return execution status and outputs to the backend.

## 🛠 Tech Stack

| Layer      | Technologies                                      |
| ---------- | ------------------------------------------------- |
| Frontend   | React, Vite, TailwindCSS, Monaco Editor, xterm.js |
| Backend    | Node.js, Express, TypeScript, Socket.io           |
| Database   | PostgreSQL                                        |
| Queue      | Redis                                             |
| CI/CD      | GitHub Actions                                    |
| Validation | Zod                                               |

## 🚦 Getting Started

### Prerequisites

* Node.js (v18+)
* PostgreSQL
* Redis

### Installation

```bash
git clone https://github.com/<username>/<repository-name>.git
cd <repository-name>
```

Install dependencies:

```bash
npm install
npm run dev
```

Configure the required environment variables before starting the services.

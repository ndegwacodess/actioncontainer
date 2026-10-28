# Containerized Full-Stack Deployment

A hands-on project for deploying a decoupled, API-driven application using containers. The frontend runs as a standalone service and communicates with a separate backend API.

## Overview

This project guides you through containerizing and deploying three independent components:

| Component | Technology | Role |
|-----------|------------|------|
| Frontend  | React (Vite) | Standalone single-page application |
| Backend   | Laravel | REST API, provided and ready to use (Check The Opensource Project Called ActionContainerLaravel) |
| Database  | PostgreSQL | Persistent data storage (Check the Folder called DockerDatabases)|

The backend is already built. Your focus is on packaging each component into a container and deploying them together.

## Architecture

```
Browser
├── Frontend (static files served by nginx)
└── API requests → Backend (Laravel)
                     └── PostgreSQL
```

## Getting Started

### 1. Review the documentation

Each component has its own README. Read them before you begin, as they explain how each service is configured and how the services interact. Start with the backend, since the frontend depends on it.

### 2. Create the frontend

Scaffold the React application with Vite:

```bash
npm create vite@latest
```

Choose the React template when prompted.

### 3. Containerize and deploy

Follow the steps in each component's README to build the images and run the full stack.

## Prerequisites

- Docker and Docker Compose
- Node.js 22 or later (for local frontend development)
- Basic familiarity with Git and the command line

## Learning Objectives

- Containerizing a React/Vite application with multi-stage builds
- Running a Laravel API in a container
- Connecting services with Docker networking and Compose
- Managing configuration through environment variables
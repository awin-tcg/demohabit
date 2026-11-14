# Habit Tracker

A web app that tracks habit goals and encourages people to stick with them. Built by Team ACD for CS 410 Software Engineering at Bellevue College.

**Live demo:** https://demohabit.vercel.app

## Overview

Users enter the habits they want to build and log each day they follow through. The app stores that data in a cloud SQL backend and uses it to show progress and motivate consistency with features like streaks.

The frontend is a single-page application that talks to the backend through an HTTP REST API, so neither side depends on the other's implementation details.

## Architecture

| Layer | Technology |
|---|---|
| Frontend | TypeScript, React, Vite, Tailwind CSS, TanStack Query, Zustand |
| Backend | ASP.NET Core Web API |
| Database | PostgreSQL |
| Hosting | Vercel (frontend), AWS Lightsail (backend and database) |

## Project layout

```
frontend/            React single-page application
  src/
    components/      habit cards, date picker, streak badge, navigation
    hooks/           data hooks (useSession, useHabits, log queries)
    services/        API client, authentication, time zone handling
    stores/          session state
    views/           pages
backend/             ASP.NET Core API (controllers, services, data models)
backend-complete/    backend variant with the database context
```

## Run it locally

Frontend:

```bash
cd frontend
npm install
npm run dev
```

Backend (requires the .NET SDK):

```bash
cd backend
dotnet run
```

## Team

Team ACD, CS 410, Bellevue College, Spring 2026. Allen Nguyen led the frontend.

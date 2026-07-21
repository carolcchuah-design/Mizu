# Mizu
Mizu Family Care Plan

# Mizu Care

A mobile-first Progressive Web App (PWA) for managing Mizu's daily care schedule, tracking family responsibilities, and recording important milestones.

---

## Overview

Mizu Care helps our family stay organized by providing a simple daily schedule for caring for Mizu. The app makes it easy to see what needs to be done, record completed tasks, and keep a history of Mizu's growth and care.

The application is designed to be fast, intuitive, and enjoyable for both adults and children.

---

# Core Features

### Today

* Current task
* Next task
* Daily progress
* Today's schedule
* Quick actions

### Task Management

* One-tap task completion
* Family member sign-off
* Automatic timestamps
* Progress tracking

### Leaderboards

* Daily
* Weekly
* Monthly
* All-Time

### History

* Completed tasks
* Search and filters
* Adult editing

### Potty Log

* Quick accident logging
* Notes
* Optional photos

### Growth Journal

* Photos
* Weight tracking
* Milestones
* Vet visits
* Vaccinations

### Notifications

* Scheduled reminders
* Success sounds
* Browser notifications

---

# Technology Stack

## Frontend

* Next.js 15 (App Router)
* React
* TypeScript
* Tailwind CSS
* shadcn/ui
* Framer Motion

## Backend

* Supabase

  * Authentication
  * Database
  * Storage
  * Realtime

## Deployment

* Vercel (recommended)

---

# Project Structure

```text
mizu-care/
│
├── app/
├── components/
├── features/
├── hooks/
├── lib/
├── public/
├── services/
├── supabase/
├── docs/
└── README.md
```

---

# Documentation

Project documentation is located in the **docs/** folder.

| Document                       | Purpose                              |
| ------------------------------ | ------------------------------------ |
| 01-Product-Vision.md           | Overall vision and goals             |
| 02-Product-Requirements.md     | Functional requirements              |
| 03-User-Stories.md             | User stories and acceptance criteria |
| 04-Information-Architecture.md | Navigation and application structure |
| 05-UI-Design-System.md         | Visual design standards              |
| 06-System-Architecture.md      | Technical architecture               |
| 07-Database-Specification.md   | Data model                           |
| 08-Development-Roadmap.md      | Development milestones               |

Always consult the relevant document before implementing a feature.

---

# Development Principles

The project follows a few simple principles:

* Mobile-first design
* Keep the interface simple
* Prefer reusable components
* Build one milestone at a time
* Test before adding new features
* Avoid unnecessary complexity
* Maintain accessibility standards
* Keep performance a priority

---

# Current MVP Scope

The first production-ready version includes:

* User authentication
* Today screen
* Schedule generation
* Task completion
* Daily progress tracking
* Leaderboards
* History
* Potty Log
* Growth Journal
* Notifications
* Recurring care reminders

Anything outside this scope should be treated as a future enhancement unless explicitly approved.

---

# Getting Started

## Prerequisites

* Node.js (LTS)
* npm or pnpm
* Git
* Supabase account
* GitHub account
* Vercel account (recommended)

---

## Installation

```bash
git clone <repository-url>

cd mizu-care

npm install
```

Create a `.env.local` file and add your Supabase credentials.

```env
NEXT_PUBLIC_SUPABASE_URL=your-project-url

NEXT_PUBLIC_SUPABASE_ANON_KEY=your-anon-key
```

Run the development server.

```bash
npm run dev
```

Open:

```text
http://localhost:3000
```

---

# Development Workflow

Follow the roadmap in **08-Development-Roadmap.md**.

Work on **one phase at a time**.

Recommended workflow:

1. Select the current roadmap phase.
2. Review the relevant documentation.
3. Build the feature.
4. Test thoroughly.
5. Commit changes.
6. Move to the next phase.

Avoid working on multiple phases simultaneously.

---

# Design Goals

Mizu Care should feel:

* Friendly
* Modern
* Lightweight
* Fast
* Easy for children
* Reliable enough for everyday use

The app should answer one question immediately:

> **What does Mizu need right now?**

Every design and development decision should support this goal.

---

# Future Enhancements

Possible future additions include:

* Multiple pets
* Multiple families
* Rewards and achievements
* Push notifications
* Native mobile apps
* Calendar integration
* Smart reminders

These features are intentionally out of scope for Version 1.

---

# License

This project is intended for private family use unless otherwise specified.

---

# Development Status

**Current Phase:** Planning Complete

The project documentation is complete and development is ready to begin with **Phase 1 – Project Foundation** as defined in **08-Development-Roadmap.md**.

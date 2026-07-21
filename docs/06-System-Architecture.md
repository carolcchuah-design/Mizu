# 06 - System Architecture

**Project:** Mizu Care
**Version:** 1.0

---

# Purpose

This document describes the overall architecture of the Mizu Care application.

The goal is to build a simple, maintainable, and scalable application that works well on mobile devices while remaining easy to understand and extend.

---

# Architecture Overview

Mizu Care consists of four primary layers:

```text
+--------------------------------------------------+
|                  User Interface                  |
|  Today • Leaderboard • History • Settings        |
+--------------------------------------------------+
                     │
                     ▼
+--------------------------------------------------+
|              Application Logic                   |
|  Schedule • Points • Notifications • Rules       |
+--------------------------------------------------+
                     │
                     ▼
+--------------------------------------------------+
|                 Data Services                    |
|  Authentication • Database • File Storage        |
+--------------------------------------------------+
                     │
                     ▼
+--------------------------------------------------+
|                 Cloud Backend                    |
|               Supabase Platform                  |
+--------------------------------------------------+
```

Each layer should have a single responsibility.

---

# Frontend

The frontend is responsible for:

* Displaying screens
* User interaction
* Form validation
* Animations
* Navigation
* Local caching
* Offline support

The frontend should never contain permanent business data.

---

# Backend

The backend is responsible for:

* User authentication
* Data storage
* File storage
* Data synchronization
* Security
* Authorization

The backend should be the single source of truth.

---

# Core Modules

The application is organized into independent modules.

## Today

Responsible for:

* Current Task
* Next Task
* Progress
* Today's Schedule
* Quick Actions

---

## Schedule

Responsible for:

* Loading today's schedule
* Determining current task
* Friday rules
* Weekend schedules
* Recurring reminders

---

## Task Manager

Responsible for:

* Completing tasks
* Recording timestamps
* Updating status
* Sign-off workflow

---

## Leaderboards

Responsible for:

* Point totals
* Daily rankings
* Weekly rankings
* Monthly rankings
* All-Time rankings

---

## History

Responsible for:

* Completed tasks
* Activity history
* Search
* Filters

---

## Potty Log

Responsible for:

* Recording accidents
* Viewing history
* Future reporting

---

## Growth Journal

Responsible for:

* Photos
* Weight
* Milestones
* Vet visits
* Vaccinations

---

## Notifications

Responsible for:

* Reminder timing
* Sounds
* Browser notifications

---

## Settings

Responsible for:

* Appearance
* Notification preferences
* Sounds
* Admin options

---

# Data Flow

Normal task completion follows this flow:

```text
User taps Complete

        │

        ▼

Choose Family Member

        │

        ▼

Validate Task

        │

        ▼

Save Completion

        │

        ▼

Update Progress

        │

        ▼

Update Leaderboard

        │

        ▼

Refresh Today Screen
```

Every module should react automatically when shared data changes.

---

# State Management

The application should maintain one shared application state.

Examples include:

* Current user
* Today's schedule
* Completed tasks
* Progress
* Leaderboard
* Settings

Screens should read from shared state instead of maintaining duplicate copies.

---

# Offline Strategy

When offline:

* Continue displaying today's schedule.
* Allow task completion.
* Allow potty logging.
* Allow journal entries.

Offline actions should be stored locally.

When internet connectivity returns:

* Automatically synchronize pending changes.
* Resolve conflicts safely.
* Refresh application data.

Users should not need to manually retry synchronization.

---

# Authentication

Users should sign in before accessing the application.

Each user belongs to one family.

Permissions are determined by role:

Adults

* Full access

Children

* Limited access

Authentication should remain invisible after the initial login.

---

# File Storage

Photos are stored separately from application data.

Examples:

* Growth Journal photos
* Potty accident photos

Application records should store only references to uploaded images.

---

# Error Handling

Errors should be handled consistently throughout the application.

Categories include:

* Network
* Authentication
* Validation
* Synchronization
* File upload

Whenever possible:

* Explain the problem.
* Preserve user data.
* Allow retry.

---

# Performance Goals

The application should feel responsive at all times.

Target goals:

* Initial load under 2 seconds
* Screen transitions under 300 milliseconds
* Task completion feedback under 1 second
* Smooth scrolling at 60 FPS where possible

Performance should take priority over unnecessary animations.

---

# Security

The application should ensure:

* Secure authentication
* Encrypted communication
* Role-based permissions
* Protected user data
* Secure file uploads

Users should only be able to access data belonging to their own family.

---

# Scalability

Although Version 1 is designed for a single family, the architecture should support future expansion.

Potential future enhancements include:

* Multiple families
* Multiple pets
* Shared households
* Custom schedules
* Rewards
* Push notifications
* Native mobile apps

These additions should not require major architectural changes.

---

# Design Principles

The architecture should always prioritize:

* Simplicity
* Reliability
* Maintainability
* Performance
* Clear separation of responsibilities

New features should be added as independent modules whenever possible rather than modifying existing functionality.


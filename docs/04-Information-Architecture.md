# 04 - Information Architecture

**Project:** Mizu Care
**Version:** 1.0

---

# Purpose

This document defines how the application is organized, how users navigate between screens, and how information is presented.

The goal is to make the application intuitive enough that any family member can use it without instructions.

---

# Application Structure

```
Mizu Care

├── Today
│   ├── Current Task
│   ├── Next Task
│   ├── Daily Progress
│   ├── Quick Actions
│   ├── Today's Schedule
│   └── Leaderboard Preview
│
├── Leaderboard
│   ├── Daily
│   ├── Weekly
│   ├── Monthly
│   └── All-Time
│
├── History
│   ├── Completed Tasks
│   ├── Potty Accident Log
│   ├── Growth Journal
│   └── Search & Filters
│
└── Settings
    ├── Theme
    ├── Notifications
    ├── Sounds
    ├── Recurring Care
    └── Admin Options
```

---

# Primary Navigation

The application uses a fixed bottom navigation bar.

```
+------------------------------------------------+
|                                                |
|                 Active Screen                  |
|                                                |
+------------------------------------------------+
|                                                |
|   🏠 Today   🏆 Leaderboard   📖 History   ⚙️ Settings   |
|                                                |
+------------------------------------------------+
```

Navigation should always remain visible.

The current page should be clearly highlighted.

---

# Today Screen Layout

```
+----------------------------------+

 Current Task

------------------------------------

 Next Task

------------------------------------

 Daily Progress

------------------------------------

 Quick Actions

 [Potty] [Journal] [History]

------------------------------------

 Today's Schedule

 6:00 AM

 6:30 AM

 8:30 AM

 ...

------------------------------------

 Leaderboard Preview

+----------------------------------+
```

The Today screen should be scrollable.

Users should rarely need to leave this page during normal daily use.

---

# Current Task Card

```
+----------------------------------+

Current Task

6:00 AM

Morning Potty

Responsible: Adult

⭐ 1 Point

[ Complete Task ]

+----------------------------------+
```

After completion:

```
✓ Completed

By Carol

6:04 AM
```

---

# Schedule Card

```
+----------------------------------+

6:30 AM

Breakfast

Adult

⭐ 1

[✓]

+----------------------------------+
```

Status colors:

Gray = Upcoming

Blue = Current

Green = Completed

Yellow = Overdue

---

# Completion Flow

```
Tap Checkbox

      │

      ▼

Choose Family Member

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

Play Animation
```

---

# Leaderboard Layout

```
Daily

🥇 Carol

32

---------------------

🥈 Bryan

29

---------------------

🥉 Ash

24

---------------------

4. Nomi

18

5. Ovi

15

6. Liby

14

7. Nely

12
```

Tabs:

Daily

Weekly

Monthly

All-Time

---

# History Layout

```
History

-----------------------------

Today

✓ Morning Potty

Carol

6:03 AM

-----------------------------

✓ Breakfast

Bryan

6:15 AM

-----------------------------

✓ Walk

Ash

5:00 PM
```

Filters:

Date

Person

Activity

---

# Potty Accident Flow

```
Tap

Log Potty Accident

        │

        ▼

Select

Pee

or

Poop

        │

        ▼

Location

(Optional Notes)

(Optional Photo)

        │

        ▼

Save
```

Target completion time:

Less than five seconds.

---

# Growth Journal Layout

```
Growth Journal

-----------------------

July 14

📷 New Photo

-----------------------

July 10

⚖ Weight

12.4 kg

-----------------------

July 3

🎉 First Beach Trip
```

Entries display newest first.

---

# Settings Structure

```
Settings

----------------------

Appearance

Notifications

Sounds

Recurring Care

Admin
```

Admin options are only visible to adults.

---

# Screen Relationships

```
                 Today
                    │
      ┌─────────────┼─────────────┐
      │             │             │
      ▼             ▼             ▼

Leaderboard     History      Settings
                     │
          ┌──────────┴──────────┐
          ▼                     ▼

Potty Log         Growth Journal
```

---

# User Journey

Morning

```
Open App

↓

Current Task

↓

Complete Task

↓

Progress Updates

↓

Close App
```

Afternoon

```
Reminder

↓

Open App

↓

Complete Task

↓

Close App
```

Evening

```
Dinner

↓

Family Time

↓

Final Potty

↓

100%

↓

Confetti 🎉
```

---

# Design Principles

The application should always feel:

* Fast
* Friendly
* Simple
* Mobile-first
* Easy for children
* Easy to understand at a glance

A family member should never need more than two taps to complete a routine task.

The app should prioritize today's responsibilities over historical information, making the Today screen the central hub for all daily interactions.


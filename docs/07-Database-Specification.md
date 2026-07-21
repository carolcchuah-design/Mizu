# 07 - Database Specification

**Project:** Mizu Care
**Version:** 1.0

---

# Purpose

This document defines the data required by the Mizu Care application.

It describes the information the application stores and the relationships between that information. It is intentionally independent of any specific database technology.

---

# Data Model Overview

The application stores information about:

* Family Members
* Scheduled Tasks
* Task Completions
* Recurring Care
* Potty Logs
* Growth Journal
* Settings

```text
Family Member
      │
      ├──────────────┐
      │              │
      ▼              ▼
Task Completion   Growth Journal
      │
      ▼
Scheduled Task

Recurring Care

Potty Log

Settings
```

---

# Family Member

Represents a person who uses the application.

### Fields

| Field  | Type              | Required |
| ------ | ----------------- | -------- |
| ID     | Unique Identifier | Yes      |
| Name   | Text              | Yes      |
| Role   | Adult / Child     | Yes      |
| Avatar | Image (Optional)  | No       |
| Active | Yes / No          | Yes      |

---

## Rules

* Names should be unique.
* Only active members appear in the sign-off list.
* Adults have additional permissions.

---

# Scheduled Task

Represents a recurring task that appears on the schedule.

### Fields

| Field          | Type                        |
| -------------- | --------------------------- |
| ID             | Unique Identifier           |
| Activity       | Text                        |
| Description    | Text                        |
| Scheduled Time | Time                        |
| Schedule Type  | Weekday / Saturday / Sunday |
| Responsibility | Text                        |
| Point Value    | Number                      |
| Active         | Yes / No                    |

---

## Rules

* A task belongs to one schedule.
* Only active tasks appear.
* Tasks are sorted by scheduled time.

---

# Task Completion

Represents one completed task.

### Fields

| Field           | Type              |
| --------------- | ----------------- |
| ID              | Unique Identifier |
| Task            | Scheduled Task    |
| Completed By    | Family Member     |
| Completion Date | Date              |
| Completion Time | Time              |
| Points Awarded  | Number            |
| Notes           | Optional Text     |

---

## Rules

* One completion per scheduled task.
* Completion cannot exist without a scheduled task.
* Completion cannot exist without a family member.

---

# Recurring Care

Represents reminders that occur every few weeks.

### Fields

| Field          | Type              |
| -------------- | ----------------- |
| ID             | Unique Identifier |
| Activity       | Text              |
| Frequency      | Number of Days    |
| Last Completed | Date              |
| Next Due       | Date              |
| Point Value    | Number            |
| Active         | Yes / No          |

---

## Default Records

Bath

* Frequency: 35 Days

Nail Grinding

* Frequency: 14 Days

---

# Potty Log

Represents an accident record.

### Fields

| Field       | Type              |
| ----------- | ----------------- |
| ID          | Unique Identifier |
| Type        | Pee / Poop        |
| Date        | Date              |
| Time        | Time              |
| Location    | Text              |
| Notes       | Optional Text     |
| Photo       | Optional Image    |
| Recorded By | Family Member     |

---

## Rules

* Type is required.
* Date is required.
* Time is required.
* Photo is optional.

---

# Growth Journal

Represents a journal entry.

### Fields

| Field       | Type                                                        |
| ----------- | ----------------------------------------------------------- |
| ID          | Unique Identifier                                           |
| Entry Type  | Weight / Milestone / Photo / Vet Visit / Vaccination / Note |
| Date        | Date                                                        |
| Title       | Text                                                        |
| Description | Text                                                        |
| Weight      | Optional Number                                             |
| Height      | Optional Number                                             |
| Photo       | Optional Image                                              |
| Created By  | Family Member                                               |

---

## Rules

* Every entry has a date.
* Every entry has a type.
* Photos are optional.

---

# Settings

Represents application preferences.

### Fields

| Field                 | Type                  |
| --------------------- | --------------------- |
| Theme                 | Light / Dark / System |
| Reminder Sounds       | On / Off              |
| Success Sounds        | On / Off              |
| Browser Notifications | On / Off              |

---

# Relationships

## Family Member

Can complete many tasks.

Can create many journal entries.

Can create many potty logs.

---

## Scheduled Task

Can have one completion per day.

---

## Task Completion

Belongs to:

* One Scheduled Task
* One Family Member

---

## Growth Journal

Created by one family member.

---

## Potty Log

Created by one family member.

---

# Validation Rules

## Family Member

* Name required.
* Role required.

---

## Scheduled Task

* Time required.
* Activity required.
* Point value must be greater than zero.

---

## Task Completion

* Family member required.
* Timestamp required.
* Task required.

---

## Potty Log

* Type required.
* Date required.
* Time required.

---

## Growth Journal

* Date required.
* Entry type required.

---

# Retention Policy

The application should retain all records unless an adult intentionally deletes them.

This includes:

* Completed tasks
* Potty logs
* Growth journal entries

Historical information should never expire automatically.

---

# Future Expansion

The data model should support future additions such as:

* Multiple pets
* Multiple families
* Rewards
* Achievements
* Vet appointments
* Medication tracking
* Custom schedules

These additions should not require restructuring the existing data model.

---

# Summary

The Version 1 data model consists of seven primary entities:

* Family Members
* Scheduled Tasks
* Task Completions
* Recurring Care
* Potty Logs
* Growth Journal
* Settings

This model is intentionally simple, covering the current requirements while leaving room for future enhancements without unnecessary complexity.


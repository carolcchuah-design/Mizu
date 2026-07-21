# 05 - UI Design System

**Project:** Mizu Care
**Version:** 1.0

---

# Purpose

This document defines the visual style and reusable UI components for Mizu Care.

The design should feel:

* Friendly
* Clean
* Modern
* Fun
* Mobile-first
* Easy for both children and adults

The interface should encourage quick interactions while making daily puppy care enjoyable.

---

# Design Principles

The UI should follow these principles:

1. Show today's information first.
2. Make common actions obvious.
3. Use large touch targets.
4. Minimize typing.
5. Keep screens uncluttered.
6. Use animation to provide feedback, not distraction.
7. Prioritize readability over decoration.

---

# Color Palette

## Primary

* Blue — Primary actions, navigation, highlights
* Green — Success, completed tasks
* Yellow — Overdue tasks, reminders
* Red — Errors and destructive actions
* Gray — Upcoming tasks, secondary text
* White / Dark Gray — Backgrounds (depending on theme)

---

## Task Status Colors

| Status    | Color  |
| --------- | ------ |
| Upcoming  | Gray   |
| Current   | Blue   |
| Completed | Green  |
| Overdue   | Yellow |

Status should always include both color and an icon for accessibility.

---

# Typography

## Heading

Used for:

* Screen titles
* Section headers

Style:

* Bold
* Large
* High contrast

---

## Body

Used for:

* Descriptions
* Instructions
* Notes

Readable at arm's length on a mobile phone.

---

## Labels

Used for:

* Buttons
* Form fields
* Navigation

Should remain short and easy to scan.

---

# Icons

Use simple, universally recognizable icons.

Suggested icons:

| Feature        | Icon |
| -------------- | ---- |
| Today          | 🏠   |
| Leaderboard    | 🏆   |
| History        | 📖   |
| Settings       | ⚙️   |
| Potty          | 🐾   |
| Growth Journal | 📷   |
| Weight         | ⚖️   |
| Vet Visit      | 🩺   |
| Vaccination    | 💉   |
| Milestone      | ⭐    |
| Reminder       | 🔔   |
| Success        | ✅    |
| Error          | ⚠️   |

Icons should always be accompanied by text.

---

# Buttons

## Primary Button

Used for:

* Complete Task
* Save
* Continue

Characteristics:

* Full width when appropriate
* Rounded corners
* High contrast
* Easy to tap

---

## Secondary Button

Used for:

* Cancel
* Back
* View Details

Should be visually less prominent.

---

## Icon Button

Used for:

* Quick Actions
* Navigation
* Floating controls

Minimum touch area should be 44 × 44 pixels.

---

# Cards

The application is built primarily using cards.

Examples include:

* Current Task
* Next Task
* Schedule Item
* Journal Entry
* History Entry
* Leaderboard Row

Each card should include:

* Rounded corners
* Consistent spacing
* Subtle shadow
* Clear hierarchy
* Comfortable touch area

---

# Forms

Forms should require as little typing as possible.

Prefer:

* Buttons
* Pickers
* Toggles
* Dropdowns
* Date pickers

Avoid long text input unless necessary.

---

# Bottom Navigation

Navigation should remain fixed to the bottom of the screen.

Items:

* 🏠 Today
* 🏆 Leaderboard
* 📖 History
* ⚙️ Settings

The active page should be clearly highlighted.

---

# Progress Indicator

Display daily progress using a circular progress ring.

Also display:

* Percentage complete
* Tasks completed
* Tasks remaining

Update immediately after task completion.

---

# Task Cards

Each task card displays:

* Time
* Activity
* Description
* Responsibility
* Point value
* Status
* Completion checkbox

Cards should visually change when completed.

---

# Quick Actions

Quick Actions appear near the top of the Today screen.

Include:

* 🐾 Log Potty Accident
* 📷 Add Journal Entry
* 📖 View History

Buttons should be large enough for one-handed use.

---

# Animations

Animations should be short and purposeful.

Examples:

* Checkbox fills when task is completed.
* Card gently fades into completed state.
* Progress ring animates to new value.
* Leaderboard updates smoothly.
* Confetti appears when daily progress reaches 100%.

Animations should never delay user interaction.

---

# Sounds

The application should support simple sounds for:

* Task reminders
* Successful task completion
* Daily completion celebration

Sounds should be optional.

---

# Empty States

When no data is available, show friendly messages.

Examples:

## History

"No completed tasks yet."

## Growth Journal

"Start documenting Mizu's adventures!"

## Potty Log

"No accidents logged. Great job!"

Empty states should feel encouraging rather than negative.

---

# Responsive Design

The application is designed mobile-first.

### Phone

Primary layout.

Single-column design.

---

### Tablet

Increase spacing.

Allow wider cards.

Maintain single-column scrolling.

---

### Desktop

Support larger screens without changing the interaction model.

The Today screen should remain the primary experience.

---

# Accessibility

The interface should meet WCAG AA guidelines.

Requirements:

* High color contrast
* Large touch targets
* Screen reader support
* Keyboard accessibility where applicable
* Visible focus states
* Icons paired with text
* Color is never the only status indicator

---

# Tone & Personality

The app should feel like a helpful family assistant rather than a business tool.

Use friendly language.

Examples:

Instead of:

"Task Completed"

Use:

"Nice work! Mizu's morning potty is done."

Instead of:

"No Records"

Use:

"Nothing here yet—let's make some memories!"

Keep messages positive, encouraging, and suitable for children without feeling childish.

---

# Design Consistency Rules

To maintain a consistent experience:

* Use the same colors for task states throughout the app.
* Reuse components whenever possible.
* Keep button placement consistent.
* Limit each screen to one primary action.
* Avoid unnecessary pop-ups or confirmation dialogs.
* Prefer bottom sheets over full-screen forms for quick actions.
* Ensure every screen can be comfortably used with one hand on a phone.

A consistent interface is more important than adding visual complexity.


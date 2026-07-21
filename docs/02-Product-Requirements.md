# 02 - Product Requirements

**Project:** Mizu Care
**Version:** 1.0
**Status:** Draft
**Last Updated:** July 2026

---

# Section 1 – Product Overview

## 1. Purpose

Mizu Care is a mobile-first Progressive Web App (PWA) designed to help our family consistently care for our puppy, Mizu.

The app serves as the single source of truth for Mizu's daily care schedule by clearly showing what needs to be done, who is responsible, and whether each task has been completed.

The primary goals are to:

* Keep Mizu's routine consistent.
* Make responsibilities clear for every family member.
* Record who completed each task.
* Encourage participation through a simple points system.
* Track Mizu's growth and development over time.

The application should be easy enough for children to use while providing adults with the tools needed to manage schedules, history, and recurring care.

---

# 2. Primary Users

## Adults

* Bryan
* Carol
* Nely
* Liby

Adults can:

* Complete tasks
* Sign off completed tasks
* Edit incorrect entries
* View analytics
* Manage recurring tasks
* Update settings

---

## Children

* Ash
* Nomi
* Ovi

Children can:

* View today's schedule
* Complete assigned responsibilities
* Sign off completed tasks
* View leaderboards
* View progress

---

## Mizu

Mizu is the dog and the focus of the application.

Mizu is **not** a user account.

---

# 3. Product Goals

The application should:

* Display today's schedule automatically based on the day of the week.
* Make completing a task take less than five seconds.
* Keep everyone informed about what has been completed and what is still outstanding.
* Encourage consistency through a simple point system and leaderboards.
* Store a permanent history of completed responsibilities.
* Track Mizu's growth and important milestones.
* Work well on both phones and tablets.
* Be installable as a Progressive Web App.

---

# 4. Non-Goals

Version 1 will **not** include:

* Multiple pet support
* Medication management
* Veterinary appointment scheduling
* GPS walk tracking
* Native iOS or Android apps
* AI health recommendations

These features may be considered in future releases.

---

# 5. Core Features

The first version of Mizu Care will include:

## Daily Schedule

* Automatic weekday, Saturday, and Sunday schedules
* Friday-only late potty reminder
* Current task indicator
* Next task preview
* Timeline view

---

## Task Completion

* One-tap completion
* Name picker for sign-off
* Automatic timestamp
* Completion history
* Success animation
* Success sound

---

## Leaderboards

Track points for:

* Daily
* Weekly
* Monthly
* All-Time

Standard tasks earn **1 point**.

The following tasks earn **5 points**:

* Bath
* Teeth brushing
* Grooming

---

## Dashboard

The dashboard should display:

* Current task
* Next task
* Daily progress
* Timeline
* Quick actions
* Leaderboard preview

---

## Potty Accident Log

Allow family members to quickly record:

* Pee
* Poop
* Date and time
* Location
* Notes
* Optional photo

The logging workflow should take less than five seconds.

---

## Puppy Growth Journal

Track:

* Weight
* Height (optional)
* Photos
* Vaccinations
* Vet visits
* Milestones
* Notes

Entries should be displayed chronologically.

---

## History

Every completed task should record:

* Task name
* Completed by
* Timestamp
* Points earned
* Optional notes

Adults can edit incorrect entries.

---

## Notifications

The application should:

* Play reminder sounds exactly at the scheduled task time.
* Play a success sound when a task is completed.
* Show browser notifications when permitted.
* Highlight overdue tasks in yellow until completed.

---

## Recurring Care

Automatically remind the family about:

* Nail grinding every 1–2 weeks (default: every 14 days)
* Bathing every 4–6 weeks (default: every 35 days)

These reminders should appear as regular scheduled tasks.

---

# 6. Design Principles

The interface should be:

* Clean
* Modern
* Friendly
* Mobile-first
* Simple enough for children
* Accessible for all family members

Navigation should require as few taps as possible.

Large buttons, readable text, and clear status indicators should be used throughout the application.

---

# 7. Success Criteria

The application will be considered successful when:

* Family members consistently use it to manage Mizu's care.
* Every scheduled task has a clear completion status.
* Sign-offs accurately identify who completed each task.
* Leaderboards update automatically and correctly.
* The schedule remains easy to understand at a glance.
* The app is fast, reliable, and enjoyable to use on mobile devices.
* The growth journal becomes a lasting record of Mizu's life and milestones.

# Section 2 – Application Structure & User Flows

This section defines the primary screens of the application, how users navigate between them, and the expected behavior of each screen.

---

# 1. Navigation

The application is designed primarily for mobile devices.

A fixed bottom navigation bar should be available on every screen.

## Bottom Navigation

| Icon | Screen      | Purpose                                    |
| ---- | ----------- | ------------------------------------------ |
| 🏠   | Dashboard   | View today's schedule and current progress |
| 📅   | Timeline    | View the complete daily schedule           |
| 🏆   | Leaderboard | View family points and rankings            |
| 📖   | History     | View completed tasks and activity logs     |
| ⚙️   | Settings    | Manage preferences and administration      |

The currently selected page should always be highlighted.

---

# 2. Dashboard

The Dashboard is the application's home screen.

It should answer three questions immediately:

* What should I be doing right now?
* What is coming up next?
* How much of today's schedule is complete?

## Dashboard Components

### Current Task Card

Displays:

* Current task
* Scheduled time
* Description
* Responsible family member or group
* Point value
* Countdown until next task
* Large **Complete Task** button (if incomplete)
* Completed badge (if finished)

---

### Next Task Card

Displays:

* Next scheduled task
* Scheduled time
* Description
* Responsible family member or group

---

### Daily Progress

Displays:

* Percentage complete
* Tasks completed
* Tasks remaining

A circular progress indicator should update immediately after every completed task.

---

### Leaderboard Preview

Displays the top three family members for today.

Selecting the card opens the full Leaderboard page.

---

### Quick Actions

Provide one-touch access to:

* Log Potty Accident
* Add Growth Journal Entry
* View Today's Timeline

---

# 3. Timeline

The Timeline displays every task scheduled for the current day.

Tasks should appear in chronological order.

Each task card should display:

* Scheduled time
* Activity name
* Description
* Responsible family member or group
* Point value
* Status indicator
* Completion checkbox

---

## Timeline Status Colors

| Status    | Color  |
| --------- | ------ |
| Upcoming  | Gray   |
| Current   | Blue   |
| Completed | Green  |
| Overdue   | Yellow |

Tasks remain yellow until completed.

---

## Timeline Interactions

Selecting a task opens a detail view containing:

* Full description
* Responsibility
* Completion history
* Notes
* Point value

---

# 4. Task Completion Flow

Completing a task should require as few taps as possible.

## Workflow

1. User taps the checkbox.
2. A bottom sheet appears.
3. User selects their name.
4. Completion is recorded.
5. Timestamp is stored.
6. Points are awarded.
7. Success sound plays.
8. Checkbox animates.
9. Progress updates.
10. Leaderboards refresh.

The process should take less than five seconds.

---

## Sign-Off

The available names are:

Adults

* Bryan
* Carol
* Nely
* Liby

Children

* Ash
* Nomi
* Ovi

Only one person may sign off each task.

---

# 5. Leaderboards

The Leaderboard page contains four tabs.

* Daily
* Weekly
* Monthly
* All-Time

Each tab displays:

* Rank
* Family member
* Total points

The leaderboard should update immediately after task completion.

---

# 6. History

The History page displays all completed activities.

Each record contains:

* Task name
* Date
* Time completed
* Completed by
* Points awarded
* Optional notes

Adults may edit incorrect entries.

Children have read-only access.

---

## Search & Filters

History should support filtering by:

* Date
* Family member
* Task type
* Completed / Missed

---

# 7. Potty Accident Log

The Potty Accident Log is intended for fast entry.

The goal is to allow logging in less than five seconds.

Each record contains:

* Pee
* Poop
* Date
* Time
* Location
* Notes (optional)
* Photo (optional)

Recent entries should appear at the top.

---

# 8. Puppy Growth Journal

The Growth Journal records important milestones.

Each entry may include:

* Weight
* Height (optional)
* Photos
* Milestone
* Vaccination
* Vet visit
* General note

Entries should be displayed chronologically.

---

# 9. Settings

Settings allow users to manage application preferences.

## Preferences

* Light Mode
* Dark Mode
* System Theme

---

## Notifications

* Reminder Sounds
* Success Sounds
* Browser Notifications

---

## Administration (Adults Only)

Adults can:

* Edit incorrect task completions
* Manage recurring reminders
* Update schedule templates
* Reset demo data (if enabled)

---

# 10. Daily User Flow

A typical day should follow this sequence:

1. Open the app.
2. View the Current Task.
3. Complete the responsibility.
4. Sign off using the name picker.
5. Hear the success sound.
6. Watch progress update.
7. Continue with the next scheduled task.

The application should require minimal navigation throughout the day.

---

# 11. Error Handling

If the internet connection is unavailable:

* Previously loaded schedules should remain available.
* Completed tasks should be stored locally.
* Changes should automatically sync once connectivity returns.

If synchronization fails:

* Notify the user.
* Retry automatically.
* Never silently discard completed tasks.

---

# 12. Accessibility

The application should be usable by both adults and children.

Requirements include:

* Large touch targets
* High color contrast
* Readable typography
* Clear status icons
* Screen reader compatibility
* Keyboard accessibility where appropriate
* Color should never be the only indicator of task status

# Section 3 – Schedule Specification & Business Rules

This section defines the scheduling system used by the application.

The schedule is the core of Mizu Care and determines what tasks are shown each day, who is responsible, and how progress is calculated.

Implementation Note: The schedules shown below are presented separately for readability. Internally, the application stores each task with its applicable day(s) (e.g., Mon–Fri, Sat, Sun, Fri only) and dynamically generates the day's schedule.

---

# 1. Schedule Types

The application supports three schedule templates.

## Weekday

Automatically used every:

* Monday
* Tuesday
* Wednesday
* Thursday
* Friday

---

## Saturday

Automatically used every Saturday.

---

## Sunday

Automatically used every Sunday.

The user should never need to manually select a schedule.

---

# 2. Schedule Behavior

At midnight each day, the application should:

* Determine the current day of the week.
* Load the appropriate schedule.
* Reset daily progress.
* Preserve all historical completion records.
* Calculate recurring reminders due that day.

---

# 3. Task Structure

Every scheduled task contains the following information.

| Field          | Description                              |
| -------------- | ---------------------------------------- |
| Time           | Scheduled start time                     |
| Activity       | Short task name                          |
| Description    | Detailed instructions                    |
| Responsibility | Person or group responsible              |
| Point Value    | 1 or 5 points                            |
| Status         | Upcoming, Current, Completed, or Overdue |

---

# 4. Task Status

Each task may exist in one of four states.

## Upcoming

The scheduled time has not yet arrived.

Color: Gray

---

## Current

The task is currently due.

Color: Blue

The Current Task card should always display this task.

---

## Completed

The task has been signed off.

Color: Green

Completed tasks display:

* Completed by
* Completion time

---

## Overdue

The scheduled time has passed and the task has not been completed.

Color: Yellow

Tasks remain yellow until completed.

Tasks are never automatically marked as missed.

---

# 5. Point Values

Most tasks award:

**1 Point**

The following activities award:

**5 Points**

* Bath
* Teeth Brushing
* Grooming

Points are awarded to the person who signs off the task.

---

# 6. Sign-Off Rules

A task is completed by:

1. Tapping the checkbox.
2. Selecting a family member.
3. Confirming completion.

The application records:

* User
* Timestamp
* Points earned

Only one family member may sign off each task.

---

# 7. Weekday Schedule

| Time     | Activity                                         | Responsibility    | Points |
| -------- | ------------------------------------------------ | ----------------- | ------ |
| 6:00 AM  | Wake / Potty                                     | Adult             | 1      |
| 6:10 AM  | Breakfast                                        | Adult             | 1      |
| 6:30 AM  | Last Call / Potty                                | Adult             | 1      |
| 6:40 AM  | Crate / Nap                                      | Adult             | 1      |
| 8:30 AM  | Leg Stretch / Potty                              | Adult             | 1      |
| 9:15 AM  | Morning Nap                                      | Mizu (Solo)       | 1      |
| 12:00 PM | Lunch / Play / Potty                             | Adult             | 1      |
| 1:00 PM  | Afternoon Nap                                    | Mizu (Solo)       | 1      |
| 2:00 PM  | Welcome Home / Potty                             | Kids              | 1      |
| 3:00 PM  | Chill Time                                       | Kids (Supervised) | 1      |
| 5:00 PM  | Evening Walk                                     | Kids              | 1      |
| 6:00 PM  | Dinner / Potty                                   | Kids              | 1      |
| 7:00 PM  | Family Time (includes grooming & teeth brushing) | Whole Family      | 5      |
| 8:30 PM  | Water Cut-off                                    | Adult             | 1      |
| 9:30 PM  | Bedtime / Potty                                  | Adult             | 1      |

---

## Friday Special Rule

Every Friday an additional task is automatically added.

| Time     | Activity   | Responsibility | Points |
| -------- | ---------- | -------------- | ------ |
| 10:30 PM | Late Potty | Adult          | 1      |

This task should only appear on Fridays.

---

# 8. Saturday Schedule

| Time     | Activity              | Responsibility | Points |
| -------- | --------------------- | -------------- | ------ |
| 6:45 AM  | Morning Start / Potty | Adult          | 1      |
| 7:15 AM  | Breakfast / Potty     | Whole Family   | 1      |
| 8:00 AM  | Morning Play          | Adult          | 1      |
| 9:30 AM  | Morning Nap           | Mizu (Solo)    | 1      |
| 12:00 PM | Lunch / Potty         | Nomi or Ovi    | 1      |
| 12:30 PM | Free Roam             | Adult          | 1      |
| 4:00 PM  | Sniff Walk / Potty    | Nomi           | 1      |
| 6:00 PM  | Dinner / Potty        | Kids           | 1      |
| 9:00 PM  | Night Routine         | Whole Family   | 1      |
| 10:30 PM | Final Potty           | Adult          | 1      |

---

# 9. Sunday Schedule

| Time     | Activity                              | Responsibility | Points |
| -------- | ------------------------------------- | -------------- | ------ |
| 6:45 AM  | Weekend Start / Potty                 | Kids           | 1      |
| 9:00 AM  | Mid-Morning / Potty                   | Adult          | 1      |
| 12:00 PM | Sunday Lunch / Potty                  | Adult          | 1      |
| 1:00 PM  | Nap Time                              | Mizu (Solo)    | 1      |
| 2:00 PM  | Reunion Play / Potty + Undercoat Rake | Whole Family   | 5      |
| 4:30 PM  | Family Walk                           | Whole Family   | 1      |
| 6:00 PM  | Dinner / Potty                        | Kids           | 1      |
| 9:30 PM  | Bedtime / Potty                       | Adult          | 1      |

---

# 10. Recurring Care Tasks

The application automatically manages recurring care reminders.

## Nail Grinding

Frequency:

Every 14 days (default)

Point Value:

5

---

## Bath

Frequency:

Every 35 days (default)

Point Value:

5

Recurring tasks appear at the top of the Today's page under a **"Due Soon"** section until completed.

After completion, the next due date is automatically calculated.

---

# 11. Daily Progress

Daily Progress is calculated as:

Completed Scheduled Tasks ÷ Total Scheduled Tasks

Recurring tasks due that day are included in the calculation.

Progress updates immediately after every completed task.

---

# 12. Completion Rules

A task can only be completed once.

A completed task may only be edited by an adult user.

Deleting a completion should require confirmation.

Every edit should be recorded in the activity history.

---

# 13. Business Rules Summary

* The schedule changes automatically based on the day of the week.
* Friday includes an additional late-night potty task.
* Overdue tasks remain yellow until completed.
* Tasks never expire automatically.
* One sign-off completes one task.
* Points are awarded immediately upon completion.
* Daily progress updates in real time.
* Recurring reminders automatically regenerate after completion.
* Historical records are never deleted automatically.

# Section 4 – Features & Functional Requirements

This section defines the functional behavior of the application's primary features.

---

# 1. Today's Screen

The Today screen is the primary screen of the application.

Users should be able to complete nearly every daily interaction without leaving this screen.

The Today screen should include:

1. Current Task
2. Next Task
3. Daily Progress
4. Quick Actions
5. Today's Schedule
6. Leaderboard Preview

---

## Current Task Card

The Current Task Card should always display the task that is currently due.

Display:

* Activity
* Scheduled Time
* Description
* Responsible Person/Group
* Point Value
* Status
* Complete Task button

If the task has already been completed, display:

* Completed by
* Completion time
* Green completed indicator

---

## Next Task Card

Display the next scheduled task.

Include:

* Time
* Activity
* Responsibility
* Description

---

## Daily Progress

Display:

* Percentage complete
* Tasks completed
* Tasks remaining

Progress updates immediately after every completed task.

If every scheduled task has been completed:

* Progress reaches 100%
* Play celebration sound
* Display confetti animation
* Display "Great job! Mizu's care is complete for today."

---

# 2. Today's Schedule

Display every task for the current day.

Each task card should contain:

* Time
* Activity
* Description
* Responsibility
* Point value
* Status
* Completion checkbox

Tasks should always remain sorted chronologically.

---

## Task Interaction

Selecting a task opens a detail sheet showing:

* Full description
* Completion status
* Completed by
* Completion time
* Notes (if any)

---

# 3. Task Completion

Task completion should require as few interactions as possible.

Workflow:

1. Tap checkbox
2. Name picker appears
3. Select family member
4. Save completion

The application automatically:

* Stores timestamp
* Awards points
* Updates progress
* Updates leaderboard
* Updates history
* Plays success sound
* Animates completion

---

## Duplicate Prevention

A completed task cannot be completed again.

Adults may edit incorrect completions.

---

# 4. Leaderboards

Leaderboards encourage participation.

Tabs:

* Daily
* Weekly
* Monthly
* All-Time

Each leaderboard displays:

* Rank
* Name
* Total Points

Top three users should be visually highlighted.

Leaderboard updates immediately after every completed task.

---

# 5. History

History contains every completed task.

Each entry stores:

* Activity
* Date
* Time
* Completed by
* Points
* Notes (optional)

Adults may edit history.

Children have read-only access.

---

## History Filters

Users may filter history by:

* Date
* Family member
* Activity
* Completed / Missed

Search should return results instantly.

---

# 6. Potty Accident Log

The Potty Accident Log provides quick recording of accidents.

The log should be accessible from:

* Quick Actions
* History
* Floating Action Button (optional)

---

## Record Fields

Required:

* Pee or Poop
* Time
* Location

Optional:

* Notes
* Photo

The current date and time should be selected automatically.

The entire logging process should take less than five seconds.

---

## Potty History

Display:

* Most recent first
* Type
* Time
* Location
* Notes
* Photo indicator

---

## Future Analytics

Potty records should support future reporting such as:

* Daily accident count
* Weekly trends
* Time-of-day patterns
* Accident-free streaks

---

# 7. Puppy Growth Journal

The Growth Journal stores important memories and health information.

Users may create entries at any time.

---

## Entry Types

* Weight
* Height
* Photo
* Milestone
* Vaccination
* Vet Visit
* General Note

Each entry stores:

* Date
* Title
* Description
* Optional photo

---

## Timeline

Display entries in chronological order.

Support filtering by entry type.

---

## Milestone Examples

* First walk
* First bath
* First grooming
* Lost first tooth
* First camping trip
* Birthday

---

# 8. Notifications

Notifications remind the family when tasks become due.

When a scheduled task begins:

* Play reminder sound
* Display browser notification (if enabled)

Notifications occur exactly at the scheduled task time.

---

## Completion Notifications

After completing a task:

* Play success sound
* Display completion animation

---

# 9. Quick Actions

Quick Actions appear on the Today screen.

Buttons:

* Log Potty Accident
* Add Growth Entry
* View History

Future Quick Actions may be added without redesigning the page.

---

# 10. Settings

Users can customize the application.

Preferences include:

Theme

* Light
* Dark
* System

Sounds

* Reminder sound
* Success sound

Notifications

* Browser notifications
* Reminder sounds

---

## Adult Settings

Adults may additionally:

* Edit completed tasks
* Manage recurring reminders
* Reset demo data
* Configure future recurring care tasks

---

# 11. Offline Behavior

If internet access is unavailable:

Users should still be able to:

* View today's schedule
* Complete tasks
* Record potty accidents
* Add journal entries

Changes should be queued locally.

Once internet connectivity returns:

* Automatically synchronize pending changes
* Preserve completion timestamps
* Prevent duplicate records

---

# 12. Error Handling

The application should provide friendly error messages.

Examples:

Unable to connect

Task already completed

Unable to synchronize

Photo upload failed

Errors should explain what happened and how to resolve the issue.

---

# 13. Accessibility

The application should follow WCAG AA accessibility guidelines.

Requirements:

* Large touch targets
* High contrast
* Screen reader labels
* Keyboard accessibility where applicable
* Icons accompanied by text
* Color is never the only status indicator

---

# 14. Performance Requirements

The application should feel responsive on modern mobile devices.

Goals:

* Initial load under 2 seconds
* Task completion under 1 second
* Smooth scrolling
* Responsive animations
* No visible layout shift
* Immediate UI updates after task completion

# Section 5 – Data & Business Logic

This section defines how the application behaves behind the scenes and the business rules that govern task completion, points, schedules, reminders, and permissions.

---

# 1. Family Members

The application supports a fixed list of family members.

## Adults

* Bryan
* Carol
* Nely
* Liby

Adults have permission to:

* Complete tasks
* Edit completed tasks
* Edit history
* Manage recurring reminders
* Update application settings

---

## Children

* Ash
* Nomi
* Ovi

Children can:

* View today's schedule
* Complete tasks
* View history
* View leaderboards

Children cannot modify completed records or application settings.

---

# 2. Task Lifecycle

Every scheduled task moves through the following lifecycle:

Upcoming → Current → Completed

or

Upcoming → Current → Overdue → Completed

Tasks are never automatically marked as missed or removed from the schedule.

---

# 3. Task Completion Rules

A task is considered complete when:

* The completion checkbox is selected.
* A family member signs off.
* The completion is successfully saved.

The application records:

* Task
* Family member
* Date
* Time
* Points earned

Each task can only be completed once.

If a mistake is made, an adult must edit the record.

---

# 4. Point System

The point system is intended to encourage participation and consistency.

## Standard Tasks

Most scheduled activities are worth:

**1 Point**

---

## Bonus Tasks

The following activities are worth:

**5 Points**

* Bath
* Grooming
* Teeth Brushing

Additional bonus tasks may be added in future updates.

---

## Point Rules

Points are awarded:

* Immediately after task completion
* To the person who signs off the task

Points are never shared between multiple users.

---

# 5. Leaderboard Logic

Leaderboards are calculated from completed tasks.

Views include:

* Daily
* Weekly
* Monthly
* All-Time

Each leaderboard displays:

* Rank
* Name
* Total Points

Leaderboard rankings should update immediately after task completion.

If two users have the same score, they share the same rank and are sorted alphabetically.

---

# 6. Schedule Generation

The application automatically determines which schedule to display based on the current day.

Weekday schedule:

* Monday
* Tuesday
* Wednesday
* Thursday
* Friday

Weekend schedules:

* Saturday
* Sunday

Users should never manually choose a schedule.

---

## Friday Rule

Every Friday, an additional late-night potty task is automatically added.

No other day includes this task.

---

# 7. Recurring Care

Recurring care reminders are automatically managed by the application.

Default reminders include:

| Activity      | Frequency     |
| ------------- | ------------- |
| Nail Grinding | Every 14 Days |
| Bath          | Every 35 Days |

When a recurring task is completed:

* The completion date is recorded.
* The next due date is automatically calculated.

Recurring reminders appear on the Today screen when due.

---

# 8. Progress Calculation

Daily Progress is calculated using scheduled tasks due for that day.

Formula:

Completed Tasks ÷ Total Scheduled Tasks

Recurring tasks due that day are included.

Progress updates immediately after each completed task.

When all scheduled tasks have been completed:

* Progress reaches 100%
* Celebration animation plays
* Completion message is displayed

---

# 9. Notifications

Reminder notifications occur exactly at the scheduled task time.

If notifications are enabled:

* Browser notification appears
* Reminder sound plays

Task reminders are sent once per scheduled task.

The application should not repeatedly notify users for overdue tasks in Version 1.

---

# 10. History

Every completed task is permanently recorded.

History includes:

* Task
* Date
* Time
* Completed by
* Points
* Notes (optional)

History is never automatically deleted.

If a task completion is edited, the updated information should be reflected in History.

---

# 11. Potty Accident Records

Each accident record contains:

Required:

* Type (Pee or Poop)
* Date
* Time
* Location

Optional:

* Notes
* Photo

Accident records do not affect points or leaderboard rankings.

---

# 12. Growth Journal Records

Growth Journal entries may include:

* Weight
* Height
* Milestone
* Vet Visit
* Vaccination
* General Note
* Photo

Journal entries are informational only and do not affect scores or progress.

---

# 13. Editing Rules

Only adults may edit:

* Completed tasks
* History entries
* Recurring reminder dates

When a task completion is edited:

* Leaderboard totals should automatically recalculate.
* Daily progress should update if applicable.

---

# 14. Offline Behavior

When offline, users can:

* View today's schedule
* Complete tasks
* Record potty accidents
* Add journal entries

Offline changes should be stored locally.

When the connection returns:

* Pending changes automatically synchronize.
* Existing records are updated without creating duplicates.

---

# 15. Error Handling

The application should gracefully handle common errors.

Examples include:

* Network unavailable
* Synchronization failed
* Task already completed
* Invalid sign-off
* Failed photo upload

Users should receive clear, friendly messages explaining the issue.

---

# 16. Future Expansion

The application should be designed to support future features without major changes.

Possible future enhancements include:

* Multiple pets
* Custom schedules
* Rewards and achievements
* Push notifications
* Calendar integration
* Vet appointment tracking
* Medication reminders
* Wearable device integration
* AI-powered care recommendations

These features are outside the scope of Version 1 but should be considered during application design.

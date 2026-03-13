---
layout: single
title: New Feature: Smart Scheduling
permalink: /S-Docs/new-feature/
---

# Smart Scheduling

AcmeTasker now includes a Smart Scheduling feature that automatically suggests optimal times for tasks based on your calendar and priorities. This document describes the feature in detail, including configuration, usage examples, and troubleshooting tips.

## Overview
Smart Scheduling analyzes existing tasks, user availability, and external calendar integrations (Google Calendar, Outlook) to recommend due dates and times. It helps teams avoid conflicts and balance workloads.

## Configuration
To enable Smart Scheduling, go to Settings > Features and toggle  Enable Smart Scheduling. Administrators can configure lookahead windows and maximum daily hours per user.

### Calendar Integration
Link your calendar via the Integrations page. The system supports OAuth for major providers. Once linked, calendar events will block suggested times.

## Using Smart Scheduling
When creating or editing a task, click the Suggest button next to the due date field. Choose a recommended slot or manually pick a time. Suggestions appear in a dropdown with confidence scores.

## Examples
1. Create a task Prepare report and click Suggest; the system may recommend next Monday at 10 AM, avoiding existing meetings.
2. Edit a high-priority task and request a slot; the algorithm may recommend working hours tomorrow.

## User Interface
Smart Scheduling appears as a sidebar panel with time slots, color-coded by availability (green = good, yellow = tentative, red = conflict). Use keyboard arrow keys to navigate suggestions.

## API Support
A new endpoint POST /tasks/{id}/suggest returns JSON suggestions:
`json
{
  suggestions: [
    {dueDate:2026-03-10T10:00:00Z,score:0.95},
    {dueDate:2026-03-11T14:00:00Z,score:0.87}
  ]
}
`

## Troubleshooting
- **No suggestions shown:** Ensure calendar is linked and user has at least one available hour in the next 7 days.
- **Incorrect suggestions:** Verify timezone settings; suggestions use the user's profile timezone.

## Rollout Notes
Smart Scheduling will be rolled out gradually. Users can opt-in via their profile, and version 1.2.1 includes performance improvements.

## Future Enhancements
Plans include machine learning models that learn individual work patterns and support for team-wide scheduling.


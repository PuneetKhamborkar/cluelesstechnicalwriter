---
layout: single
title: AcmeTasker Release Notes
permalink: /S-Docs/release-notes/
toc: true
sidebar: nav
---

# Release Notes

## On this page

- [Version 1.2.0 (2025-12-01)](#version-120-2025-12-01)
- [Version 1.1.5 (2025-08-15)](#version-115-2025-08-15)
- [Version 1.1.0 (2025-04-10)](#version-110-2025-04-10)
- [Version 1.0.0 (2024-10-01)](#version-100-2024-10-01)
- [How to read these notes](#how-to-read-these-notes)
- [Upgrade instructions](#upgrade-instructions)
- [Known Issues](#known-issues)

## Version 1.2.0 (2025-12-01)
- Added new REST endpoint for managing tags.
- Improved performance on task listing by paginating database queries.
- Fixed issue with SOAP CreateTask returning incorrect IDs.
- Enhanced Smart Scheduling to consider user calendar availability.

## Version 1.1.5 (2025-08-15)
- Security patch: fixed XSS vulnerability in comment rendering.
- Updated dependencies to address CVE-2025-1234.
- Added ability to export tasks as CSV.

## Version 1.1.0 (2025-04-10)
- Initial public release with core task management features.
- Features include task creation, assignment, due dates, and notifications.
- Included mobile apps for iOS and Android with offline sync.

## Version 1.0.0 (2024-10-01)
- Beta launch for early adopters; basic task tracking and project grouping.


### How to read these notes
Each release entry includes major enhancements, bug fixes, and security updates. For detailed changelogs, refer to the GitHub repository tags.

### Upgrade instructions
To upgrade, back up your database, update the application files, and run <code>npm run migrate</code>. Review the migration log for any required manual steps.

### Known Issues
- Users may experience slow loading when more than 10,000 tasks are present; a fix is planned for v1.3.0.


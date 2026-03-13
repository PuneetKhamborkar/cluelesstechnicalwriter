---
layout: single
title: Troubleshooting Guide
permalink: /S-Docs/AcmeTasker/troubleshooting/
---

# Troubleshooting

This guide helps you resolve common problems encountered while using or installing AcmeTasker.

## Application Won't Start
- **Cause:** Node.js missing or incorrect version.
  **Solution:** Install Node.js 14+ and restart the application.
- **Cause:** Configuration file syntax error.
  **Solution:** Validate config.json with an online JSON validator.

## Cannot Log In
- **Cause:** Incorrect password.
  **Solution:** Use  Forgot password link to reset.
- **Cause:** Account not activated.
  **Solution:** Check your email for an activation link or contact admin.

## API Returns 401 Unauthorized
- **Cause:** Missing or invalid API key.
  **Solution:** Verify the Authorization header: Bearer YOUR_API_KEY.
- **Cause:** API key expired or revoked.
  **Solution:** Generate a new key from the user profile page.

## Tasks Not Syncing
- **Cause:** Network connectivity issues.
  **Solution:** Check internet connection and server status at status.acmetasker.com.
- **Cause:** Browser caching problem.
  **Solution:** Clear browser cache and reload the page.

## Installation Errors
- **Permission denied (Linux/Windows)**: Run with sudo or as administrator.
- **Database connection failed**: Verify credentials in config.json and ensure the database server is running.

## Performance Issues
- **Slow page loads with many tasks**: Enable pagination or archive completed tasks.
- **High CPU usage**: Check for long-running queries or memory leaks in logs.

## Mobile App Issues
- **App crashes on launch**: Update to the latest version and ensure the device OS is supported.
- **Offline sync not working**: Make sure the app has storage permissions and network access.

## Email Notifications Not Sent
- **Cause:** SMTP misconfiguration.
  **Solution:** Verify SMTP host, port, and credentials in config.
- **Cause:** Emails marked as spam.
  **Solution:** Add the sending domain to your spam whitelist.

## Contacting Support
If problems persist after following the above steps, email support@acmetasker.com with:
1. A description of the issue
2. Steps to reproduce
3. Relevant log excerpts or screenshots
4. Your configuration file (with sensitive values redacted)


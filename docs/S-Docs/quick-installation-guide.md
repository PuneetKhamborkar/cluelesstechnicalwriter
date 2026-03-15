---
layout: single
title: Quick Installation Guide
permalink: /S-Docs/quick-install/
---

# Installation

## On this page

- [End User (Desktop)](#end-user-desktop)
- [End User (Mobile)](#end-user-mobile)
- [Server Installation (Linux)](#server-installation-linux)
- [Server Installation (Docker)](#server-installation-docker)
- [Post-installation](#post-installation)
- [Troubleshooting Installation](#troubleshooting-installation)

This quick guide covers installing AcmeTasker for both end users and server administrators.

## End User (Desktop)
1. Visit https://app.acmetasker.com and sign up for an account.
2. Download the desktop app (Windows/Mac) from the download page.
3. Run the installer and follow the prompts.
4. Launch the app and log in with your credentials.

## End User (Mobile)
1. Open the App Store (iOS) or Google Play (Android).
2. Search for  AcmeTasker and install the app.
3. Open the app and sign in or create an account.

## Server Installation (Linux)
1. Ensure you have Node.js 14+ and a supported database installed.
2. Clone the repository: git clone https://github.com/acme/acmetasker.git.
3. Navigate to the project directory and run npm install.
4. Copy config.example.json to config.json and update settings.
5. Run database migrations: npm run migrate.
6. Start the server: npm start or use a process manager like PM2.

## Server Installation (Docker)
1. Pull the latest image: docker pull acmetasker/app:latest.
2. Create a docker-compose.yml with database and app services.
3. Set environment variables in the compose file (PORT, DATABASE_URL, etc.).
4. Run docker-compose up -d.

## Post-installation
- Access the admin console at /admin to create initial users and configure settings.
- Configure a reverse proxy (Nginx/Apache) for SSL termination.

## Troubleshooting Installation
- **Permission denied**: ensure you run installers as administrator or root.
- **Database connection failed**: verify the host, port, user, and password in config.json.

For detailed instructions, consult the full installation manual available on the documentation portal.


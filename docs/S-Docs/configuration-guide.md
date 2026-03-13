---
layout: single
title: AcmeTasker Configuration Guide
permalink: /S-Docs/configuration-guide/
---

# AcmeTasker Configuration Guide

This guide explains how to configure AcmeTasker for production and development environments. It covers file-based settings, environment variables, and advanced options used by administrators and deployers.

## Prerequisites

Before configuring, ensure Node.js (v14+) and a supported database (MySQL or PostgreSQL) are installed. Docker images are available for containerized deployments.

## Configuration File Structure

The main configuration file config.json contains sections for database, email, authentication, and logging.

### Sample config.json

`json
{
   database: {
    host: localhost,
    port: 3306,
    user: acme_user,
    password: secret
  },
  email: {
    smtpHost: smtp.example.com,
    smtpPort: 587
  }
}
`

## Database Setup

Create the database schema using the provided schema.sql script or run 
pm run migrate. Connection pooling settings can be adjusted in db.pool.

## Email and Notifications

Configure SMTP settings for sending notifications. Optionally integrate with SendGrid or Mailgun via API keys. TLS and authentication options are configurable.

## Environment Variables

Useful environment variables include NODE_ENV, PORT, and ADMIN_EMAIL. For Docker, set these in the container environment or compose file.

## Advanced Configuration

Adjust rate limits, caching, and third-party service integrations in advanced.json or via the admin panel. Examples include Redis cache settings and OAuth client credentials.

## Logging Configuration

Specify log levels and output destinations (console, file, syslog) in the logging section. Use JSON format for compatibility with log aggregation tools.

## Load Balancing & Clustering

For high availability, deploy multiple application instances behind a load balancer. Use a shared Redis instance for session storage and sticky sessions if required.

## Security Settings

Enable HTTPS, configure the sessionSecret, and set password complexity rules. Disable local signup if using SSO providers such as OAuth2 or SAML.

## Backup Settings

Configure automated backups by specifying database dump commands and retention policies. Backups can be stored on S3 or network storage.

## Example Profiles

Different profiles (development, staging, production) can be maintained in config.dev.json and config.prod.json. The application selects a profile based on NODE_ENV.

## Troubleshooting Configuration

If the application fails to start, check log files under /logs and verify that the configuration file is valid JSON. Common issues include missing fields and incorrect credentials.

## Contact Support

For assistance with configuration, contact support@acmetasker.com with your config file attached. Provide error logs and environment details for faster resolution.


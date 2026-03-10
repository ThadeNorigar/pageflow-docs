---
layout: default
title: Security Policy — PageFlow
---

# Security Policy — PageFlow

**Last updated:** March 10, 2026

## Architecture

PageFlow is built on Atlassian Forge, a serverless sandboxed runtime. All data processing occurs within the Forge environment — no customer data is stored on external servers.

## Data Handling

- Microsoft OneNote data is accessed via OAuth 2.0 through Forge built-in provider mechanism and processed in real-time only during import
- No customer data is persisted outside the Atlassian Forge environment
- All API communication is encrypted via TLS 1.2+

## Access Control

- The app follows the principle of least privilege with minimal Confluence and Microsoft Graph API scopes
- OAuth 2.0 tokens are managed and encrypted by the Forge platform

## Input Validation

- User inputs are validated against allowlist regex patterns
- HTML content is sanitized with tag and attribute allowlisting before conversion to Confluence Storage Format
- Uploaded filenames are sanitized to prevent path traversal

## Dependency Management

- Dependencies are monitored via npm audit and kept up to date
- Static analysis is performed using ESLint with @typescript-eslint rules

## Vulnerability Reporting

Security issues can be reported to [pageflow@adrianphilipp.de](mailto:pageflow@adrianphilipp.de). We will acknowledge receipt within 48 hours and address confirmed vulnerabilities within the timeframes defined by Atlassian's [Marketplace security bug fix policy](https://developer.atlassian.com/platform/marketplace/security-bugfix-policy/).

## Incident Response

In case of a security incident, we will notify affected customers and Atlassian following the [Marketplace incident communication guidelines](https://developer.atlassian.com/platform/marketplace/app-security-incident-management-guidelines/).

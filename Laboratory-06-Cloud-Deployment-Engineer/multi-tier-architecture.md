# Multi-Tier Architecture

## What Is a Two-Tier Architecture?
A two-tier architecture separates an application into a web/application tier and a database tier.

## The Web/Application Tier
Nextcloud provides the user interface and handles HTTP requests for the private cloud storage system.

## The Database Tier
MariaDB stores persistent application information, including user accounts and file metadata.

## Why Separate Them?
Separate containers make services easier to manage, update, and troubleshoot. Proper networking and access controls are still necessary to protect the system.

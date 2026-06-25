# Storage Platform

## Overview

Storage Platform is a multi-cloud file management service built using FastAPI.

The platform provides a single API layer that can work with multiple storage providers without changing application code.

Supported providers:

* AWS S3
* Azure Blob Storage
* MinIO
* Google Cloud Storage

## Problem Statement

Applications often become tightly coupled to a specific cloud storage provider.

Migrating between providers requires code changes and increases maintenance complexity.

## Solution

A provider abstraction layer was implemented using the Strategy Pattern.

Applications interact with a common storage interface while provider-specific logic is handled internally.

## Features

### File Upload

* Upload files to cloud storage

### File Download

* Download stored files

### File Delete

* Remove files from storage

### File Listing

* List uploaded files

### Signed URLs

* Generate temporary download links

### Metadata Management

* Store file metadata in PostgreSQL

### Provider Switching

* Change storage provider through configuration only

## Architecture

Client
|
FastAPI API
|
Storage Service
|
-

|      |      |         |
S3   Azure   GCP     MinIO

## Tech Stack

### Backend

* Python
* FastAPI

### Database

* PostgreSQL

### Cache

* Redis

### Cloud Storage

* AWS S3
* Azure Blob
* MinIO
* GCP Storage

### DevOps

* Docker
* Docker Compose

## Future Enhancements

* File Versioning
* Virus Scanning
* Image Compression
* Multi-Part Uploads
* Audit Logs
* User Authentication

## Author

Saroni

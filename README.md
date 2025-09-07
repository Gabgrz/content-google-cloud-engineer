# Google Cloud Engineer Course Project

A comprehensive microservices application demonstrating Google Cloud Platform services, originally from the Linux Academy GCP Cloud Engineer course. This fork resolves deprecated Go versions and provides a modern, deployable example.

## Architecture

The application consists of four main services:

- **Frontend** (App Engine) - Web interface for uploading product images with user authentication
- **Products Service** (Kubernetes Engine) - Manages product data using BigQuery and Cloud Storage
- **Ads Service** (Compute Engine) - Serves advertisements from Cloud Spanner database
- **Image Parser** (Cloud Functions) - Processes uploaded images using Vision API and stores metadata in Bigtable

## Services Used

- **App Engine** - Frontend web application
- **Kubernetes Engine** - Products microservice
- **Compute Engine** - Ads microservice with auto-scaling
- **Cloud Functions** - Image processing pipeline
- **Cloud Storage** - File storage (public/private buckets)
- **Cloud Spanner** - Ads database
- **BigQuery** - Product analytics
- **Bigtable** - Image metadata storage
- **Cloud Vision API** - Image analysis
- **Pub/Sub** - Event messaging
- **Cloud Load Balancing** - Traffic distribution

## Quick Start

1. Set up your GCP project and update `common/project_settings.sh`
2. Run the deployment script:
   ```bash
   ./create.sh
   ```
3. Configure environment variables for the frontend as prompted

## Project Structure

- `frontend/` - App Engine web application
- `products/` - Kubernetes-based product service
- `ads/` - Compute Engine ads service
- `image_parser/` - Cloud Function for image processing
- `common/` - Shared configuration and setup scripts

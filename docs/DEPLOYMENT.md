# Deployment & CI/CD Infrastructure

## Important Note

**This repository currently contains a static exported build of Amalgam Creator OS.** 

Full Vite/React/TypeScript CI requires the source project containing `package.json`. Until that source tree is restored or moved into this repository, CI/CD is configured for static artifact validation and deployment only.

## Overview

The current infrastructure supports automated validation of the static build and deployment to Vercel.

## CI/CD Pipeline

### GitHub Actions: `static-ci.yml`

This workflow runs on every push and pull request to `main`.

1. **Verification**: Checks for the existence of `index.html` and the `assets/` directory.
2. **Artifact Upload**: Uploads the static site content as a build artifact.
3. **Deployment**: On pushes to `main`, the static site is automatically deployed to Vercel.

## Setup Instructions

### Vercel Deployment Secrets

To enable automated deployment, the following GitHub Secrets must be configured in the repository:

- `VERCEL_TOKEN`: Your Vercel Personal Access Token.
- `VERCEL_ORG_ID`: Your Vercel Organization ID.
- `VERCEL_PROJECT_ID`: Your Vercel Project ID.

## Maintenance

**Maintained by:** Sierra Warren Developments, LLC  
**Last Updated:** 2026-06-06

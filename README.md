# SPDC NodeJS

A SharePoint Data Connector (SPDC) for synchronizing SharePoint document libraries to Azure Blob Storage and local storage, written in Node.js/TypeScript.

## Features
- Syncs SharePoint files and folders to Azure Blob Storage
- Supports delta and full sync
- Handles metadata and permissions
- Modular, extensible architecture

## Project Structure
```
/ (root)
├── auth/                # Authentication and Key Vault logic
├── changeDetection/     # Change detection logic
├── common/              # Shared DTOs and enums
├── config/              # Configuration management
├── core/                # Core utilities (logging, blob, etc.)
├── dataExtraction/      # SharePoint data extraction
├── dataProcessing/      # Metadata and permission processing
├── graphApi/            # Microsoft Graph API client
├── scripts/             # Utility scripts
├── staging/             # Output staging logic
├── state/               # State repository (delta tokens, item state)
├── sync/                # Sync manager and logic
├── certs/               # Certificates for authentication
├── app.ts               # Main entry point
├── package.json         # NPM dependencies
├── tsconfig.json        # TypeScript config
```

## Setup
1. Install dependencies:
   ```bash
   npm install
   ```
2. Configure environment variables in a `.env` file (see CONFIGURATION.md for details).
3. Place your certificate files in the `certs/` directory.

## Running
- Build TypeScript:
  ```bash
  npx tsc
  ```
- Run the app:
  ```bash
  node dist/app.js
  ```
- For development (using ts-node):
  ```bash
  npm run dev
  ```

## Configuration
See `CONFIGURATION.md` for all environment variables and options.

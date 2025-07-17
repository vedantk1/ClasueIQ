# ClauseIQ Utility Scripts

This directory contains utility scripts for ClauseIQ development and maintenance.

## Scripts

### Development Scripts
- **setup-for-development.sh** - 🚀 **MAIN SETUP SCRIPT** - Automated development environment setup
- **dependency-audit.sh** - Checks for outdated and vulnerable dependencies in both backend and frontend
- **setup_shared_types.sh** - Sets up the shared types package for development
- **sync_types.py** - Synchronizes TypeScript and Python type definitions
- **generate_ts_types.py** - Generates TypeScript types from Python Pydantic models
- **verify_shared_types.py** - Verifies that shared types are in sync between frontend and backend

### System Maintenance Scripts
Database maintenance scripts are located in the `backend/` directory:
- `backend/check_all_users.py` - Analyzes all users in the system
- `backend/check_pinecone_docs.py` - Checks Pinecone vector database document storage
- `backend/clear_database.py` - Clears all documents, chat sessions, and vector data

## Usage

### Development Scripts
```bash
# 🚀 Complete development setup (recommended)
./scripts/setup-for-development.sh

# Individual scripts
./scripts/dependency-audit.sh  # Check dependencies
./scripts/setup_shared_types.sh  # Set up shared types
python3 scripts/sync_types.py  # Sync types
python3 scripts/verify_shared_types.py  # Verify types
```

### Database Scripts
```bash
# From project root, with backend virtual environment
cd backend && source venv/bin/activate
python3 check_all_users.py
python3 check_pinecone_docs.py
python3 clear_database.py
``` 
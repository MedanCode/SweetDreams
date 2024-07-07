# Sweet Dreams Confectionaries API

Welcome to the Sweet Dreams Confectionaries API. This API provides endpoints for user authentication, interactions with the AI, and more.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Documentation](API_DOCS.md)
- [Contributing](CONTRIBUTING.md)

## Installation

Please refer to the [installation guide](INSTALLATION.md) for detailed instructions.

## Usage

1. **Start the server**:
   ```bash
   uvicorn app:app --host 0.0.0.0 --port 8000 --reload
   ```

2. **Access the API documentation**:
   Visit `http://localhost:8000/docs` for interactive API documentation.

3. **Example curl command**:
   ```bash
   curl -X POST "http://localhost:8000/chat" -H "Authorization: Bearer YOUR_ACCESS_TOKEN" -H "Content-Type: application/json" -d '{"message": "Hello, AI!"}'
   ```

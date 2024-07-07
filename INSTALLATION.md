# Installation Guide

## Prerequisites

- Python 3.12
- Virtual Environment

## Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/your-repo/sweet-dreams.git
   cd sweet-dreams
   ```

2. **Create a virtual environment**:
   ```bash
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Setup environment variables**:
   Create a `.env` file in the project root directory and add the following:
   ```env
   DEBUG=True
   OPENAI_API_KEY=your_openai_api_key
   SECRET_KEY=your_secret_key_here
   DATABASE_URL=sqlite+aiosqlite:///sweet_dreams.db
   ACCESS_TOKEN_EXPIRE_MINUTES=30
   HOST=0.0.0.0
   PORT=8000
   LOG_LEVEL=INFO
   ```

5. **Initialize the database**:
   ```bash
   python init_db.py
   ```

6. **Run the application**:
   ```bash
   uvicorn app:app --host 0.0.0.0 --port 8000 --reload
   ```

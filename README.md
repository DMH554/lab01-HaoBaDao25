# Study Assistant — starter

A starter repository for the CSC10014 Smart Virtual Assistant project.

## Setup

Requirements: Python 3.10 or newer (tested with Python 3.12) and Git.
Python 3.9 (the default on macOS) is too old and fails at the `pip install -e .` step.

1. Clone the repository and enter it:

        git clone https://github.com/DMH554/lab01-HaoBaDao25.git
        cd lab01-HaoBaDao25

2. Create a virtual environment (use python3.12, or any python3.10+ you have):

        python3.12 -m venv .venv

3. Activate it. The prompt should start with (.venv):

        source .venv/bin/activate

   On Windows PowerShell use `.venv\Scripts\Activate.ps1` instead.

4. Upgrade pip and install the dependencies:

        python -m pip install --upgrade pip
        pip install -r requirements.txt
        pip install -e .

5. Check your environment. Every line should show [ OK ]:

        python scripts/check_env.py

Every time you open a new terminal, go to the project folder and run
`source .venv/bin/activate` again.

## Run

        python -m assistant "where is the IT helpdesk?"

Expected output:

        IT Helpdesk: room E.005, open Mon-Fri 08:00-17:00.

## Test

        pytest -q

Expected output: 4 passed.

## Project structure

- `src/assistant/` - backend code of the assistant (Python package)
- `data/` - data files, for example `offices.csv`
- `tests/` - automated tests run with pytest
- `scripts/` - helper scripts, for example `check_env.py`
- `ui/` - user interface (planned)
- `docs/` - documentation
- `requirements.txt` - Python dependencies
- `pyproject.toml` - package configuration

# Basic Patient Database Explorer (RAG) -> llama3.2 Vision

A simple Streamlit application that enables users to ask natural language questions about a patient database. The app processes the user's query, converts it to SQL using a large language model (LLM), executes the query on a SQLite database, and synthesizes the results into a natural language response.

## Features
- Converts natural language queries to SQL.
- Executes SQL queries on a SQLite database.
- Synthesizes SQL query results into human-readable responses.
- Interactive user interface built with Streamlit.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/saadtariq001s/patient-database-explorer.git
    cd patient-database-explorer
    ```

2. Create and activate a virtual environment (optional but recommended):
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Run the Streamlit app:
    ```bash
    streamlit run app.py
    ```

## Usage
1. Open the app in your browser (Streamlit will provide the URL).
2. Enter a natural language query in the input box (e.g., "How many patients are from California?").
3. Click the "Get Insights" button to:
    - View the generated SQL query.
    - See the query results in tabular format.
    - Read the synthesized response in plain language.

## Prerequisites
- Python 3.8 or higher
- [Ollama API](https://ollama.com/) access (for query-to-SQL conversion and result synthesis).

## File Structure
- `app.py`: Main application code.
- `requirements.txt`: List of Python dependencies.
- `patient.db`: SQLite database file (created dynamically at runtime).
- `README.md`: Project documentation (this file).

## Notes
- The `ollama` library must be configured and authenticated properly to use the LLM features.
- Ensure you have permissions to access the LLM model specified in the code.

## License
This project is open-source and licensed under the MIT License.

---

### Example Query
**Input:** "How many patients are from California?"  
**Generated SQL:** `SELECT COUNT(*) FROM patients WHERE state = 'California';`  
**Result:** 3  
**Synthesized Response:** "There are 3 patients from California."

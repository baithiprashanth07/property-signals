# Property Signal

Property Signal is a Python and Streamlit chatbot for exploring a curated property data snapshot. It retrieves relevant DarGlobal project records and Wasalt listing records, sends source-grounded evidence to OpenRouter, and links every supported answer back to the public source.

## Features

- Streamlit chat interface with starter questions
- Location, property type, bedroom, and budget-aware retrieval
- Cheapest, most expensive, and largest-result sorting
- Up to six retrieved evidence records per question
- Source citations and direct public-source links
- Session conversation history
- OpenRouter `openrouter/free` model routing
- Clear snapshot and source-limit messaging

## Data snapshot

`data/public-corpus.json` contains:

- 17 DarGlobal development records
- 22 Wasalt listing records
- A collection date of 2026-11-18

DarGlobal records come from its public project catalogue and reviewed project pages. The Wasalt records are a sample of listings visible on the public Al Narjis, North Riyadh sale page, not a complete or live inventory.

Prices and availability can change. Use the links shown in the app to verify current details. Additional collection scope and source observations are documented in `RESEARCH.md`.

## Requirements

- Python 3.11 or later
- An OpenRouter API key
- Internet access

## Local setup

1. Clone or download this project.
2. Create and activate a Python virtual environment:

```powershell
python -m venv .venv
.venv\Scripts\Activate.ps1
```

3. Install dependencies:

```powershell
python -m pip install -r requirements.txt
```

4. Add the API key to `.env`:

```dotenv
OPENROUTER_API_KEY=your-openrouter-api-key
```

Alternatively, configure Streamlit secrets in `.streamlit/secrets.toml`:

```toml
OPENROUTER_API_KEY = "your-openrouter-api-key"
```

5. Start the application:

```powershell
python -m streamlit run app.py
```

Open the local URL printed by Streamlit, normally `http://localhost:8501`.

## How it works

1. `app.py` loads `data/public-corpus.json`.
2. The user question is normalized and checked for location, property type, bedrooms, budget, and sorting criteria.
3. The retrieval function ranks matching records and sends up to six records as evidence.
4. OpenRouter receives the question, recent chat context, and evidence JSON.
5. Streamlit displays the answer, source markers, retrieved source cards, and source URLs.

The model is instructed not to invent facts or use evidence absent from the supplied snapshot. OpenRouter model availability and capacity can vary.

## Project structure

```text
app.py                   Streamlit interface and retrieval logic
data/public-corpus.json  Curated dated property records
requirements.txt         Python dependencies
.env                     Local API-key configuration (ignored by Git)
RESEARCH.md              Source scope and collection observations
.gitignore               Local and generated-file exclusions
```

## Security

Keep API keys in `.env` or Streamlit secrets. Never commit `.env`, `.streamlit/secrets.toml`, or API keys to source control. Both locations are excluded by the project Git configuration.

## Sources

- [DarGlobal project catalogue](https://darglobal.co.uk/projects)
- [DarGlobal Trump Mansions](https://darglobal.co.uk/rayana/trump-mansions)
- [DarGlobal Neptune](https://darglobal.co.uk/neptune)
- [Wasalt Al Narjis for-sale listings](https://wasalt.sa/en/properties-for-sale-in-north-riyadh-al-narjis)
- [Example Wasalt listing](https://wasalt.sa/en/property/sale/apartment-9241-sqm-with-2-bedrooms-5948554)
- [OpenRouter free-model routing](https://openrouter.ai/docs/guides/routing/routers/free-router)

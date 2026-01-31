---
# Custom Agent Tutorial

A small Python-based example that demonstrates how to configure and run a "custom agent" script which uses web search (Serper) and OpenAI APIs to process queries. This repository includes the agent runner (`agent.py`), a configuration file (`config.yaml`), and a `requirements.txt` listing dependencies.

## Features
- Simple agent runner for interactive or scripted queries
- Pluggable configuration via `config.yaml` for API keys and options
- Minimal example to learn how to wire search + LLM APIs together

## Prerequisites
- Python 3.10+ (recommended)
- pip (or use conda)
- Valid API keys for:
  - Serper (for web search): https://serper.dev/
  - OpenAI (for LLM access): https://openai.com/

## Setup
1. Clone this repository (use your fork or the original):

```bash
git clone https://github.com/brothergbk/custom_agent_tutorial.git
cd custom_agent_tutorial
```

2. Create and activate a virtual environment (using conda or python venv):

Using conda:

```bash
conda create -n agent_env python=3.10 pip
conda activate agent_env
```

Or using venv:

```bash
python3 -m venv .venv
source .venv/bin/activate   # macOS / Linux
.\.venv\Scripts\activate  # Windows (PowerShell)
```

3. Install dependencies:

```bash
pip install -r requirements.txt
```

## Configuration
Open `config.yaml` and add your API keys and any other required configuration values. Example keys to set:

```yaml
serper_api_key: "YOUR_SERPER_API_KEY"
openai_api_key: "YOUR_OPENAI_API_KEY"
# other options may be present depending on scripts in the repo
```

Note: If `config.yaml` is not present, create it at the repo root. Keep your keys secret — do not commit them to public repositories.

## Running the Agent
The repository includes an `agent.py` script. To run a query using the default runner:

```bash
python agent.py run
```

Depending on how `agent.py` is implemented you may be able to pass additional arguments or run an interactive prompt. If you want help from the script itself, try:

```bash
python agent.py --help
# or
python agent.py -h
```

## Examples
- Run a simple query (if supported):

```bash
python agent.py run --query "What is the capital of France?"
```

Adjust flags/arguments according to the script's CLI.

## Troubleshooting
- Missing dependencies: ensure `pip install -r requirements.txt` completed successfully.
- API key errors: verify keys are correct and have required permissions for Serper/OpenAI.
- Network errors: ensure your machine has internet access and no outbound requests are blocked.

## Contributing
Feel free to open issues or PRs with improvements, bug fixes, or documentation updates.

## License
Specify the license for the project here (e.g., MIT). If no license file exists, add one or clarify the intended license.

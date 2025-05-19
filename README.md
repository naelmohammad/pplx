# pplx & pplxpro

**Perplexity CLI Agent**  
A command-line interface for [Perplexity AI](https://www.perplexity.ai/).

---

## Features

- Query Perplexity AI directly from your terminal
- Supports multiple models (e.g., sonar-pro, mistral-7b-instruct)
- Simple, scriptable, and fast
- pplx - supports default models for non-pro perplexity users.
- pplxpro - supports additional models for perplexity pro users. 

## Supported Models as of 05/19/2025

- sonar-small-online
- sonar-medium-online
- sonar-small-chat
- sonar-medium-chat
- mistral-7b-instruct
- llama-3.1-sonar-small-128k-online
- llama-3.1-sonar-large-128k-online
- sonar-pro
- gpt-4-omni
- claude-3.5-sonnet
- gemini-2.0-flash

---

## Requirements

- macOS Sequoia (or similar Unix-like system)
- Python 3.6 or later
- `git`
- Perplexity API key

---

## Installation

### 1. Clone the Repository

```bash
git clone https://github.com/naelmohammad/pplx.git
cd pplx
```

### 2. (Recommended) Create a Virtual Environment

```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Install the CLI Script

```bash
mv pplx > ~/.local/bin/pplx
mv pplxpro > ~/.local/bin/pplxpro

chmod +x ~/.local/bin/pplx
chmod +x ~/.local/bin/pplxpro

```

### 5. Add to PATH

Ensure `~/.local/bin` is in your PATH.  
For **bash**:
```bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
```
For **zsh** (default on recent macOS):
```bash
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.zshrc
```

### 6. Set Your Perplexity API Key

Generate your API key at: [Perplexity API Docs](https://docs.perplexity.ai/guides/getting-started#generating-an-api-key)

Export your API key as an environment variable:

For **bash**:
```bash
echo 'export PERPLEXITY_API_KEY="your-api-key"' >> ~/.bashrc
```
For **zsh**:
```bash
echo 'export PERPLEXITY_API_KEY="your-api-key"' >> ~/.zshrc
```

Reload your shell configuration:

```bash
source ~/.bashrc    # or source ~/.zshrc
```

---

## Usage

Ask a question from your terminal:

```bash
pplx "What is the time in epoch format?"
pplxpro "What is the time in epoch format?"

```

Specify a model:

```bash
pplx -m sonar-pro "Explain Moore's Law"
pplxpro -m llama-3.1-sonar-small-128k-online "What is the time in epoch format?"

```

Show help and options:

```bash
pplx -h
pplxpro -h
```

### CLI Options

```
usage: pplx [-h] [-m {sonar-pro,mistral-7b-instruct,sonar-small,sonar-medium}] query [query ...]

positional arguments:
  query                 Your search query (no quotes needed)

options:
  -h, --help            Show this help message and exit
  -m, --model           Model to use (default: sonar-pro)
```

```
usage: pplxpro [-h]  [-m {sonar-small-online,sonar-medium-online,sonar-small-chat,sonar-medium-chat,mistral-7b-instruct,llama-3.1-sonar-small-128k-online,llama-3.1-sonar-large-128k-online,sonar-pro,gpt-4-omni,claude-3.5-sonnet,gemini-2.0-flash}] query [query ...]

```
---

## Troubleshooting

- Ensure your API key is set and your shell is reloaded.
- Make sure `~/.local/bin` is in your PATH.
- For issues, open an [issue on GitHub](https://github.com/naelmohammad/pplx/issues).

---

## License

GPL V3 License

---

**Happy querying!**

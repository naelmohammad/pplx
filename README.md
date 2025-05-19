# pplx
Perplexity cli agent for use with https://www.perplexity.ai/



How to Install Perplexity CLI on macOS Sequoia
Requirements:

Python 3.6 or later (pre-installed on most modern Macs)

requests Python library (install with pip install requests)

A Perplexity API key (set as an environment variable)


1. Installation Steps:

Download the CLI Script:
Open Terminal and run:


curl -s https://raw.githubusercontent.com/naelmohammad/pplx/main/pplx.py > ~/.local/bin/pplx
chmod +x ~/.local/bin/pplx

2. Add to PATH:
Ensure ~/.local/bin is in your PATH. You can add it by running:


echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc

If you use Zsh (the default on recent macOS versions), replace .bashrc with .zshrc.

3. Set Your API Key:
Generate API keys:
- https://docs.perplexity.ai/guides/getting-started#generating-an-api-key

Export your Perplexity API key as an environment variable:


echo 'export PERPLEXITY_API_KEY="your-api-key"' >> ~/.bashrc

(Again, use .zshrc if you use Zsh.)

4. Restart Terminal or run source ~/.bashrc (or source ~/.zshrc) to apply changes.


Usage Example
Ask a question from your terminal:
pplx "What is the time in epoch format?"


You can also use additional options, such as specifying the model or displaying citations:

pplx -m sonar-pro "Explain Moore's Law"

More options: 
usage: pplx [-h] [-m {sonar-pro,mistral-7b-instruct,sonar-small,sonar-medium}] query [query ...]




pplx "What is the time in epoch format?" 

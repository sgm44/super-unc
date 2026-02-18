# Bot Agent

A simple browser-based chat agent powered by the Anthropic Claude API. No build step, no dependencies — just open `index.html`.

## Setup

1. Get an API key from [console.anthropic.com](https://console.anthropic.com)
2. Open `index.html` and find this line near the top of the `<script>` block:
   ```js
   const API_KEY = '';
   ```
3. Paste your key between the quotes
4. Open `index.html` in a browser (or serve locally — see below)

## Running locally

```bash
# Python
python3 -m http.server 8000

# Node
npx serve
```

Then open `http://localhost:8000`.

## How it works

- The bot opens with: *"What would you like help with today?"*
- It asks one clarifying question before answering
- Full conversation history is sent with each request so the bot maintains context

## Customizing

| Variable in `index.html` | Purpose |
|---|---|
| `API_KEY` | Your Anthropic API key |
| `MODEL` | Claude model to use |
| `SYSTEM_PROMPT` | Controls the bot's personality and behavior |

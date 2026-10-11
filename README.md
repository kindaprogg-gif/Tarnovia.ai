# Tarnovia.ai

**Your AI assistant. Your models. Your control.**

Tarnovia.ai is a lightweight AI assistant built with Python and Flask. It provides a web-based chat interface for interacting with AI models through OpenAI-compatible APIs, with support for local Ollama models when running locally.

## ✨ Features

- 💬 **AI Chat** — chat with supported AI models through a simple web interface.
- 🔌 **OpenAI-Compatible APIs** — connect to compatible AI providers.
- 🖥️ **Local Ollama Support** — run supported local models with Ollama.
- 🌐 **Web Interface** — access the application through your browser.
- ⚙️ **Configurable** — configure the model and API connection using environment variables.
- 🚀 **Self-Hosting** — run locally or deploy as a web service.

## 🛠️ Tech Stack

- Python
- Flask
- HTML, CSS, and JavaScript
- OpenAI-compatible Chat Completions API
- Ollama (optional, for local use)

## 📋 Requirements

- Python 3.10 or newer
- `pip`
- An API key from a supported AI provider, or a local Ollama installation

## 🚀 Run Locally

1. Clone the repository:

   ```bash
   git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
   cd YOUR_REPOSITORY
   ```

2. Install the dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Configure your API connection.

   **Windows PowerShell:**

   ```powershell
   $env:TARNOVIA_API_KEY="your-api-key"
   $env:TARNOVIA_MODEL="gpt-4.1-mini"
   ```

   Keep your API key private. Never commit it to GitHub.

4. Start the application:

   ```bash
   python gui.py
   ```

5. Open your browser at:

   [http://127.0.0.1:8765](http://127.0.0.1:8765)

## 🦙 Using Ollama

To use local models, install and run Ollama on your computer, download a compatible model, and configure Tarnovia.ai to use your local Ollama service.

Ollama must be accessible from the environment running Tarnovia.ai. A cloud-hosted instance cannot automatically access Ollama running on your personal computer.

## ☁️ Cloud Deployment

Tarnovia.ai can be deployed as a Python web service on a platform such as Render.

Typical configuration:

- **Build command:** `pip install -r requirements.txt`
- **Start command:** `gunicorn gui:app`

Add your API credentials through the hosting provider's environment-variable settings:

- `TARNOVIA_API_KEY` — your provider's API key
- `TARNOVIA_MODEL` — the model to use, such as `gpt-4.1-mini`
- `TARNOVIA_BASE_URL` — optional API base URL for a compatible provider

Make sure `gunicorn` is included in `requirements.txt` before deploying.

**Security note:** Before exposing the application publicly, configure it so visitors cannot change shared server settings or consume your API quota without appropriate limits. Never expose API keys in browser-side code.

## 🔐 Security

- Store API keys in environment variables.
- Do not commit `.env` files, API keys, or private configuration files.
- Add authentication and rate limiting before offering a public instance to unrestricted users.
- Review provider usage and costs when enabling API access.

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for details.

## 🤝 Contributing

Suggestions, bug reports, and contributions are welcome. Please open an issue to discuss significant changes before submitting a pull request.

---

**Tarnovia.ai** — built to make AI more accessible and customizable.

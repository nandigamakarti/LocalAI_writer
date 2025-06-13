# 🧠 LocalAI Explainer  
**Explain Any Concept Simply — Powered by Your Local LLM**

A clean and privacy-first web app that uses locally running large language models (via Ollama) to break down any concept in simple terms. No cloud APIs. No data leaks. Just pure, offline AI.

---

## 🌟 App Type

**Concept Explainer** – enter any topic, and get a plain-language explanation using local inference.

---

## ⚙️ Features

- 🛡️ **Fully Local Inference** – no internet, no external APIs; all responses are generated using Ollama on your machine  
- 🧠 **Multi-model Support** – switch easily between models like `llama3`, `mistral`, `gemma`, and more  
- 🎛️ **Adjustable Temperature** – control creativity with a simple slider  
- 💬 **Prompt & Response Interface** – clean, minimal UI with instant feedback  
- 📝 **Local Logging** – every explanation is saved automatically  
- 📱 **Responsive UI** – works smoothly on both desktop and mobile devices  

---

## 🚀 Quickstart

### ✅ Prerequisites

- Node.js `v14+`
- npm `v6+`
- Ollama installed and running: [https://ollama.com](https://ollama.com)
- At least one model pulled (e.g., `ollama pull llama3`)

---

## 🛠️ Installation & Setup

```bash
# Clone the repo
git clone https://github.com/nandigamakarti/LocalAI_writer.git
cd LocalAI_writer

# Install dependencies
npm install

# Configure environment variables (optional)
cp .env-example .env
```

### 🧠 Pull a model with Ollama

```bash
ollama pull llama3  # or mistral, gemma, phi, etc.
```

---

## ▶️ Run the App

Start the app:

```bash
npm start
```

For development mode (with hot-reloading):

```bash
npm run dev
```

Then open your browser:

```
http://localhost:3000
```

---

## 🧪 Using the App

1. Type any concept into the input box (e.g., “Quantum Entanglement”)
2. Choose a model (e.g., `llama3`)
3. Adjust the temperature if needed (higher = more creative, lower = more focused)
4. Click “Explain”
5. The output will be displayed and logged

---

## 📁 Project Structure

```
LocalAI_writer/
├── public/
│   ├── index.html      # Frontend UI
│   ├── script.js       # Client-side JS
│   └── styles.css      # Basic styling
├── logs/               # Auto-generated explanation logs
├── server.js           # Express API backend
├── .env                # Environment variables
├── .env-example        # Example config
├── package.json        # Dependencies
└── README.md           # Project documentation
```

---

## 🧩 How It Works

1. User inputs a concept and submits the request
2. The backend (`server.js`) sends the prompt to the Ollama local API
3. Ollama runs the selected model and returns a response
4. Response is shown on-screen and saved locally in the `logs/` folder

---

## 🛠 Customization

### ➕ Add More Models

```bash
ollama pull phi
ollama pull codellama
```

Then update the model dropdown in `public/index.html`.

### 🎨 Customize the Prompt Logic

Edit the prompt generation in `server.js` to make responses more formal, casual, or use role-based instructions (e.g., “Explain as if to a 12-year-old”).

---

## ❗ Troubleshooting

- **Ollama not running?** → Start it from terminal: `ollama run llama3`
- **Model missing?** → Run: `ollama pull <model-name>`
- **App not loading?** → Check browser console or terminal logs

---

## 📄 License

MIT License – use, fork, and modify freely.

---

## 🙌 Acknowledgements

- [Ollama](https://ollama.com) – for making local LLMs accessible
- [Express](https://expressjs.com) – lightweight backend API
- All open-source contributors and model creators

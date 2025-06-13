# Local Inference Concept Explainer

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)

A lightweight web application that explains concepts in simple terms using locally running Large Language Models (LLMs). This application leverages Ollama to run inference on your local machine, ensuring privacy and eliminating the need for external API calls.

![Concept Explainer Screenshot](https://via.placeholder.com/800x450.png?text=Concept+Explainer+App)

## 🌟 Features

- **Local Inference**: All processing happens on your machine - no data sent to external services
- **Multiple Model Support**: Works with various models available in Ollama (Llama 3, Mistral, Gemma, etc.)
- **Adjustable Parameters**: Control temperature settings to fine-tune response creativity
- **Responsive Design**: Works on both desktop and mobile devices
- **Logging**: Keeps track of all explanations for future reference
- **Simple Interface**: Clean, intuitive UI for easy interaction

## 🚀 Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher)
- [npm](https://www.npmjs.com/) (v6 or higher)
- [Ollama](https://ollama.ai/) installed and running on your machine

### Installation

1. **Clone the repository**

   ```bash
   git clone https://github.com/nandigamakarti/LocalAI_writer.git
   cd LocalAI_writer
   ```

2. **Install dependencies**

   ```bash
   npm install
   ```

3. **Set up environment variables**

   Copy the example environment file and modify if needed:
   ```bash
   cp .env-example .env
   ```

4. **Install and set up Ollama**

   - Download and install Ollama from [https://ollama.ai/](https://ollama.ai/)
   - Pull at least one model:
     ```bash
     ollama pull llama3
     ```
   - You can also pull other models like:
     ```bash
     ollama pull mistral
     ollama pull gemma
     ```

## 🔧 Usage

1. **Start the server**

   ```bash
   npm start
   ```
   
   For development with auto-restart:
   ```bash
   npm run dev
   ```

2. **Access the application**

   Open your browser and navigate to:
   ```
   http://localhost:3000
   ```

3. **Using the application**

   - Enter a concept or term you want explained in the input box
   - Adjust the temperature slider if desired (lower for more focused responses, higher for more creative ones)
   - Select the model you want to use from the dropdown
   - Click "Explain" and wait for the response
   - The explanation will appear in the output section

## 📁 Project Structure

```
├── public/                 # Static files
│   ├── index.html          # Main HTML file
│   ├── script.js           # Client-side JavaScript
│   └── styles.css          # CSS styles
├── logs/                   # Generated log files
├── .env                    # Environment variables
├── .env-example            # Example environment file
├── .gitignore              # Git ignore file
├── package.json            # Project dependencies
├── README.md               # Project documentation
└── server.js               # Express server and API endpoints
```

## 🔍 How It Works

1. The Express server provides an API endpoint for generating explanations
2. When a user submits a concept, the request is sent to the server
3. The server uses the Ollama client to send the prompt to the locally running LLM
4. The LLM generates an explanation which is returned to the client
5. All interactions are logged to a local file

## ⚠️ Troubleshooting

- **Connection Issues**: Make sure Ollama is running before starting the app
- **Model Not Found**: Ensure you've pulled the model you're trying to use with `ollama pull <model-name>`
- **Slow Responses**: Response time depends on your hardware and the model size
- **Error Messages**: Check the console and log files for detailed error information

## 🛠️ Development

### Adding New Models

To add support for new models:

1. Pull the model using Ollama: `ollama pull <model-name>`
2. Add the model to the dropdown in `public/index.html`

### Customizing Prompts

You can modify the prompt template in `server.js` to change how concepts are explained.

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgements

- [Ollama](https://ollama.ai/) for providing the local LLM runtime
- [Express](https://expressjs.com/) for the web server framework
- All the amazing open-source LLM models that make local inference possible
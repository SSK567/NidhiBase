# NidhiBase
NidhiBase: A privacy-first, zero-dependency personal finance dashboard featuring on-device AI (WebLLM/WebGPU), offline voice-to-ledger (Whisper), and live global market charts in a single-file architecture.


# 💸 NidhiBase — Human-First Finance

NidhiBase is a privacy-first, edge-computed personal finance strategist and portfolio tracker. It is built entirely as a **single-file web application** (HTML/CSS/JS) with zero external build dependencies, ensuring maximum portability and security. 
*💡 **Inspiration:** This project is deeply inspired by **FinVault — Financial Hub**. While FinVault set a great benchmark for financial tracking, NidhiBase builds upon that vision by introducing strictly on-device, offline-first AI capabilities.*
Instead of relying on cloud servers for processing your sensitive financial data, NidhiBase leverages the power of modern browser APIs to run **Large Language Models (LLMs) and Speech-to-Text (STT) completely offline and on-device**.

🙏 Acknowledgments
Massive shoutout and credit to FinVault — Financial Hub for the original design and conceptual inspiration for a unified financial dashboard.

Built with WebLLM and Transformers.js.
https://ssk567.github.io/FinVault/

## ✨ Key Features

* **🧠 On-Device AI Strategist:** Runs LLMs (like Llama 3.2 1B or Qwen 4B) locally using **WebLLM** and **WebGPU**. No API keys, no server costs, and your data never leaves your machine.
* **🎙️ Offline Voice Khata (Whisper):** Uses `Transformers.js` to run the Whisper-tiny model directly in the browser via WebAssembly. Simply speak your transactions, and the AI categorizes and logs them offline.
* **🌍 Global Market RAG (Retrieval-Augmented Generation):** Fetches live global stock and crypto prices directly from public sources (Finnhub, TwelveData, Yahoo Finance) and injects them into the local AI's prompt for real-time, context-aware financial tutoring.
* **🔐 Local JSON Vault:** Total data ownership. All transactions, portfolios, and budgets are saved to your local file system using the Native File System API.
* **📊 Live TradingView Integration:** Synchronized global market charts that automatically update when you ask the AI about a specific stock or asset.
* **🧮 Comprehensive Calculators:** Built-in tools for SIP, SWP, Lumpsum, EMI, CAGR, XIRR, and Tax Regime comparisons.

## 🛠️ Tech Stack & Architecture

* **Frontend:** Vanilla HTML5, CSS3, JavaScript (ES6+)
* **AI/ML (In-Browser):** WebLLM (MLC-AI), Transformers.js (@xenova/transformers)
* **Hardware Acceleration:** WebGPU (for LLM inference), WebAssembly (for Whisper STT)
* **Storage:** `localStorage` & File System Access API (Local JSON Vault)
* **Data Sources (Client-Side):** TradingView Widgets, Finnhub, TwelveData, Yahoo Finance, mfapi.in

*Note: This project deliberately uses a single-file architecture to demonstrate complex state management, dynamic UI rendering, and edge-AI integration without relying on frameworks like React or build tools like Webpack.*

## 🚀 How to Run Locally

Since this is a client-side only application, getting started is incredibly simple:

1. **Clone the repository:**
   ```bash
   git clone [https://github.com/yourusername/NidhiBase.git](https://github.com/yourusername/NidhiBase.git)


Note: For the On-Device AI (WebLLM) to work, you must use a WebGPU-enabled browser (Chrome/Edge 113+ or Safari 18+).

   🔒 Security & Privacy Notice
This application is designed for absolute privacy. The core ledger and financial data remain strictly within your browser's local storage and the local JSON vault you define. The AI model runs on your local GPU, meaning your financial queries are never sent to OpenAI, Google, or any third-party server.

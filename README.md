# 🏢 Real Estate Management — Smart Cockpit

An intelligent, AI-powered master cockpit for real estate management: visualizing processes and architecture, analyzing portfolio data and fixed costs.

## ✨ Key Features

* **🤖 Multi-AI Integration:** Supports [Google Gemini](https://ai.google.dev/), [OpenAI](https://platform.openai.com/), [OpenRouter](https://openrouter.ai/) (including Anthropic Claude models there) and local models via [Ollama](https://ollama.com/).
* **📊 Interactive Dashboard:** Overview of key KPIs (Managed Units, Energy Consumption, Open Tickets) with AI-powered ticket creation and consumption normalization from emails or documents.
* **⚙️ Dynamic Process & Architecture Diagrams:** Automatic generation of process flow diagrams (BPMN-style) and IT architecture diagrams (C4-style) from simple text descriptions (Mermaid.js).
* **💶 Fixed Cost Management:** Automatic extraction of cost items from uploaded invoices.
* **🥧 Portfolio Analysis:** Visual representation of property/tenant distributions as a doughnut chart.
* **🕸️ Knowledge Graph:** Building and expanding a network of entities and relations (e.g., who manages which building).
* **💬 AI Document Chat:** Direct interaction with the AI assistant for domain-specific questions.
* **📥 Export:** Save data as CSV or download diagrams (processes, architecture, portfolio, knowledge graph) as PNG images.

## 🚀 Installation & Usage

1. **Download:** Save the `index.html` file locally on your computer.
2. **Run:** Simply open the HTML file in a modern web browser (Chrome, Firefox, Edge). No local server is needed (except for Ollama). **Important:** The external libraries (Mermaid, Chart.js, vis-network, html2canvas, pdf.js) are loaded from a CDN — without an internet connection the app starts in reduced mode and shows a warning banner.
3. **Configure AI:**
   * Select the desired **AI Provider** at the top of the app.
   * Enter the corresponding **API Key** (the key is never stored and never written into the URL — it is only sent as a request header to the provider).
   * If you use [Ollama](https://ollama.com/) locally, ensure the Ollama service is running on `http://localhost:11434` and CORS is properly configured.
   * Click **🔌 Test** to verify the connection.

## 💾 Data Storage (localStorage)

The app stores the active tab, fixed costs, portfolio data, chat history, knowledge graph, KPI values and the selected provider/model configuration in the browser's `localStorage` and restores them after a reload. The **API key is deliberately not stored** and must be re-entered after each reload.

## 🛠️ Technologies & Libraries Used

This project is a lightweight Single-Page Application (SPA) built with Vanilla JavaScript, HTML5, and CSS3 (CSS variables for theming). External libraries (via CDN):

* [**Mermaid.js**](https://mermaid.js.org/) – For rendering process and architecture diagrams.
* [**Chart.js**](https://www.chartjs.org/) – For visualizing portfolio data (doughnut chart).
* [**Vis-Network**](https://visjs.github.io/vis-network/docs/network/) – For interactive rendering of the knowledge graph.
* [**html2canvas**](https://html2canvas.hertzen.com/) – To export HTML elements and diagrams as PNG images.
* [**pdf.js**](https://mozilla.github.io/pdf.js/) – For text extraction from PDF invoices.

## 💡 Usage Notes

* **Drag & Drop:** In the "Overview" and "Fixed Costs" modules, invoices or email content can be dragged and dropped directly into the designated drop zones (.txt, .csv, .json, .xml, .eml, .pdf; max 2 MB).
* **Privacy:** Since processing happens directly in the browser via API calls, sensitive data is sent directly to the selected AI provider. If strict data privacy is required, it is highly recommended to use the local connection via Ollama.

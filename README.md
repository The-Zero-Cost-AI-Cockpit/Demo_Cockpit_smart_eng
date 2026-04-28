# 🏢 Real Estate Management — Smart Cockpit

An intelligent, AI-powered master cockpit for managing real estate, visualizing processes and architecture, as well as analyzing portfolio data and fixed costs.

## ✨ Key Features

* **🤖 Multi-AI Integration:** Seamlessly supports various AI providers like [Google Gemini](https://ai.google.dev/), [OpenAI](https://platform.openai.com/), [Anthropic Claude](https://www.anthropic.com/api), [OpenRouter](https://openrouter.ai/), and local models via [Ollama](https://ollama.com/).
* **📊 Interactive Dashboard:** Overview of key KPIs (Managed Units, Energy Costs, Open Tickets) with AI-powered ticket creation and consumption normalization from emails or documents.
* **⚙️ Dynamic Process & Architecture Diagrams:** Automatic generation of BPMN process flows and C4 IT architectures through simple text descriptions.
* **💶 Fixed Cost Management:** Automatic extraction of cost items from uploaded invoices.
* **🥧 Portfolio Analysis:** Visual representation of property or tenant distributions using pie charts.
* **🕸️ Knowledge Graph:** Building and expanding a network of entities and relations (e.g., who manages which building).
* **💬 AI Document Chat:** Direct interaction with the AI assistant for domain-specific questions.
* **📥 Export:** Save data as CSV or download diagrams as images.

## 🚀 Installation & Usage

1. **Download:** Save the `Cockpit Smart.html` file locally on your computer.
2. **Run:** Simply open the HTML file in a modern web browser (e.g., Chrome, Firefox, Edge). No local server is needed (except for Ollama).
3. **Configure AI:** * Select the desired **AI Provider Set** at the top of the app.
   * Enter the corresponding **API Key**.
   * If you use [Ollama](https://ollama.com/) locally, ensure the Ollama service is running on `http://localhost:11434` and CORS is properly configured.
   * Click **🔌 Test** to verify the connection.

## 🛠️ Technologies & Libraries Used

This project is designed as a lightweight Single-Page Application (SPA) using Vanilla JavaScript, HTML5, and CSS3 (with CSS variables for theming). Additionally, the following external libraries are used:

* [**Mermaid.js**](https://mermaid.js.org/) – For rendering BPMN and C4 architecture diagrams.
* [**Chart.js**](https://www.chartjs.org/) – For visualizing portfolio data (pie charts).
* [**Vis-Network**](https://visjs.github.io/vis-network/docs/network/) – For interactive rendering of the knowledge graph.
* [**html2canvas**](https://html2canvas.hertzen.com/) – To export HTML elements and diagrams as PNG images.

## 💡 Usage Notes

* **Drag & Drop:** In the "Overview" and "Fixed Costs" modules, invoices or email content can be dragged and dropped directly into the designated drop zones.
* **Privacy:** Since the processing happens directly in the browser via API calls, sensitive data is sent directly to the selected AI provider. If strict data privacy is required, it is highly recommended to use the local connection via Ollama.

# chatbot-guardrail-practice

## Description

**chatbot-guardrail-practice** is a context-aware AI assistant built with the [`agents`](https://github.com/openai/openai-agents) library. It uses the Gemini 2.0 Flash model to demonstrate how to apply **input and output guardrails** using custom Pydantic schemas. The agent is integrated with [Chainlit](https://docs.chainlit.io/) to create an interactive conversational interface.

The assistant is designed for customer support and includes guardrails to detect and filter math-related input or output.

---

## Features

- ✅ Guardrail on **input**: Detects if a user is asking for help with math homework  
- ✅ Guardrail on **output**: Flags any response that includes math-related content  
- ✅ Powered by Gemini 2.0 via OpenAI-compatible API  
- ✅ Chainlit-based chat interface  
- ✅ Uses `RunContextWrapper` for structured agent execution

---

## Tech Stack

- **Python 3.8+**
- **Libraries**:
  - [`agents`](https://github.com/openai/openai-agents)
  - `chainlit`
  - `pydantic`
  - `dotenv`
  - `asyncio`

---

## Installation

1. **Clone the repository**:

```bash
git clone https://github.com/moizdevhub/chatbot-guardrail-practice.git
cd chatbot-guardrail-practice

Create and activate a virtual environment (recommended):

python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
Install dependencies:

pip install -r requirements.txt
If requirements.txt is missing, install manually:

pip install agents chainlit python-dotenv pydantic
Create a .env file with your Gemini API key:

GEMINI_API_KEY=your_gemini_api_key
```

## Usage
Start the Chainlit server:

chainlit run main.py
Open your browser at the local address (usually http://localhost:8000) to start chatting.

Example prompt:

Can you solve this equation for me?
You’ll see a guardrail warning if your input or the assistant's output includes math.


## License
This project is licensed under the MIT License.

# AI Agent - Kaggle Project

An AI-powered agent project built with Google's Gemini API and Agent Development Kit (ADK). This project demonstrates how to create and interact with LLM agents using Python.

## 📋 Project Structure

```
kaggle/
├── Day_1a_From_Prompt_to_Action.ipynb    # Main Jupyter notebook
├── hero_agent/                            # Agent module
│   ├── __init__.py
│   ├── agent.py                          # Agent implementation
│   └── .env                              # Environment variables (gitignored)
├── kaggleenv/                            # Python virtual environment
├── .gitignore                            # Git ignore rules
└── README.md                             # This file
```

## 🚀 Getting Started

### Prerequisites

- Python 3.8+
- Google Gemini API key
- pip (Python package manager)

### Installation

1. **Clone or navigate to the project directory**
   ```bash
   cd kaggle
   ```

2. **Create and activate a virtual environment** (if not already done)
   ```bash
   python -m venv kaggleenv
   
   # On Windows:
   kaggleenv\Scripts\activate
   
   # On macOS/Linux:
   source kaggleenv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   # Or install individual packages:
   pip install google-genai python-dotenv ipykernel jupyter
   ```

### Configuration

1. **Create a `.env` file** in the project root and `hero_agent/` directory:
   ```env
   GOOGLE_API_KEY=your_api_key_here
   ```

2. **Get your Google API Key**:
   - Visit [Google AI Studio](https://aistudio.google.com/app/apikey)
   - Create a new API key
   - Add it to your `.env` file

## 📖 Usage

### Running the Jupyter Notebook

```bash
# Start Jupyter
jupyter notebook

# Open: Day_1a_From_Prompt_to_Action.ipynb
```

### Using the Hero Agent

```python
from hero_agent.agent import root_agent

# The agent is pre-configured with Gemini 2.5 Flash Lite model
# Use it to answer questions or process prompts
response = root_agent.generate(prompt="Your question here")
```

## 🔧 Agent Configuration

The agent is configured in `hero_agent/agent.py`:

- **Model**: `gemini-2.5-flash-lite` (optimized for speed and efficiency)
- **Name**: `root_agent`
- **Purpose**: Helpful assistant for user questions

You can modify the model, description, and instructions in `agent.py` as needed.

## 🔐 Security

- **Never commit `.env` files** - They contain sensitive API keys
- The `.env` file is already in `.gitignore`
- Always keep API keys private and secure

## 📦 Dependencies

Key packages used:
- `google-genai` - Google AI API client
- `google-adk` - Agent Development Kit
- `python-dotenv` - Environment variable management
- `jupyter`/`ipykernel` - Notebook environment

## 🐛 Troubleshooting

### API Key Issues
```
🔑 Authentication Error: Please make sure you have added 'GOOGLE_API_KEY' to your Kaggle secrets.
```
- Verify `.env` file exists and contains your API key
- Run: `python -c "from dotenv import load_dotenv; load_dotenv(); import os; print(os.getenv('GOOGLE_API_KEY'))"`

### Virtual Environment Issues
- Ensure the virtual environment is activated
- Reinstall packages: `pip install --upgrade -r requirements.txt`

## 📝 Notes

- This project is set up for local development
- For Kaggle notebook environment, add secrets directly in Kaggle secrets manager
- The agent can be extended with custom instructions and tools

## 📄 License

Apache License 2.0 - See license headers in project files

## 🤝 Contributing

To contribute improvements:
1. Create a feature branch
2. Make your changes
3. Test thoroughly
4. Push and create a pull request

---

**Happy prompting! 🚀**

# 🚀 LangGraph Tutorials

A comprehensive collection of tutorials and examples demonstrating the power of **LangGraph** for building sophisticated AI workflows and state machines.

---

## ✨ Features

- **LangGraph Workflows**: Learn how to build complex AI workflows with state management
- **Real-World Examples**: Practical implementations including BMI calculator workflows
- **Interactive Notebooks**: Step-by-step Jupyter notebooks for hands-on learning
- **LangChain Integration**: Examples using LangChain and OpenAI for intelligent applications

---

## 📋 Project Structure

```
lg-tutorials/
├── 1_BMI_WF/
│   └── bmi_wf.ipynb          # BMI Workflow tutorial
├── 0_test_instals.ipynb       # Installation verification
├── main.py                    # Main application entry point
├── pyproject.toml             # Project dependencies
└── README.md                  # This file
```

---

## 🛠️ Installation

### Prerequisites
- Python 3.12+
- [uv](https://github.com/astral-sh/uv) package manager

### Setup

1. **Clone the repository**
   ```bash
   git clone <your-repo-url>
   cd lg-tutorials
   ```

2. **Create virtual environment (using uv)**
   ```bash
   uv venv
   source .venv/bin/activate  # On macOS/Linux
   # or
   .venv\Scripts\activate     # On Windows
   ```

3. **Install dependencies**
   ```bash
   uv pip install -e ".[dev]"
   ```

---

## 📦 Dependencies

- **langchain** ≥ 1.2.12 - LLM framework
- **langchain-community** ≥ 0.4.1 - Community integrations
- **langchain-openai** ≥ 1.1.11 - OpenAI integration
- **langgraph** ≥ 1.1.2 - Graph-based AI workflows
- **ipython** ≥ 9.11.0 - Enhanced Python shell
- **python-dotenv** ≥ 0.9.9 - Environment variable management

---

## 🎓 Tutorials

### 1. BMI Workflow (`1_BMI_WF/bmi_wf.ipynb`)
A practical tutorial demonstrating how to build a state machine workflow using LangGraph that calculates BMI and manages workflow state transitions.

**What you'll learn:**
- Creating LangGraph state graphs
- Defining workflow nodes and edges
- State management and transitions
- Workflow compilation and execution

---

## 🚀 Getting Started

1. **Verify Installation**
   ```bash
   jupyter notebook 0_test_instals.ipynb
   ```

2. **Run Tutorials**
   ```bash
   jupyter notebook 1_BMI_WF/bmi_wf.ipynb
   ```

3. **Run Main Application**
   ```bash
   python main.py
   ```

---

## 🔑 Environment Variables

Create a `.env` file in the project root for sensitive configurations:

```env
OPENAI_API_KEY=your_api_key_here
```

---

## 💡 Usage Example

```python
from langgraph.graph import StateGraph
from langchain_openai import ChatOpenAI

# Create your state graph
graph = StateGraph(state_schema=YourState)

# Add nodes and edges
graph.add_node("node_name", your_function)
graph.add_edge("start", "node_name")

# Compile and run
workflow = graph.compile()
result = workflow.invoke({"input": "data"})
```

---

## 🤝 Contributing

Contributions are welcome! Feel free to:
- Add more tutorials
- Improve existing examples
- Report issues

---

## 📝 License

This project is open source and available under the MIT License.

---

## 🙋 Questions?

For questions or support, please open an issue or refer to the [LangGraph documentation](https://langchain-ai.github.io/langgraph/).

---

**Happy Learning! 🎉**

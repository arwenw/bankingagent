# 🏦 Compliant Banking AI Agent
**An end-to-end Machine Learning System for Automated Credit Risk Assessment.**

## 🌟 Project Overview
This project features a production-ready AI agent that evaluates loan applications. It combines a **Deep Learning Neural Network** for risk prediction with a **Deterministic Rule Engine** to ensure 100% regulatory compliance.

## 🏗️ Technical Architecture
The system is built using a multi-stage pipeline:
1. **The Brain (PyTorch):** A multi-layer perceptron (MLP) trained on historical customer data to predict approval probability.
2. **The Guardrails (Logic Layer):** A configurable safety layer that overrides AI decisions if they violate institutional policies (e.g., Debt-to-Income limits).
3. **The Gateway (FastAPI):** A high-performance REST API for real-time inference.
4. **The Interface (Gradio):** A chat-based UI allowing human-in-the-loop auditing.



## 🛠️ Tech Stack
- **Language:** Python 3.12
- **Deep Learning:** PyTorch (Tensors, Linear Layers, ReLU, Sigmoid)
- **Deployment:** FastAPI, Uvicorn, Docker
- **Data Science:** Scikit-Learn (Train-Test Splitting, Scaling)
- **UI:** Gradio

## 🚀 Key Features
- **Configurable Policy:** Bank rules are decoupled from code via `bank_policy.json`, allowing for zero-downtime policy updates.
- **Explainable AI (XAI):** The agent provides natural language explanations for rejections instead of "black-box" scores.
- **Robust Validation:** Implements feature scaling and train-test splits to prevent model overfitting.

## 📈 How to Run
1. **Train the Model:** Run `train.py` to generate `banking_model.pth`.
2. **Launch API:** `uvicorn main:app --reload`
3. **Open UI:** Run `app_ui.py` to access the chat interface.

## 🛡️ Compliance & Ethics
This agent includes specific checks for bias and feature importance, ensuring that sensitive attributes are not used in the decision-making process.

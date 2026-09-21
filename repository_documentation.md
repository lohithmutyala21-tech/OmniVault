# 🏆 OmniVault: Privacy-First Local AI Analyst

**Submission for the Snapdragon® AI Lab Build & Present Challenge**

OmniVault is an offline, zero-latency document intelligence application designed for professionals handling highly sensitive data (legal, medical, financial). By leveraging quantized Large Language Models (LLMs) from the **Qualcomm AI Hub** and executing them directly on the **Snapdragon NPU**, OmniVault ensures 100% data privacy without sacrificing performance.

## 🌟 Key Features
*   **100% Local Processing:** Documents are parsed and analyzed entirely on the edge. No internet required.
*   **Snapdragon NPU Optimized:** Utilizes `onnxruntime` with `QNNExecutionProvider` to offload heavy AI tasks to the NPU, saving CPU/GPU overhead and battery life.
*   **Secure Document Parsing:** Native PDF extraction that never writes temporary files to unencrypted storage.

## 🛠️ Tech Stack
*   **Hardware Target:** Snapdragon-powered HP PCs (e.g., Snapdragon X Elite / X Plus).
*   **AI Integration:** Models compiled and optimized via [Qualcomm AI Hub](https://aihub.qualcomm.com/).
*   **Inference Engine:** ONNX Runtime (QNN Execution Provider).
*   **Frontend:** Python & Streamlit for a lightweight, native-feeling desktop UI.

## 🚀 How to Run Locally

### Prerequisites
1. A Snapdragon-powered Windows PC.
2. Python 3.10 or higher.
3. Git installed.

### Installation Steps

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/omnivault-snapdragon.git
   cd omnivault-snapdragon
   ```

2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

3. **Download Qualcomm AI Hub Model:**
   * Visit the Qualcomm AI Hub and compile a quantized Llama-3 or Mistral model for the Snapdragon NPU.
   * Export the ONNX model and place it in the project root under `models/qualcomm_quantized_llama_npu.onnx`.
   *(Note: If the model is not found, the app will gracefully fall back to a simulation mode to demonstrate the UI workflow).*

4. **Launch the Application:**
   ```bash
   streamlit run app.py
   ```

## 🧠 Why Snapdragon?
Enterprise AI currently relies heavily on cloud APIs, creating massive privacy vulnerabilities. Snapdragon's dedicated NPU enables OmniVault to shift enterprise-grade AI to the edge. This provides instantaneous responses (zero network latency), strict compliance with data privacy regulations (HIPAA, GDPR), and significantly reduced power consumption compared to running similar models on a standard x86 CPU.

---
*Created for the Qualcomm Snapdragon AI Lab Challenge - 2026.*
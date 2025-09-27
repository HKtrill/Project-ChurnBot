# 🤖 Project ChurnBot: Turning Churn Into Intelligence

**Tech Stack:** 🗄️ SQLite, 📊 Jupyter, 🐍 Python, 🔥 PyTorch, 🔧 MLOps, 💻 TypeScript, 🐳 Docker, ⚛️ React, 🌐 Node.js

**Author:** 👤 Phillip Harris

## 📖 Synopsis

ChurnBot transforms telecommunications customer retention from guesswork into precision science. It is an intelligent AI assistant built specifically for telecom churn patterns. Unlike general-purpose models, ChurnBot focuses on telecom-specific behaviors to provide accurate, actionable insights where it matters most.

## 🚨 Problem Statement: Traditional AI Approaches Miss Telecom-Specific Signals

General-purpose models often treat telecom churn like a standard classification task, potentially missing critical domain-specific signals:
- **Call patterns** and usage anomalies
- **Billing disputes** and payment behaviors  
- **Service degradation** indicators
- **Subscription anomalies** and plan changes

**Result:** High false positives/negatives → wasted marketing spend & preventable customer churn.

ChurnBot addresses these gaps with specialized telecom intelligence that general-purpose models may not fully capture.

## 🧠 Core Thesis: Specialized Smaller Models > Generic Larger Models

**Research Hypothesis:** Domain-specific smaller models consistently outperform massive general-purpose LLMs on specialized tasks like telecom churn prediction.

**Key Arguments:**
- 🎯 **Focused Architecture:** Smaller models trained on domain-specific data capture nuanced patterns that large models miss
- ⚡ **Computational Efficiency:** Specialized models achieve superior performance with dramatically lower computational overhead
- 🔍 **Signal vs. Noise:** Smaller models avoid the "curse of generalization" that causes larger models to dilute domain-specific signals
- 💡 **Feature Engineering Advantage:** Traditional ML techniques (feature engineering, ensemble methods) outperform brute-force parameter scaling

This thesis challenges the current industry assumption that "bigger is always better" by demonstrating measurable superiority in precision, recall, and resource efficiency for domain-specific applications.

## 🎯 Domain-Specific Intelligence
### Three-Stage Cascade Model
- **🧠 Artificial Neural Network** → Complex relationship modeling  
- **🚀 Gradient Boosting** → Final prediction refinement

This specialized pipeline is optimized for precision + recall in telecom churn, detecting patterns that general-purpose models may not generalize effectively.

### Pipeline Architecture
```
data_loader → preprocessor → feature_engineer → leakage_monitor → cascade_model → experiment_runner
```

## 🎯 Choose Your Experience

**⚡ Terminal Version (Light):** For telecom analysts and technical teams — fast, efficient insights through command-line interaction.

**📈 Dashboard Version (Heavy):** For telecom executives — rich visualizations and executive-ready presentations.

Both versions are specialized for telecom churn, analyzing call patterns, data usage shifts, billing disputes, and service degradation that general-purpose models may not capture. All computations run locally, keeping sensitive subscriber data on your network.

## 🔒 Privacy & Security: Local-First Philosophy

ChurnBot runs entirely on your machine with **zero cloud dependencies**:
- ✅ **No external data transfers** — sensitive subscriber data never leaves your network
- ✅ **No monthly fees** or API costs
- ✅ **Full data sovereignty** — maintain compliance and avoid regulatory penalties
- ✅ **Immediate analysis** — no network latency or downtime

Compare this to general-purpose models that may rely on cloud APIs with inherent data exposure risks.

## 📊 Benchmark Superiority

<!-- Benchmark results and performance comparisons will be published here -->
<!-- Testing against leading LLM baselines in progress -->

## 💼 Real-World Impact

**Business ROI:**
- 📉 Reduce churn-related losses through precise targeting
- 📈 Improve executive decision-making with actionable insights
- 🛡️ Maintain full data sovereignty → avoid compliance penalties
- 💰 Eliminate cloud API costs and subscription fees

**Security ROI:**
- 🔒 Complete data privacy — no external data exposure
- 📋 Regulatory compliance maintained
- 🏢 Enterprise-grade security through local execution

## ⬇️ Clone or Download

```bash
git clone https://github.com/HKtrill/Project-ChurnBot.git
cd Project-ChurnBot
npm install # or yarn
```

## 📂 Project Structure

```
prototype/
├── data/
│   ├── raw/
│   │   └── WA_Fn-UseC_-Telco-Customer-Churn.csv
│   └── test_splits/
├── churn_pipeline/   # TODO: extract churn model interface into interfaces/
│   ├── __init__.py
│   ├── data_loader.py
│   ├── preprocessor.py
│   ├── feature_engineer.py       # Optimizing
│   ├── leakage_monitor.py
│   ├── cascade_model.py          # Optimizing
│   ├── cascade_model_cpp_wrapper.py    # NEW: TODO: implement C++ model wrapper
│   └── experiment_runner.py
├── chatbot_pipeline/
│   ├── __init__.py
│   ├── user_input_handler.py          # TODO: implement input parsing and validation
│   ├── query_processor.py             # TODO: implement query formatting for each model
│   ├── churn_prediction_interface.py  # TODO: connect to Churn model pipeline interface
│   ├── security_model_interface.py    # TODO: connect to Security pipeline interface
│   ├── it_model_interface.py          # TODO: connect to IT pipeline interface
│   └── response_generator.py          # TODO: implement response formatting and templates
├── security_pipeline/
│   ├── __init__.py
│   ├── threat_data_loader.py          # TODO: implement security data loading
│   ├── threat_preprocessor.py         # TODO: implement cleaning and preprocessing
│   ├── feature_engineer.py            # TODO: implement security-specific feature extraction
│   ├── anomaly_detector.py            # TODO: implement anomaly detection model
│   ├── security_model_cpp_wrapper.py  # NEW: TODO: implement C++ security model wrapper
│   └── experiment_runner.py           # TODO: implement experimentation framework
├── it_pipeline/
│   ├── __init__.py
│   ├── it_data_loader.py              # TODO: implement IT data loading
│   ├── it_preprocessor.py             # TODO: implement IT data cleaning and preprocessing
│   ├── feature_engineer.py            # TODO: implement IT-specific feature engineering
│   ├── predictive_model.py            # TODO: implement predictive model for IT metrics/outages
│   ├── it_model_cpp_wrapper.py        # NEW: TODO: implement C++ IT model wrapper
│   └── experiment_runner.py           # TODO: implement experimentation framework
├── interfaces/
│   ├── __init__.py
│   ├── churn_model_interface.py       # TODO: place extract churn model interface here
│   ├── security_model_interface.py    # TODO: define standard methods like train(), predict(), evaluate()
│   ├── it_model_interface.py          # TODO: define standard methods like train(), predict(), evaluate()
│   └── cpp_model_interface.py         # NEW: TODO: define standard C++ model interface
├── utils/
│   ├── utils.py                       # TODO: add additional shared utility functions
│   └── cpp_utils.py                   # NEW: TODO: add C++ integration utilities
├── notebooks/
│   ├── churn_pipeline_lab.ipynb       # TODO: Clean up
│   ├── chatbot_pipeline_lab.ipynb     # TODO: set up lab for multi-model chatbot experimentation
│   ├── security_pipeline_lab.ipynb    # TODO: set up lab for security experimentation
│   ├── it_pipeline_lab.ipynb          # TODO: set up lab for IT experimentation
│   └── cpp_benchmarking_lab.ipynb     # NEW: TODO: create C++ vs Python benchmarking notebook
├── cpp_models/                        # NEW: C++ optimized models directory
│   ├── shared_cpp/                    # NEW: Common C++ optimizations
│   │   ├── include/
│   │   │   ├── optimization_utils.h    # TODO: implement branch & bound, early termination
│   │   │   ├── data_structures.h       # TODO: implement cache-friendly containers
│   │   │   ├── memory_manager.h        # TODO: implement custom allocators
│   │   │   └── common_types.h          # TODO: define common data types
│   │   └── src/
│   │       ├── optimization_utils.cpp  # TODO: implement CS theory optimizations
│   │       ├── data_structures.cpp     # TODO: implement optimized data layouts
│   │       └── memory_manager.cpp      # TODO: implement memory management
│   ├── churn_pipeline_cpp/            # NEW: Churn C++ models
│   │   ├── include/
│   │   │   ├── churn_cascade.h         # TODO: implement main cascade interface
│   │   │   ├── random_forest.h         # TODO: implement custom RF with optimizations
│   │   │   ├── neural_network.h        # TODO: implement custom ANN with sparse matrices
│   │   │   ├── recurrent_network.h     # TODO: implement custom RNN with early termination
│   │   │   └── telecom_features.h      # TODO: define telecom-specific data structures
│   │   ├── src/
│   │   │   ├── churn_cascade.cpp       # TODO: implement cascade orchestrator
│   │   │   ├── random_forest.cpp       # TODO: implement RF with branch & bound
│   │   │   ├── neural_network.cpp      # TODO: implement ANN with SIMD optimizations
│   │   │   ├── recurrent_network.cpp   # TODO: implement RNN with memory optimization
│   │   │   └── telecom_features.cpp    # TODO: implement feature processing
│   │   ├── bindings/
│   │   │   ├── python_bindings.cpp     # TODO: implement pybind11 interface
│   │   │   └── __init__.py             # TODO: set up Python module
│   │   ├── tests/
│   │   │   ├── test_rf.cpp             # TODO: implement unit tests for RF
│   │   │   ├── test_ann.cpp            # TODO: implement unit tests for ANN
│   │   │   └── test_cascade.cpp        # TODO: implement integration tests
│   │   └── CMakeLists.txt              # TODO: set up build configuration
│   ├── security_pipeline_cpp/         # NEW: Security C++ models
│   │   ├── include/
│   │   │   ├── security_cascade.h      # TODO: implement security model interface
│   │   │   ├── anomaly_detector.h      # TODO: implement anomaly detection algorithms
│   │   │   ├── bot_detector.h          # TODO: implement bot detection models
│   │   │   └── threat_classifier.h     # TODO: implement threat classification
│   │   ├── src/
│   │   │   ├── security_cascade.cpp    # TODO: implement security pipeline orchestrator
│   │   │   ├── anomaly_detector.cpp    # TODO: implement real-time anomaly detection
│   │   │   ├── bot_detector.cpp        # TODO: implement bot detection algorithms
│   │   │   └── threat_classifier.cpp   # TODO: implement threat classification
│   │   ├── bindings/
│   │   │   ├── python_bindings.cpp     # TODO: implement pybind11 security interface
│   │   │   └── __init__.py             # TODO: set up security Python module
│   │   ├── tests/
│   │   │   ├── test_anomaly.cpp        # TODO: implement anomaly detection tests
│   │   │   └── test_bot_detection.cpp  # TODO: implement bot detection tests
│   │   └── CMakeLists.txt              # TODO: set up security build configuration
│   ├── it_pipeline_cpp/               # NEW: IT C++ models
│   │   ├── include/
│   │   │   ├── it_cascade.h            # TODO: implement IT model interface
│   │   │   ├── outage_predictor.h      # TODO: implement outage prediction
│   │   │   ├── performance_monitor.h   # TODO: implement performance monitoring
│   │   │   └── servicenow_interface.h  # TODO: implement ServiceNow integration
│   │   ├── src/
│   │   │   ├── it_cascade.cpp          # TODO: implement IT pipeline orchestrator
│   │   │   ├── outage_predictor.cpp    # TODO: implement predictive maintenance
│   │   │   ├── performance_monitor.cpp # TODO: implement system performance analysis
│   │   │   └── servicenow_interface.cpp # TODO: implement ServiceNow API integration
│   │   ├── bindings/
│   │   │   ├── python_bindings.cpp     # TODO: implement pybind11 IT interface
│   │   │   └── __init__.py             # TODO: set up IT Python module
│   │   ├── tests/
│   │   │   ├── test_outage_prediction.cpp # TODO: implement outage prediction tests
│   │   │   └── test_performance.cpp    # TODO: implement performance monitoring tests
│   │   └── CMakeLists.txt              # TODO: set up IT build configuration
│   ├── benchmarks/                    # NEW: Performance benchmarking
│   │   ├── churn_benchmark.cpp         # TODO: implement churn model benchmarking
│   │   ├── security_benchmark.cpp      # TODO: implement security model benchmarking
│   │   ├── it_benchmark.cpp            # TODO: implement IT model benchmarking
│   │   ├── memory_profiling.cpp        # TODO: implement memory usage profiling
│   │   └── compare_all_pipelines.cpp   # TODO: implement comprehensive benchmarking
│   ├── scripts/                       # NEW: Build and deployment scripts
│   │   ├── build_all.sh               # TODO: create master build script
│   │   ├── install_dependencies.sh    # TODO: create dependency installation script
│   │   ├── run_benchmarks.sh          # TODO: create benchmark execution script
│   │   └── generate_bindings.sh       # TODO: create Python binding generation script
│   └── CMakeLists.txt                 # TODO: set up master build configuration
├── BasePipeline.py                    # TODO: implement base class for pipelines
├── requirements.txt                   # TODO: add pybind11, cmake, and other C++ dependencies
└── README.md
```

## 📋 Requirements

### System Requirements
- Python 3.8+
- Node.js 16+
- 8GB RAM minimum (16GB recommended)
- 2GB free disk space

### Python Dependencies
```bash
torch>=1.9.0
scikit-learn>=1.0.0
pandas>=1.3.0
numpy>=1.21.0
jupyter>=1.0.0
fastapi>=0.68.0
uvicorn>=0.15.0
```

### Frontend Dependencies
```bash
react>=18.0.0
typescript>=4.4.0
@types/react>=18.0.0
@types/node>=16.0.0
```

## ⚙️ Installation & Setup

### Backend Setup:
```bash
cd backend
pip install -r requirements.txt
uvicorn app.main:app --reload
```

### Frontend Setup:
```bash
cd ../frontend
npm install
npm start
```

### Terminal Version:
```bash
python BasePipeline.py --mode terminal
```

### Dashboard Version:
```bash
python BasePipeline.py --mode dashboard
# Then navigate to http://localhost:3000
```

## 🧪 Testing

<!-- Testing framework and benchmarks coming soon -->

## 🧪 Benchmark Testing

<!-- Automated benchmark comparison against LLM baselines -->
<!-- Results and performance metrics will be published here -->

## 🏗️ Architecture

ChurnBot demonstrates production-ready MLOps with careful handling of sensitive data:

**Core Components:**
- **Data Pipeline:** Secure local processing with leakage monitoring
- **Model Pipeline:** Three-stage cascade for optimal precision/recall
- **Interface Pipeline:** Dual-mode accessibility (terminal + dashboard)
- **Experiment Pipeline:** Reproducible benchmarking and validation

**Design Principles:**
- 🛡️ Privacy-first architecture
- 🎯 Domain-specific optimization  
- ⚡ Performance-optimized inference
- 🔄 Reproducible experiments

## ❓ Why ChurnBot Matters

ChurnBot isn't just another AI tool — it's a **research-backed, production-ready solution** solving real-world telecom challenges:

- 📊 **Evidence-based:** Clear, reproducible benchmarks over marketing hype
- 🎓 **Research-grade:** Publication-ready methodology and results
- 🏭 **Production-ready:** Modular, scalable architecture for enterprise deployment
- 🔐 **Security-first:** Local execution addresses real enterprise concerns

This positions ChurnBot as a standout project in a market flooded with generic AI applications.

## 📞 Support

For questions or issues, please open a GitHub issue or contact the maintainer.

---

**ChurnBot:** Where telecom domain expertise meets cutting-edge ML — turning customer churn from reactive guesswork into proactive intelligence.

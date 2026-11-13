# Infinity-LiteOCR-Millions-Images
Develop Khmer OCR train with 16 millions images

A high-throughput, lightweight optical character recognition (OCR) pipeline and FastAPI web service designed and optimized to handle massive training corpora and ultra-fast inference without heavy framework dependencies (e.g., bypassing heavy `torchvision` overhead).

---

## Features

- **High-Throughput Inference API**: Powered by FastAPI with multiple model endpoint versions (`/recognize` and `/recognize2`) for flexible deployment and version switching.
- **Lightweight & Dependency-Optimized**: Streamlined model inference pipeline utilizing pure PIL and optimized tensor backloads for minimal container footprints.
- **Massive Scale Training Ground**: Built on top of extensive multi-million image datasets and rigorous domain adaptation pipelines.
- **Modern Web Demo UI**: Includes an out-of-the-box browser interface (`API/index.html`) with clipboard paste support (`Ctrl+V`), drag-and-drop zones, latency tracking, and dark-mode styling built with Tailwind CSS.

---

## Project Structure

```text
├── API/
│   ├── index.html       # Sleek Tailwind-powered OCR web demo client
│   └── main.py          # FastAPI server handling /recognize & /recognize2 endpoints
├── inference/           # Core inference engines and model runners
├── model/               # Model weights and configuration structures
├── makefile             # Automation shortcuts for building and running services
└── README.md
```

---

## Quick Start

### 1. Prerequisites
Ensure you have Python installed along with your preferred virtual environment manager (e.g., Conda or venv).

### 2. Installation & Dependencies
Clone the repository and install the required dependencies:

```bash
git clone https://github.com/SoyVitouPro/Infinity-LiteOCR-Millions-Images.git
cd Infinity-LiteOCR-Millions-Images
pip install -r requirements.txt  # Or use your project's poetry/conda setup
```

### 3. Running the API Server
Start the FastAPI server locally:

```bash
cd API
uvicorn main:app --reload --port 5348
```

### 4. Accessing the Web Demo
You can launch or host the included interactive UI (`API/index.html`) locally to test images via file pickers or direct clipboard pasting (`Ctrl+V`).

---

## Endpoints

- **`POST /recognize`**: Version 1 baseline OCR inference pipeline.
- **`POST /recognize2`**: Optimized version 2 inference pipeline with enhanced multi-model routing and improved latency.

---

## License

This project is licensed under the terms specified in the LICENSE file.
"""

with open("README.md", "w", encoding="utf-8") as f:
    f.write(readme_content)

print("README.md generated successfully.")

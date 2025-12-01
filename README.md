
<div align="center">
  <img src="klepto_small.jpg" alt="Klepto2 Logo" width="400" />
  <h1>Klepto</h1>
  <p><strong>KLEPTO - A Docker Image Secrets Scanner</strong></p>
  <p>
    <a href="#features">Features</a> •
    <a href="#installation">Installation</a> •
    <a href="#usage">Usage</a> •
    <a href="#output">Output</a> •
    <a href="#contributing">Contributing</a>
  </p>
</div>


Klepto is a powerful tool for scanning Docker images to detect secrets and vulnerabilities. It searches public Docker Hub repositories for images matching your criteria and analyzes them using advanced detectors like **trufflehog** and **gitleaks**.

---

## ✨ Features
- Search Docker Hub for images by keyword
- Extract and analyze images for secrets
- Supports multiple detectors for comprehensive scanning
- Customizable detection rules

---

## 📦 Installation
Tested on:
- Debian Bookworm
- WSL Ubuntu 24.04.3 LTS

```bash
sudo apt install git curl jq docker.io python3 docker-registry docker-compose
git clone https://github.com/telekom-security/klepto.git
```

---

## 🚀 Usage
```bash
sudo ./search.sh SEARCHTERM
```

Edit configuration:
- `script.sh` → Set your API key
- `parser.py` → Adjust `desired_detector_type` and `undesired_terms`

---

## 🖼 Workflow

<div align="center">
  <img src="workflow.png" alt="Klepto Workflow" width="300" />
</div>

Steps:
1. Search Docker Hub
2. Pull Image
3. Extract Layers
4. Scan for Secrets
5. Generate Report
---

## 📌 Roadmap
- Add support for private registries
- Implement parallel scanning
- Enhance reporting with HTML output

---

## 🤝 Contributing
Feel free to open issues or submit pull requests.

---

## 👏 Authors
Thanks to **Maximilian Gutowski** and **Jakub Sucharkiewicz**

---

## 📜 License
GPL 3.0

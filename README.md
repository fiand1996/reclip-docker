# reclip-docker

Automated GitHub Actions workflow to build and publish multi-architecture Docker images for [averygan/reclip](https://github.com/averygan/reclip) to GitHub Container Registry (GHCR).

> **Note:** This repository does not contain application code or a local `Dockerfile`. It automatically fetches the upstream repository, builds the Docker image for **`linux/amd64`** and **`linux/arm64`**, and pushes it to GHCR.

---

## 🚀 Quick Start (Kubernetes / Docker)

### Pull the Image

```bash
docker pull ghcr.io/fiand1996/reclip-docker:latest

```

### Run with Docker

```bash
docker run -d \
  -p 8899:8899 \
  -v reclip-downloads:/app/downloads \
  --name reclip \
  --restart unless-stopped \
  ghcr.io/fiand1996/reclip-docker:latest

```

Access the application at `http://localhost:8899`.

---

## ⚙️ How It Works

- **Manual Trigger:** Can be manually triggered anytime via the **Actions** tab.
- **Scheduled Trigger:** Automatically rebuilds every 14 days to keep `yt-dlp` and base dependencies fresh.

---

## 📜 Credits & Acknowledgments

- **[ReClip](https://github.com/averygan/reclip)** by Avery Gan – The original open-source application.

---

## 📄 License

[MIT](https://www.google.com/search?q=LICENSE)

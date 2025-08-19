# .devcontainer/Dockerfile
FROM python:3.12-slim

# ── OS パッケージ ──
RUN apt-get update && apt-get install -y \
        build-essential curl git && \
    rm -rf /var/lib/apt/lists/*

# ── Python パッケージ ──
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# デフォルトの作業ディレクトリ
WORKDIR /workspace
ARG PY_VERSION
FROM python:${PY_VERSION:-3.9-slim}

LABEL maintainer="Osiozekhai Aliu"

RUN apt update && apt full-upgrade -y 
RUN apt install -y \
    git \
    build-essential \
    curl \
    nano \
    libssl-dev \
    bash \
    gcc \
    g++ \
    musl-dev \
    python3-dev \
    libffi-dev \
    bash-completion \
    pkg-config

RUN rm -rf /var/lib/apt/lists/*

# Install Rust using rustup
RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y

# Add the cargo bin directory to the PATH
ENV PATH="/root/.cargo/bin:${PATH}"

RUN pip install --upgrade pip
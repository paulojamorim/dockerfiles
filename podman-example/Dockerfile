FROM pytorch/pytorch:2.0.0-cuda11.7-cudnn8-runtime

RUN apt-get update && apt-get install -yq --no-install-recommends \
    autotools-dev \
    build-essential \
    ca-certificates \
    cmake \
    make \
    git \
    wget \
    unzip \
    vim \
    software-properties-common \
    x11-apps \
    autoconf \
    bison \
    curl \
    flex \
    g++ \
    gcc \
    pkg-config \
    zlib1g-dev \
    python3.7 \
    python3.7-dev \
    libpython3.7 \
    python-pip \
    libpthread-stubs0-dev \
    libblas-dev liblapack-dev gfortran \
    llvm-4.0-dev  \
    libpng-dev libfontconfig-dev libxrender-dev libncurses5-dev \
    libx11-dev libxt-dev \
    freeglut3 freeglut3-dev \
    libxrender1 libfontconfig1 && \
    rm -rf /var/lib/apt/lists/* 

RUN pip install --no-cache-dir future opencv-python numpy torch \
        typing-extensions scipy scikit-image scikit-learn cython \
        tqdm matplotlib torchinfo

USER ${USER}
WORKDIR /code
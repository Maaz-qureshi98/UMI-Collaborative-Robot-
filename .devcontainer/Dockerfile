FROM chicheng/orb_slam3:latest

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    python3-pip ffmpeg libglib2.0-0 \
    libsm6 libxext6 libxrender-dev \
    && rm -rf /var/lib/apt/lists/*

WORKDIR /workspace

COPY conda_environment.yaml .
RUN pip3 install zarr numpy opencv-python \
    torch torchvision torchaudio \
    diffusers accelerate \
    hydra-core wandb \
    pymunk pygame \
    dill==0.3.5.1


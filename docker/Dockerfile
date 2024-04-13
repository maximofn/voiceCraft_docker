FROM nvcr.io/nvidia/cuda:11.8.0-cudnn8-devel-ubuntu22.04

RUN apt-get update \
    && apt-get install -y git git-lfs python3 python3-pip \
    && apt-get install -y libgl1-mesa-glx libglib2.0-0 \
    && curl -s https://packagecloud.io/install/repositories/github/git-lfs/script.deb.sh | bash \
    && git lfs install \
    && rm cuda-keyring_1.0-1_all.deb \
    && ln -s /usr/bin/python3 /usr/bin/python \
    && rm -rf /var/lib/apt/lists/*

RUN apt-get update \
    && apt-get install -y git git-lfs --no-install-recommends espeak libespeak-dev ffmpeg \
    && rm -rf /var/lib/apt/lists/*

# RUN pip3 install --no-cache-dir torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118 \
RUN git clone --depth 1 https://huggingface.co/spaces/pyp1/VoiceCraft_gradio \
    && cd VoiceCraft_gradio && cp requirements.txt requirements_no_aenas.txt \
    && sed -i '/aeneas/d' requirements_no_aenas.txt \
    && pip3 install --no-cache-dir -r requirements_no_aenas.txt \
    && pip3 install --no-cache-dir -r requirements.txt
    # && pip3 install --no-cache-dir gradio==3.23.0

WORKDIR /VoiceCraft_gradio
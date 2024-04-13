# Voice Craft docker

Dockerization of the [Hugging Face Voice Craft Space](https://huggingface.co/spaces/pyp1/VoiceCraft_gradio)

 * Repository: [https://github.com/coqui-ai/TTS](https://github.com/coqui-ai/TTS)
 * Model card: [https://huggingface.co/coqui/XTTS-v2](https://huggingface.co/coqui/XTTS-v2)
 * Space: [https://huggingface.co/spaces/pyp1/VoiceCraft_gradio](https://huggingface.co/spaces/pyp1/VoiceCraft_gradio)

## Requisites

[Docker](https://docs.docker.com/desktop/) and [nvidia container toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html) must be installed.

## Usage

### Download the image from the Docker Hub

You can download the image and run it

```bash
docker pull maximofn/voice_craft:latest
./run_app.sh
```

### Build the image

Or you can build the image and run it

```bash
./build_docker_image.sh
./run_app.sh
```
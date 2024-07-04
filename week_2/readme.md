

# Intro

1. Activate Saturn Cloud Account
2. Setup SSH key
3. Create a resource
    - pip install -U transformers accelerate bitsandbytes sentencepiece
4. Connect to github repo
    4.1 Config Env Variables (HF token)
5. Start Server
6. Run 'nvidisa-smi' to check the availability of GPU

# Ollama Setup

## From CLI

curl -fsSL https://ollama.com/install.sh | sh
ollama start
ollama run phi3

## Docker

docker run -it \
    -v ollama:/root/.ollama \
    -p 11434:11434 \
    --name ollama \
    ollama/ollama

# Docker Compose

cd week_2/docker_elasticsearch_ollama
docker-compose up

## AI Project
A Docker Compose setup for Open WebUI, Ollama and Fabric services with GPU support.

- **webui**: This is the Web UI component of the project. It is available on port 3000 of the host and depends on the Ollama service.
- **ollama**: This is the Ollama service, which is required by the webui.

## Setup

1. Clone the project with Git `git clone https://github.com/aliuosio/ai.git`
2. Navigate into the project directory `cd ai`
3. copy `.env.temp` to `.env`
3. Run `docker compose up -d` to create and start your environment.


## Ollama Setup

	docker compose exec ollama ollama pull llama3.2:3b

>  (llama3.2:3b is the default set in .env.temp)
> find more models: `https://ollama.com/library`


## Usage
The Web UI is accessible at 
	
	http://localhost:3000


## Fabric Usage

    docker compose exec fabric bash

Please note that this service is configured for GPU acceleration and requires NVIDIA drivers working with docker
## NVIDIA GPU Setup on debian bassed Linux

To enable Docker to use NVIDIA drivers on a Linux system, follow these steps:

1. Install the NVIDIA Container Toolkit:

	https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html

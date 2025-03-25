# README.md

This repo contains a sample RAG system using hatchet to deal with the batch processing and execution. 

This code will:

1. reads a website and parses the text content
2. reasons about what information is most relevant to the user request
3. generates a response for the user

## Components

This repo contains: 

* Frontend react application
* FastAPI that will act as our edge service
* Hatchet worker 

## Requirements

In order to execute this code you need to have:

* poetry
* npm
* Hatchet
* docker
* docker-compose
* Ollama

## Setup

Before building and running the application make sure to start docker and create a API token, 

Create a `.venv` file based on `.venv-example` including your generated token 


## Build

In order to install required packages run the following command

```sh
poetry install
```

This will install the required packages

## Run

Start the API with 

```sh
poetry run api
```

In a different Terminal start the hatchet worker with

```sh
poetry run hatchet
```

In another terminal go to the frontend folder and start with

```sh
npm start
```

You can now use <http://localhost:3000> and test the query and <http://localhost:8080> to view the execution status of the workflow.

## References

This application is based on the tutorial <https://docs.hatchet.run/home/tutorials/fastapi-react/project-setup> with minor changes to use ollama.

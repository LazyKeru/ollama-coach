# Run via docker: 

## Using CPU
```
docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

## Using GPU
```
docker run -d --gpus=all -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```
**install the NVIDIA Container Toolkit to use the GPU**

It is pretty impressing seeing the difference of speed when the ai uses the GPU compared to only using the CPU.

# Install Modelfile

```
docker cp ./Modelfile ollama:/home/Modelfile
docker exec -it ollama ollama create noel -f /home/Modelfile
```

# Run Modelfile

```
docker exec -it ollama ollama run noel
```
docker pull ghcr.io/toeverything/affine-self-hosted:alpha-abbey-wood

docker run -it --name affine -d -v {$PWD}/docker_examples/docker_volumes/affine/app:/app/data -p 3000:3000 ghcr.io/toeverything/affine-self-hosted:latest
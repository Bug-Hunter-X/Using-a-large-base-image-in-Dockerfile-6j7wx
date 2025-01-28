# Dockerfile Bug: Using a Large Base Image

This repository demonstrates a common but easily avoidable issue in Dockerfiles: using overly large base images.  The provided `Dockerfile` uses `ubuntu:latest`, which is a significant size and includes many unnecessary packages.

The `DockerfileSolution.txt` file shows how to mitigate this by utilizing a slimmer base image, resulting in a smaller and more efficient Docker image.  This is important for reducing image size, faster downloads, and overall improved performance.

This example is simple but highlights a common best practice: choose the smallest, most appropriate base image for your needs.

## How to reproduce

1. Clone this repository.
2. Build the Docker image using `docker build -t large-image .`
3. Examine the image size using `docker images`.
4. Build the improved Docker image from `DockerfileSolution.txt` (you will need to rename it to `Dockerfile`).
5. Compare the size of the two images.
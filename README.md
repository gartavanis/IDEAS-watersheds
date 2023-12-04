# Instructions for getting setup with Docker for the IDEAS-watersheds workshop 

**Note:** *: the Docker image might take a while to download, so make sure you do these steps ahead of the workshop.*

  1.	Go to [Docker](https://www.docker.com/products/docker-desktop/) and download Docker Desktop. Make sure you download the correct version based on your computer’s architecture. Follow the instructions to install Docker Desktop.
  2.	Start Docker Desktop and make sure it’s running while you do the next steps. You might need to create an account and sign in if you don’t already have one.
  3.	Start a new terminal session.
  4.	Pull the parflow/subsettools image from DockerHub. Choose the correct version based on your computer’s architecture:
     - For the x86_64/amd64 architecture type:
    	```bash
      docker pull george135/subsettools_amd64
      ```
     - For the arm64 architecture type:
     ```bash
     docker pull george135/subsettools_arm64
     ```
  5. Once the image has finished downloading, you can run the image with:
     ```bash
     docker run -dp 8888:8888 george135/subsettools_arm64:latest start-notebook.sh --NotebookApp.token=''
     ```
  7. 


# Instructions for getting setup for the IDEAS-watersheds workshop 

**Note:** *The Docker image might take a while to download, so make sure you do these steps ahead of the workshop.*

  1.  Follow the instructions [here](https://hydroframesubsettools.readthedocs.io/en/latest/getting_started.html#creating-a-hydrogen-hydroframe-hydrodata-account-and-registering-a-pin) to create a Hydrogen account.
  2.	Go to [Docker](https://www.docker.com/products/docker-desktop/) and download Docker Desktop. Make sure you download the correct version based on your computer’s operating system and architecture. Follow the instructions to install Docker Desktop. ![alt text](https://github.com/gartavanis/IDEAS-watersheds/blob/main/Docker.png)
  3.	Launch Docker Desktop. The application should be running while you do the next steps. (You might need to create a Docker account and sign in if you don’t already have one.)
  4.	Start a new terminal session to type the commands in steps 4 and 5:
  5.	Pull the parflow/subsettools image from DockerHub. Choose the correct version based on your computer’s architecture:
- For the x86_64/amd64 architecture:
```bash
docker pull george135/subsettools_amd64
```
- For the arm64 architecture:
```bash
docker pull george135/subsettools_arm64
```
**NOTE:** *If your Docker is running out of space, you might need to use [docker system prune](https://docs.docker.com/engine/reference/commandline/system_prune/) with the appropriate options to clear out old containers and make space for the new one.*

  5. Once the image has finished downloading, you can run the container with:
- For the x86_64/amd64 architecture:
```bash
docker run -dp 8888:8888 george135/subsettools_amd64:latest start-notebook.sh --NotebookApp.token=''
```
- For the arm64 architecture:
```bash
docker run -dp 8888:8888 george135/subsettools_arm64:latest start-notebook.sh --NotebookApp.token=''
```
  6. Use a browser to navigate to your [JupyterLab container](http://localhost:8888/lab?) or use the link that will appear next to your container on the Docker Desktop application: ![alt text](https://github.com/gartavanis/IDEAS-watersheds/blob/main/Docker2.png)
  7. You should see a JupyterLab environment like this: ![alt text](https://github.com/gartavanis/IDEAS-watersheds/blob/main/Docker3.png)
  8. Click on the Terminal application to start a terminal session *inside* the container.
  9. Clone the GitHub repository that contains the example workflows for `subsettools and `hf_hydrodata`:
```bash
git clone https://github.com/hydroframe/subsettools-binder.git
```
 10. Navigate to `subsettools-binder` -> `subsettools` folder and click on the `definte_subset.ipynb` notebook. ![alt text](https://github.com/gartavanis/IDEAS-watersheds/blob/main/Docker4.png)
 11. Make sure the notebook runs successfully without errors. **You will need to provide your Hydrogen email and pin in the first code cell of the notebook.**
 12. Congratulations, you're all setup for Sunday!
 13. The documentation for [subsettools](https://hydroframesubsettools.readthedocs.io/en/latest/index.html) and [hf_hydrodata](https://hf-hydrodata.readthedocs.io/en/latest/) is hosted at Read The Docs

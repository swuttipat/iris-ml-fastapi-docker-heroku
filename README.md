> Written with [StackEdit](https://stackedit.io/).

#### Prerequisites
Before we begin, ensure that you have the following installed on your system:

1.  Python 3.6 or higher
2.  FastAPI
3.  Uvicorn
4.  Docker
5.  Heroku CLI
6.  Git
  
Here's a concise set of instructions for deploying a machine learning model using FastAPI, Docker, and Heroku. In this guide, we assume that you have developed and saved the model using the provided kaggle notebook.

1.  Develop and save the model with this Kaggle:

    -   Open Kaggle: [Kaggle Notebook](https://www.kaggle.com/code/wuttipats/irisdataset-classification-model-naivebayes)
2.  Create a Docker container:
    
    -   Build the Docker image: `docker build -t app-name .`
    -   Run the Docker container: `docker run -p 80:80 app-name`
3.  Create a Git repo:
    
    -   If you clone this repo, this step is not needed. Alternatively, you can delete the existing git repo with `rm -rf .git` and start with a new one:
        -   `git init`
        -   `git add .`
        -   `git commit -m "initial commit"`
        -   `git branch -M main`
4.  Create a Heroku project:
    
    -   Log in to Heroku: `heroku login`
    -   Create a new Heroku app: `heroku create your-app-name`
    -   Add the Heroku remote to your Git repo: `heroku git:remote your-app-name`
    -   Set the Heroku stack to use the container: `heroku stack:set container`
    -   Push your changes to Heroku: `git push heroku main`

With these instructions, you should now have a deployed machine learning model using FastAPI, Docker, and Heroku.

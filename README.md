# Google Cloud Function
## starting a project 

To start a new project in google cloud, we can go to the firebase console 
(https://console.firebase.google.com) or create it from Google cloud Plateform console. 

## Creating a virtual environment 
Firstly, we have to install 'python3-venv' with the following command:
```
python -m venv cloud-function 
```
here in this example, I have given the name "cloud-function" to my virtual environment.

Secondly, we need to activate our virtual environment that we have just created by executing
the following command: 

````
.\cloud-function\Scripts\activate
````

In order to add new packages to our virtual environment, we have created a file called 
"requirements.txt" and we executed the following the command: 
````
pip install -r requirements.txt
````
##Deploying our function on Cloud functions
After having installed Google Cloud SDK,we have firstly to set our project ID with the following command :
````
gcloud config set project [YOUR_PROJECT_ID]
````
Then, we deploy our function with this command 
````
gcloud functions deploy [FUNCTION_NAME] --runtime python39 --triger-http
````
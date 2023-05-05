# lotr-demo
Lord of the Rings - Fellowship of the Ring Demo

## Setup
Under the setup folder:  
1. pip install -r ./setup/requirements.txt
2. copy .env_sample to .env
3. Update .env file with API keys
4. Run the notebook to load the data into the Pinecone index  
5. Deploy the Streamlit app 

---  

## Streamlit deployment

To deploy a Streamlit app on Streamlit Cloud with secrets, follow these steps:

1. Develop your Streamlit app locally: Create your Streamlit app using Python and the Streamlit library. Ensure it runs without issues on your local machine.

2. Set up secrets locally: Create a .env file in your project directory to store your secrets, and use the python-dotenv library to load them in your app. Add the .env file to your .gitignore to prevent your secrets from being uploaded to GitHub.

3. Create a GitHub repository: Create a new repository on GitHub to store your Streamlit app's code. Commit and push your changes, including the app code and a requirements.txt file with all the necessary dependencies.

4. Sign up and log in to Streamlit Cloud: Go to https://streamlit.io/cloud, sign up for a free account, and log in.

5. Deploy your app: Click "New app" in the top right corner of the Streamlit Cloud dashboard. Select your GitHub repository and branch containing your Streamlit app.

6. Configure the app: Streamlit Cloud should automatically detect your app's main file (either app.py or streamlit_app.py). Configure other settings as needed based on your Streamlit Cloud plan.

7. Add secrets to Streamlit Cloud: Navigate to the "Secrets" tab in your app's settings on Streamlit Cloud. Add your secrets as key-value pairs, using the same keys as in your local .env file.

8. Update your app code: In your Streamlit app code, replace the usage of python-dotenv with the os.environ dictionary to access secrets. For example:

```
import os

MY_SECRET_KEY = os.environ['MY_SECRET_KEY']
DATABASE_URL = os.environ['DATABASE_URL']
```

9. Commit and push code changes: Commit and push the updated app code to your GitHub repository.

10. Deploy and view your app: Click "Deploy" to start the deployment process. Streamlit Cloud will install the necessary dependencies and launch your app. Once deployed, click on the unique URL on your app's page in the Streamlit Cloud dashboard to view your app in your web browser.

11. Streamlit Cloud will automatically redeploy your app whenever you push changes to the GitHub repository.







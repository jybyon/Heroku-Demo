# Heroku-Demo

- in model.py:
    - clean up data, use the data to train chosen model, and then use PICKLE to save the model as model.pkl
 
- in app.py:
    - use FLASK to create our web app (specify what occurs for all routes i.e. depending on the exact url input, different functions will be run)

if we run app.py in our anaconda terminal ($ python app.py), our web app will run LOCALLY
    - can use the IP address shown in output - go to the address in your web browser to see your app
    - this is useful for checking that your code is working as intended, but note that this is only locally accessible


- Procfile
    - in this file we specify which file needs to be executed first
    - the code might look like this: ($ web: gunicorn app: my_flask_app_name)
          - note that the flask app name isn't referring the name of the app.py file, but rather the name of the Flask app object created in app.py

- requirements.text
    - must specify all libraries that need to be installed in our environment when deploying. This includes package names as well as their specific versions
 
### with all these files committed to your github repo, it is possible to use a PaaS such as Heroku to do the rest
    - if we connect our github repo to Heroku and choose to deploy, it will provide a URL to our web app that is now running and available online

    - to check the logs for our app, on command prompt run       $ heroku login
         this will make us log in to heroku on the web browse, after which we return to command prompt to now run    $ heroku logs --app our_heroku_deployed_app_name 

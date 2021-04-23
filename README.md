# IPL Score Prediction

## Indian Premier League 2008-2019

### Ball-by-ball Indian Premier League (IPL) cricket dataset

##### Context
Indian Premier League (IPL) is a Twenty20 cricket format league in India. It is usually played in April and May every year. As of 2019, the title sponsor of the game is Vivo. The league was founded by Board of Control for Cricket India (BCCI) in 2008.

##### Content
Data till Season 11 (2008 - 2019)
matches.csv - Match by match data
deliveries.csv - Ball by ball data

##### Acknowledgements
Data source from 2008-2017 - CricSheet.org and Manas - Kaggle
Data source for 2018-2019 - IPL T20 - Official website

##### Inspiration
Draw analysis, player/team performance, apply and learn statistical methods on real da

## Aim 

Predict the Score 

# To deploy on Heroku you need two things:
+ requirements.txt file
+ Procfile

**How to Get the requirements.txt file**

# Method 1: using pip
pip freeze > requirements.txt

# Method 2: using pipreqs (recommended)
+ First install pipreqs
pip install pipreqs
+ Second use pipreqs to get the requirements.txt file of any project
pipreqs yourmlapp_folder

**For the  procfile can I simply use: web: gunicorn app:app?**
+ What to Put inside the Procfile
+ web: gunicorn app:app

**should the static and templates folder remain the same for deployment as the one we prepared during Productionization?**
+ Yes,  you will have to push them too to github

**Procfile**
For Heroku you need to say which is the first file bascially you need to execute. 
web:gunicorn app: app
Which is your file of Flask you want to run first? app.py

**setup.sh**
Script program for bash that helps us to execute code with respect to requirement.txt. 
It helps us to setup environment for streamlit library. 

**Flasgger**
This will help us to create the UI part in a much feasible and easy way. It won't be that decorative but it would be a good front end web app. In Flasgger, Swagger will automatically generate the frontend UI part. 

In this repository, we have performed implementation of end To end kaggle machine learning project for car price prediction with deployment.


### 🟢 For EDA + Model Building, please refer to: IPL PYTHON.ipynb
### 🟢 For Model Deployment, please refer to app.py


### 🔵 Creating the flask API

```
app = Flask("__name__")
```

The loadPage method calls our home.html.
```
@app.route("/")
def loadPage():
	return render_template('home.html', query="")
```

The predict method is our POST method, which is basically called when we pass all the inputs from our front end and click SUBMIT.
```
@app.route("/", methods=['POST'])
def predict():
```
  
The run() method of Flask class runs the application on the local development server.
```
app.run()
```


Yay, our model is ready, let’s test our bot.
The above given Python script is executed from Python shell.

Go to Anaconda Prompt, and run the below query.
```
python app.py
```


Below message in Python shell is seen, which indicates that our App is now hosted at http://127.0.0.1:5000/ or localhost:5000
```
* Running on http://127.0.0.1:5000/ (Press CTRL+C to quit)
```


HERE'S HOW OUR FRONTEND LOOKS LIKE:

<img src="frontend.PNG" alt=" " style="width: 600px;">

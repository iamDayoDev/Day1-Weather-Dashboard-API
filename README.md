## DAY 1: DevOps Challenge - WEATHER-DASHBOARD

## REQUIRED TECHNOLOGIES:

- Python
- AWS S3 Setup
- API fetching and processing

In this project, Openweather API was utilized and this was fetched using python. The result was then parsed into json format before being stored inside an S3 bucket.

## STEPS INVOLVED:

### 1. Create openweather account

Proceed to openweather website and create an account. After this, create an API key which will be used in fetching the weather information across different regions.

### 2. Setup your work environment within VSCode

```
weather-dashboard/
├── src/
│   ├── init.py
│   └── weather_dashboard.py
├── .env
├── .gitignore
└── requirements.txt
```

nside the .gitignore you'll want to prevent git from moving specific files to your repo either because of security or due to file size (not in this case though).

So, inside .gitignore, type:

```
.env
.git
```

Inside the requirement.txt, type the following python packages and their version. We will need to install them in the next step

```
boto3==1.26.137
python-dotenv==1.0.0
requests==2.28.2
```

- boto3 allows python to speak to your aws s3 bucket
- python-dotenv let you be able to store and retrieve data inside secured .env
- requests allows you to fetch data via API


### 3. Installing the package needed

With the requirements.txt file, let's install all our packages.

`python install -r requirement.txt`
This will install the three packages and make them accessible to use

### 4. Configure AWS

`aws configure`

- Put the Access Key ID and press enter
- Put the secret access key also and press enter
- Leave others as default by pressing Enter

```
WEATHER_API_KEY=(OpenWeather API Keys Generated)
AWS_BUCKET_NAME=(Put A Globally Unique S3 Bucket Name)
```

### 5. Let write the script to fetch and store the weather info

In the weather-dashboard.py, use `git clone https://github.com/iamDayoDev/Day1-Weather-Dashboard-API.git` to fetch the script

Now, let's run the python script,
Run this command `python3 src/weather_dashboard.py`

### 6. Resource Check and Cleaning
- Verify your stroed data in the S3 Bucket
- EMPTY THE S3 BUCKET AND DELETE THE BUCKET

### You have succeffully created a weather app that makes API calls and store the data in an S3 Bucket


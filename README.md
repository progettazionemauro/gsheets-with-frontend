# gsheets-with-frontend
## Installation on Ubuntu 

Django-Google-Sheet

1) fork this repo

### Scaffold the project in VSC

1) make new directory for the project. After cd in the new directory
2) python3 -m venv venv
3) source venv/bin/activate
4) git clone --branch <name_of_branch> <http:// github link>
5) ls -la
6) cd gsheets-with-frontend
7) pip3 install -r requirements.txt
8) pip3 install -U django-gsheets-import

# Google Sheets Template Preparation

### Prepare the database
1) python3 manage.py makemigrations
2) python3 manage.py migrate
3) python3 manage.py createsuperuser
4) python3 manage.py loaddata authors works

### Run the project
1) python3 manage.py runserver <port ...8081, 8082....>
2) go to localhost/admin 
3) If all is OK you can see the data imported from google sheet template

### Now we go to scaffold Google Sheets template
### Setting up a Google Cloud Project¶
- create a Google Sheet - [here is the example](https://docs.google.com/spreadsheets/d/1Ujp2H4wwlBRKeAhc3yGEIcoRne9DLNtVm6Cu6-_Dg3Y/edit#gid=0)
- go in GCC (Google Cloud Console)
- go in Cloud Ovierview / Dashboard / Create New Project
- Go in “Enable API Services” > Library and select the following API: Google Sheets API and Google Picker API
- Go in “Enable API Services” > Credentials [for official reference](https://cloud.google.com/service-usage/docs/enabled-service?hl=it#default)
In alto a sx creare le credenziali
Flaggare “Application Data”
Are you planning …. flaggare NO
dare il nome al service account e poi Create and Continue con il ruolo di Owner






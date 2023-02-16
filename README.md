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
- Share and give editor rights to that account
- go in GCC (Google Cloud Console)
- go in Cloud Ovierview / Dashboard / Create New Project
- Go in “Enable API Services” > Library and select the following API: Google Sheets API and Google Picker API
- Go in “Enable API Services” > Credentials [for official reference](https://cloud.google.com/service-usage/docs/enabled-service?hl=it#default)
- Go in API > APIs and Services > Ouauth Consent Screen > External > Create: a) only App name, b) User support email and c) Developer contact information > Save and Continue
- Go in “Enable API Services” > Credentials > Create Credentials > OAuth client ID > Application Type: Web Application > Name: <App-Google-Sheets-Django > Create > and after Authorised JavaScript origins for local testing http://localhost:8000 and after you can also add multiple relevant URIs here
- Dowload JSON: here you can find Your Client ID and Your Client Secret
- Note: Accessing the selected Google Sheet while only using the non-sensitive .../auth/drive.file scope requires the project’s App ID to be set. It is automatically created with each Google Cloud Project and can be found as Project number on your project’s dashboard or under the same name at Main Menu > IAM & Admin > Settings.
- Go in Iam Admin > Create Service Account > Service Account Name > Create and Continue after Grant this Service ... > Select Role > Owner > Continue > Done
- Copy the generated email
- Now in Google Sheets Template that you have created > Sharing > paste the generated email
 
### Back to the project
- Only for testing (not in production)
 in file settings.py
 
 #### The Browser API key; see "Key" under "APIs & Services" > "Credentials" > "API Keys"
GSHEETS_IMPORT_API_KEY = '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'

#### The Client ID; see "Client ID" under "APIs & Services" > "Credentials" > "OAuth 2.0 Client IDs"
GSHEETS_IMPORT_CLIENT_ID = '109874705921151975570'

#### The App ID; see "Project Number" under "IAM & Admin" > "Settings"
GSHEETS_IMPORT_APP_ID = '998033857983'









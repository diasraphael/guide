# Python Django rest framework

## check python version

```
python --version
```

## create project folder

```
mkdir django_rest_framework
```

## create virtual environment

```
python -m venv venv
```

By creating virtual environment we are making all the packages under this venv folder so that it wont affect other projects.

## Once virtual environment is created we need to activate

on windows for permission denied error run the below cmd

```
Set-ExecutionPolicy Bypass -Scope Process

.\venv\Scripts\activate
```

save the workspace with a file

## add the packages in requirements.txt

```
pip install -r requirements.txt
```

## update pip to latest

```
python.exe -m pip install --upgrade pip
```

## create a project

```
mkdir backend
cd backend
django-admin startproject home .
```

To create the project within the current directory

## Request

HTTP request returns HTML
Rest Api HTTP request returns JSON

```
response = requests.get(endpointurl)
print(response.json()) // returns python dictionary similar to javascript json notation with some difference
print(response.text) // returns text response
print(response.status_code) // returns response status code
```

## create new packages

python manage.py startapp api

when ever we create packages it needs to be entered in the main app settings file

## retrieving user data from request

```
def api_home(request, *args, **kwargs):
print(request.body) // returns data send in the body which is in byte string.
print(json.loads(request.body)) // converts byte string to json data
return JsonResponse({'message': 'This is the json response'})
```

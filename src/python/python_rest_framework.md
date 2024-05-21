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
print(request.body) // returns data send in the body which is in json byte string.
print(json.loads(request.body)) // converts byte JSON string to python dictionary
data['headers']= dict(request.headers)
data['content_type']= request.content_type
return JsonResponse({'message': 'This is the json response'})

// JsonResponse accepts dictionary as the input and it converts to a JSon response
// HttpResponse returns  HTML/text as response
```

## retrieving query parameters(values passed via url)

after the question mark all the values are query parameters

```
https://github.com?abc=123
```

data['params'] = dict(request.GET)

#### this interaction of converting the JSON object to Python dictionary can go wrong many times.

## Django rest framework

making or turning an api into a django rest framework

1: we need to add a decorator api_view from rest_framework.decorators(with that we can restrict the methods get, post).api_view is used when we use a function.

2. we can use Response from the django rest framework and use that to send the response back to client.

3. we can use serializers to converts object to dict and back to object.a model can have multiple serializers if needed.

4. rest_framework=>generics=>ListCreateApiView,RetrieveApiView,

```
serializer =ProductSerializer(data=request.data)
if serializer.is_valid(raise_exception=True):
  print(serializer.data)
  return Response(serializer.data)
```

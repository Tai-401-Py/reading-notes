# Auth and Production Server

## [The Web Token](https://jwt.io/introduction/)

JSON Web tokens are a compact waty of ttransmitting information between parties as a JSON object.

They are handy and can be used for things such as authorization and info exchange. 

They consist of 3 portions seperated by dots (.) Header/Payload/Signature.
 
JSON parsesrs are common in programming languages because they map directly to objects. Conversely, XML and SAML doesn't do the same. 

## [Integrating JWT with Django](https://simpleisbetterthancomplex.com/tutorial/2018/12/19/how-to-use-jwt-authentication-with-django-rest-framework.html)

JWT is typically exchanged for a user/pass to create an access/refreesh token. 

```py
pip install djangorestframework_simplejwt

# settings.py

REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': [
        'rest_framework_simplejwt.authentication.JWTAuthentication',
    ],
}
 
# urls.py

from django.urls import path
from rest_framework_simplejwt import views as jwt_views

urlpatterns = [
    # Your URLs...
    path('api/token/', jwt_views.TokenObtainPairView.as_view(), name='token_obtain_pair'),
    path('api/token/refresh/', jwt_views.TokenRefreshView.as_view(), name='token_refresh'),
]
```

## [RUNSERVER NOT PRODUCTION SERVER](https://vsupalov.com/django-runserver-in-production/)

The docs say don't do it! 

While it's good for development and test purposes it is unstable. 

WWhen a request hits your server it should be passed to  a web server, there are aloso application servers which uses the fancy requests to construct python objeccts. 

The project provides a `uwsgi.py` file, which contains a function to be called by the application server. This function gets a Python object representing the incoming request.

TL;DR: To run in production use Nginx for web server, and let the application be handled by a WSGI app server like Gunicorn. 

If you plan on running on Heroku, a web server is provided implicitly. You don’t have to take care of it. You just need to specify a command to run your application server (again, Gunicorn is fine) in the Procfile.
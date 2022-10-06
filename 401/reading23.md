
# [Docker](https://wsvincent.com/beginners-guide-to-docker/)

Docker under the hood is just Linux Containers which are a type of virtualization. 

Virtualization has it's roots at the beginning of comp-sci when giant mainframes are the norm. How could programmers all use the same computer, the answer, virtualization. Virtual machines allow many people to share the same resources of a computer all while operating in thier own environments. 

If you rent space on an AWS, you don't get a dedicated peice of hardware, you probably share that hardware with hunderds or evn thougsands of people. 

In recent years containerization has become more popular, for most applications a virtual machine provides more resources than needed and a container is sufficient. 

Fundamentally Docker is just that, a way to implement Linux Containers. 

## Containers Vs. Virtual Environments

Virtual environments are run locally in an isolated box, though they can only isolate packages. When you use a reference to the main program, it's on the main computer. Not actually within the virtual enviroment. 

Containers are like whole OS's in a box instead of just isolating packages. 

A baking analogy we can use here is as follows:

* A Dockerfile is the recipe for a cake
* An image is a snapshot of the recipe at a given time
* A docker-compose.yml says how to make the cake
* And the container is the actual, baked cake

## Creating an Image

We can create an image and container just for Python and later add to it. First you need to create a local directory, next yyou define the image with a `Dockerfile` similar to a pipenv or a requiremtns.txt file. This `Dockerfile` is a list of all of the requirements needed to build our image. 

Every Dockerfile mus begin with a `FROM` command. Each of these dockerfiles is read from top to bottom. Once you have completeed instructions it's time to Build.

`docker image build .` **DONT FORGET THE PERIOD**

Each of these images built is made up of is often a flavor of linux, images are layerd like this because they need to be immutable like a git-commit. this helps ensure consistency when two developers build the same image. The second, is performance. Docker itself caches the steps in Dockerfile to speed up subsequent builds. 

The `Dockerfile` for our image will completely replace the the local dev environment. The `docker-complose.yml` will contain the container instructions. 

```py
# $ touch Dockerfile
# $ touch docker-compose.yml
```

# [Django Rest Framework](https://www.django-rest-framework.org/api-guide/permissions/)

Toigether with Auth and Throttling, permissions determine access. They typically ue auth info in the `request.user` and `request.auth` props. 

The simplest perm are to authorize any authenticated user and deny any who aren't. Slightly less strict would allow READ ONLY permissions to unauthenticated users. This would correspond to `IsAuthenticatedOrReadOnly` Class in the REST framework.

REST framework also support perms at the object level. These are used to determine if a user should be able to act upon a model insance/object.

These object lebvel permissions are run when `.get_object()` is called. As with view level perms, an `exceptions.PermissionDenied` will be raised if the user is not authorized to act on the object. 

If you would like to override on a generic view you need to call explicitly `.check_object_permissions(req,obj)` on the view at the point it is retrieved. 

Limitations are that this prevents viewing and editing, but in order to stop creation permissions mst be enables on the `Serializer` class, or override the `perform_create()`

## Setting permissions 

The default may be set globally

```py
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}
```

If not set, it will default to allow any. 

## API Reference

- AllowAny - This will allow unrestricted access regardless of authentication status.
- IsAuthenticated will deny anyone not Authenticated
- IsAdminUser will deny anyone who isn't an admin. 
- IsAuthenticatedOrReadOnly - Will allow authenticate users to perform requeests but unauthenticaed can use any `GET`, `HEAD`, or `OPTIONS`.
- DjangoModelPermissions
  - This class ties into Django's standard `django.contrib.auth` Model Perms. This perm must only be applied to views that have a queryset prop. or `get_queryset()` method. 

  
    `POST` requests require the user to have the add permission on the model.
    `PUT` and `PATCH` requests require the user to have the change permission on the model.
    `DELETE` requests require the user to have the delete permission on the model.


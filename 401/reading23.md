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





Docker Images
==============================


## Lab – Dockerfiles II

This is a challenge lab and provides minimal instructions, thus requiring you to use the course powerpoint, your
resourcefulness, and the Docker references you have learned about in class to complete several Dockerfile and image
oriented tasks.

The goal of the lab is to produce a single layer Alpine image look alike that automatically runs a Bash shell.

### 1. Export An Alpine Container To Create A TAR File Of The Alpine File System

```
user@ubuntu:~/websvr$ cd
user@ubuntu:~$ mkdir alpining
user@ubuntu:~$ cd alpining/
user@ubuntu:~/alpining$
```

`docker container create`

`docker container export`

### 2. Create A Dockerfile That Builds Your New Alpine Image With The Bourne Executable As The Default Command

```
FROM scratch
ADD
CMD
```

- What is the difference between the approach outlined here and simply using FROM alpine
- Can you guarantee that FROM will use a specific set of approved bits?
- Can you guarantee that FROM will always use an image with only one layer?

### 3. Content Addressable FROM

The Dockerfile FROM command supports three possible forms:

- FROM <imageRepo>
- FROM <imageRepo>:<tag>
- FROM <imageRepo>@<digest>

By using the Alpine image repository name and the SHA digest you can guarantee that a specific set of bits is used as
your base. Recreate the previous project using FROM with the Alpine digest.

### 4. Load/Save

- Run `docker container ls` to display all of your images
- `docker image save` (one of) the custom Alpine image repos you just created
- Remove the custom image and ensure that it is no longer present
- `docker image load` the custom alpine image back from the saved file

Can you guarantee this image is the same as the prior image? If so how?

### [OPTIONAL Extra Credit] Build the Python 2.7 Image

The official Python images are sourced here:  

- https://github.com/docker-library/python

Build the image for Python 2.7 using the above URL, specifying the master branch
and the Python 2.7 Dockerfile.

<br>

Congratulations, you have completed the Dockerfile II lab!

<br>

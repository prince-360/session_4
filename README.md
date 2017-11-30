# Session 4

The project will have to be versioned using git and pushed on your personal
account. The git repository will have to be called project_4
Your repository will have to contain:

## File required:

* `requirements.txt`
* `.gitignore`
* `Dockerfile`
* `your source code`

## Run time

* python 3

## Dead-line

2017-12-06 23:59

## Repository

**project_4**

## Description

You have to write a simple service that can resize images.

The supported file extensions are:

* jpeg
* png
* gif
* bmp

The output file will be resized based on the query parameter **scale** which is
a float number, and then, send the file on the HTTP response with the status **200**.

Examples:

```
POST /resize?scale=2
POST /resize?scale=0.5
POST /resize?scale=1.5
POST /resize?scale=1.0
```

If **scale** parameter is not a number or not in range 0 < scale < +inf, then you
will return the status 400 with an empty body.

If the file sent to your service is not a image, then you  will return the
status 400 with an empty body.

Your service will have to run on a Docker instance so feel free to organize your
code as you want.

Your base docker image will have to be **python:3.6.3** and expose the port of
your service.

Base Dockerfile that you need to use.

```
FROM python:3.6.3
RUN pip install -r requirements.txt
```


## Server

The server will listen on the post **8888** and the interface **0.0.0.0**

## Tips

To manipulate images, you can use the powerful library called **pillow**

```
pip install pillow
```

## Important

* If you project repository is not private => deleted
* If your project doesn't run => 0/100
* If your project crashed => 0/100

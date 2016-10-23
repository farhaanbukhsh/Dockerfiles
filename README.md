# Dockerfiles


## Jupyter


Command to build container:


`sudo docker build -t "python-tool:0.0.1" --rm=true --no-cache . `


Command to run the `container` and mount the working directory:


`sudo docker run --rm --name "python-tools" -it -p 8888:8888 -v "$PWD":/project python-tool:0.0.1 bash`


Inside the container run :

`jupyter-notebook --ip=0.0.0.0 --no-browser`


Page will be served on `localhost:8888`

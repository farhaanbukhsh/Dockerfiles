# Dockerfiles


## Jupyter


Command to build container:


`sudo docker build -t "python-tool:0.0.1" --rm=true --no-cache . `


Command to run the `container` and mount the working directory:


`sudo docker run --rm --name "python-tools" -it -p 8888:8888 -v "$PWD":/project python-tool:0.0.1 bash`


Inside the container run :

`jupyter-notebook --ip=0.0.0.0 --no-browser`


Page will be served on `localhost:8888`


## Pagure

- Clone pagure on the machine

- Add this `Dockefile` in the same repo 

- Then run the docker build command mention in the file

- Run the `docker` container as: 

    `sudo docker run --rm --name "pagure" -it -p 5000:5000 pagure:0.0.1 bash`

- Inside the container run `./runserver.py --host 0.0.0.0`

# che
Eclipse Che for a local install

# Install and run Che
$ mkdir data
$ docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v `pwd`/data:/data -e CHE_HOST=10.249.26.199 -ti eclipse/che start

# Stop Che
$ docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v `pwd`/data:/data -e CHE_HOST=10.249.26.199 -ti eclipse/che stop

# Restart Che
$ docker run --rm -v /var/run/docker.sock:/var/run/docker.sock -v `pwd`/data:/data -e CHE_HOST=10.249.26.199 -ti eclipse/che stop restart

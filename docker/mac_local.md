## Running docker locally

[This](https://docs.docker.com/engine/installation/mac/#examples-on-mac-os-x)
is a handy little doc to get a `docker`ized version of you app up and
running locally.

The two things I needed were:
1. to run `docker run` with `-P` to map ports to random local ports.
2. Then run `docker port CONTAINER` to get the port mappings
3. run `docker-machine ip default` to get the ip
4. Then put it all together to access locally


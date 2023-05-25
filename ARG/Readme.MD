## ARG

Arg is used to supply few variables at the image creation
arg is the only instruction used before from
arg cant be accessed after FROM.
-------

## ENV and ARG

ENV used at the time of image and container creation

* Create one env variable and assign the value of ARG to that.
* Then we can access ARG values through ENV both in image and container.
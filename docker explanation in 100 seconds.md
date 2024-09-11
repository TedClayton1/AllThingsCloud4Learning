Docker a tool that can package software into containers that run reliably in any environment. What is a
container and why do you need one? Pretend you built an app with "Cobol" that runs on some weird flavor of
Linux and you want to share this app with you friend but he is on a totally diff system.
The problem is how do we replicate the environment our software needs on any machine. One way to package an app is 
with a virtual machine where the hardware is simulated then installed with the required os and dependencies.
This allows us to run multiple apps on the same infrastructure.

However, each vm is running it's own OS they tend to be bulky/slow. A docker container is conceptually very similar
to a vm with 1 key difference instead of virtualizing hardware containers only virtualize the OS. Or in other words all apps/
containers are run by a single kernel and this makes everything more faster/efficient.

There are 3 universal elements in the universe of docker. 
1. Dockerfile
2. Image
3. Container (self-contained, runnable software application/service that's packaged with all the dependencies it needs to run
.) Containers are lightweight and are isolated, allowing multiple containers to run simultaneously on the same host. 

The dockerfile is like dna it's just code that tells docker how to build an image which itself is a snapshot of your 
software along with all its dependencies down to the os level. THe image is immutable and can be used to spin up multiple
containers which is your actual software running in the real world.

To create a docker file and use "from" to start from an existing template like Ubuntu. THis base image gets pulled down
from the cloud and you can also upload your own images to a variety of diff docker registries. From there you might
want to use a terminal command like "RUN" that installs dependencies into your image. You can set environment varieables
and all kinds of other stuff. Then the last thing you'll do is set a default command that is executed when you start up
a container. 

Now, we can create the image file by running the command "docker build -t myapp ./" It goes through each step in our docker
file to build the image layer by layer. Then we can bring this image to life as a container with the "docker run myapp" command.
As your app demands more resources you can run it on multiple machines, multiple clouds on-prem or wherever you want
reliably.
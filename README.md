# Containers from Scratch in Go

Three core concepts in linux that is essential to build a container are:
1. Namespaces
2. Chroot
3. Cgroups

## Namespaces:
In simple words, a Namespaces is where we limit what a container process can see. It enables the isolation required to execute multiple containers on a single machine, providing each with an environment that appears independent. Each can be requested independently, providing a process and its children with a view limited to a subset of the machine'.
There are six namespaces PID, MNT, USER, IPC, NET, UTC. They restricts the view of the resources in the host machine for the running containers.

## Chroot:
A chroot is an operation that changes the apparent root directory for the current running process and their children. When we specify a image while running a docker container, it takes the file system that is packed up in the image and unpacks it in your host machine and chroots the running container to see that new file system.

## CGroup:
It limits what container can use. It limits the resources that containers can use. It enforces fair resource sharing.



# CST8915 - Lab 4
Tahir Onur Ozkoral - 041122154

## Demo Video

[YouTube Demo Video](https://youtu.be/L5gzbuqMzNo)


## Reflection Questions

### 1. What are the main differences between a Docker image and a Docker container?
Docker image's purpose really similar to a blueprint. Basically it contains the application code and dependencies required to run it, as defined in the Dockerfile. In contrast a container is like an instance created using that blueprint.

### 2. Explain how Docker's layered architecture improves efficiency.
Docker uses layers so it doesn't have to rebuild or download everything every time. Like if we change something in the code, it won't bother with recreating the dependencies layer, or other unrelated layers. It would only recreate the changed layer and the layers that are affected by that change. So it makes it super efficient to change things faster with less resources.

### 3. Why does each container get its own writable layer?
Quite similar to why we run vms, but for containers it is on a different scale. Instead of isolating a whole operating system, we keep changes isolated between containers. Each container can modify its own files without affecting the original image or other containers.

### 4. What are the benefits of using Docker Compose over running containers individually?
The main reason is usually the practicality. We can manage multiple services using a single .yaml instead of running and configuring each container separately. It also naturally makes things like networking, volumes, and scaling easier to manage.
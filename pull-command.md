### Pull an image from Docker Hub {#pull-an-image-from-docker-hub}

To download a particular image, or set of images \(i.e., a repository\), use docker pull. If no tag is provided, Docker Engine uses the :latest tag as a default. This command pulls the debian:latest image:

![](/assets/import4.png)

Docker images can consist of multiple layers. In the example above, the image consists of two layers; fdd5d7827f33 and a3ed95caeb02.

Layers can be reused by images. For example, the debian:jessie image shares both layers with debian:latest. Pulling the debian:jessie image therefore only pulls its metadata, but not its layers, because all layers are already present locally:

![](/assets/pull.png)

To see which images are present locally, use the[`docker images`](https://docs.docker.com/engine/reference/commandline/images/)command:

![](/assets/pull2.png)



Docker uses a content-addressable image store, and the image ID is a SHA256 digest covering the image’s configuration and layers. In the example above, debian:jessie and debian:latest have the same image ID because they are actually the same image tagged with different names. Because they are the same image, their layers are stored only once and do not consume extra disk space.






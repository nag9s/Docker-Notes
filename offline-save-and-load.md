[https://www.percona.com/blog/2017/05/23/how-to-save-and-load-docker-images/](https://www.percona.com/blog/2017/05/23/how-to-save-and-load-docker-images/)

On_serverA _, get the image, and save it to a file:

![](/assets/save.png)

all you need to do is move the generated tar file to _serverB _\(by using “scp” or [any other](https://en.wikipedia.org/wiki/Sneakernet) means\), and execute the following:

![](/assets/load2.png)


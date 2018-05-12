# Wordpress with zip (or a customized docker image of wordpress)

To be able to use Duplicator in wordpress, we need to be able to zip. So I made a Dockerfile, where I use wordpress:latest and add stuff to it (wordpress:latest seems to understand Ubuntu commands).

To upload this to your docker-hub repo, build the Dockerfile, tag it, and push.

```
cd build
docker build -t wp-with-zip .
docker tag <the_tag> <user>/wp-with-zip:latest
docker push <user>/wp-with-zip
cd ..
```
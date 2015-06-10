# Nginx Dockerfiles

Dockerfiles for building [nginx](http://nginx.org) images on various base OS images

### How to use:
* ##### Serving static files (why I put this together in the first place)
  * Get the image (using the Centos tag in this example)
    ```
    docker pull nickmich/nginx:centos
    ```

  * Run the container
    ```
    docker run --nginx-static -d -p 8777:8777 -v <directory-of-nginx-config>:/opt/nginx -v <directory-of-static-files>:/var/nginx nickmich/nginx:centos
    ```

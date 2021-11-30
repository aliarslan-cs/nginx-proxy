# nginx-proxy

A running example of [soheilhy/nginxproxy.md](https://gist.github.com/soheilhy/8b94347ff8336d971ad0) using dockers.

You only need to update `server-list.conf` to make nginx work as a proxy server.

Run the nginx docker image as:

    docker run -it -p 80:80 --rm -v $(pwd)/server-list.conf:/etc/nginx/conf.d/server-list.conf --name the-nginx-proxy nginx

To test locally also add below line to `/etc/hosts` on your host machine. Remove any existing line for 127.0.0.1.

    127.0.0.1 example-google.com example-bing.com example-yahoo.com

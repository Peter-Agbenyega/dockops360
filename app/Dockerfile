# Use a lightweight base image
FROM alpine:latest

# Install a simple web server (busybox httpd)
RUN apk add --no-cache busybox-extras

# Create web server directory
RUN mkdir -p /var/www/localhost/htdocs

# Create an index.html file
RUN echo "<h1>Welcome to DockOps360 Application Container</h1>" > /var/www/localhost/htdocs/index.html

# Start the web server
CMD ["busybox", "httpd", "-f", "-p", "8080"]

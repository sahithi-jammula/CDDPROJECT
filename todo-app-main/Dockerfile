# Use official Nginx image (lightweight and fast)
FROM nginx:alpine

# Set the working directory inside the container
WORKDIR /usr/share/nginx/html

# Remove default Nginx static content
RUN rm -rf ./*

# Copy only necessary files from the host to the container
COPY ./index.html ./style.css ./script.js ./favicon.ico ./
COPY sources ./sources

# Expose port 80 for the web server
EXPOSE 80

# Start Nginx
CMD ["nginx", "-g", "daemon off;"]
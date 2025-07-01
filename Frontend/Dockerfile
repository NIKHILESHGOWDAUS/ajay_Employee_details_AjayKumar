# Use the lightweight nginx image
FROM nginx:alpine

# Remove default nginx config file
RUN rm -rf /etc/nginx/conf.d/default.conf

# Copy your custom nginx config to the container
COPY default.conf /etc/nginx/conf.d/

# Remove default nginx html content
RUN rm -rf /usr/share/nginx/html/*

# Copy the frontend build output to nginx's html directory
COPY build/ /usr/share/nginx/html/

# Expose port 80
EXPOSE 80

# Start nginx server (this is default CMD in nginx image, so optional to specify)
CMD ["nginx", "-g", "daemon off;"]


# Use the official Nginx image from Docker Hub
FROM nginx:alpine

# Copy the HTML, CSS, and JS files to the Nginx HTML directory
COPY index.html /usr/share/nginx/html/
COPY styles.css /usr/share/nginx/html/
COPY script.js /usr/share/nginx/html/

# Expose port 80 to allow traffic
EXPOSE 80

# Start Nginx server
CMD ["nginx", "-g", "daemon off;"]

# Use official Node.js image
FROM node:18

# Set working directory inside the container
WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the application files
COPY . .

# Expose the backend port
EXPOSE 3423

# Run the server
CMD ["node", "server.js"]


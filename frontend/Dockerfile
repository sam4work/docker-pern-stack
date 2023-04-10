# Base image
FROM node:18-alpine as frontend

# Set working directory
WORKDIR /app


# Copy package files
COPY package*.json .

# Install production dependencies
RUN npm ci 

# Copy the rest of the application files to the container
COPY . .

# Build the application
# Specify a default command to run when the container starts
CMD [ "npm", "run", "build" ]
# Stage 1: Build stage (for example, for a React app)
FROM node:14 AS builder

WORKDIR /app

# Copy package files and install dependencies
COPY package*.json ./
RUN npm install

# Copy source files and build the app
COPY . . 
RUN npm run build  # This will generate the /build directory

# Stage 2: Nginx stage to serve the app
FROM nginx:alpine

# Copy the Nginx configuration (if needed)
COPY ./nginx/default.conf /etc/nginx/conf.d/default.conf

# Copy the build directory from the builder stage to the Nginx HTML directory
COPY --from=builder /app/build /usr/share/nginx/html

# Expose the port on which Nginx will run
EXPOSE 3000

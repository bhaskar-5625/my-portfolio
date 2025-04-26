# Use an official Node.js runtime as a parent image
FROM node:20

# Set working directory
WORKDIR /app

# Copy package.json and install dependencies
COPY package*.json ./
RUN npm install

# Copy the rest of the code
COPY . .

# Build the app
RUN npm run build

# Install serve to serve the build
RUN npm install -g serve

# Start the app
CMD ["serve", "-s", "build", "-l", "3000"]

# Expose port
EXPOSE 3000

# Use the required version of NodeJS
FROM node:16.20.2-buster-slim

# Expose the port (I'm using a M1 Mac)
EXPOSE 5050

# Set up the working directory for the app
WORKDIR /app

# Copy the list of dependencies
COPY ./package* .

# Install the dependencies
RUN npm i

# Copy the rest of the source code
COPY . .

# Build the project
RUN npm run build

# Install the utility to serve the static files to a port
RUN npm install -g serve

# Run the project
CMD ["serve", "-s", "-l", "5050", "build"]
# Use the lightweight image of the required Golang version
FROM golang:1.16-alpine3.14

# Expose the port
EXPOSE 8080

# Set up the directory for the app
WORKDIR /app

# Copy the dependency list
COPY go.mod .

# Install the dependenices
RUN go mod download

# Copy the rest of the source code
COPY . .

# Compile the project with the name "server" for the executable
RUN go build -o server app.go

# Run the project
CMD ["./server"]
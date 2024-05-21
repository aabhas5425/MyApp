# Use the official Go image as a base image
FROM golang:1.16-alpine

# Set the working directory inside the container
WORKDIR /app

# Copy go.mod and go.sum files to the working directory
COPY go.mod go.sum ./

# Download Go modules
RUN go mod download

# Copy the rest of the application code to the working directory
COPY . .

# Build the application
RUN go build -o myapp

# Specify the command to run the application
CMD ["./myapp"]

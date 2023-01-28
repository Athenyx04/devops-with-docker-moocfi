# We need Go 1.16. I found this from Docker Hub.
FROM golang:1.16

EXPOSE 8080

WORKDIR /usr/src/app

# Copy all of the source code
COPY . .

# Add the environment information
ENV REQUEST_ORIGIN http://localhost:5000

# Install all packages and build
RUN go build

# Test the build
RUN go test

# And finally the command to run the application
CMD ["./server"]
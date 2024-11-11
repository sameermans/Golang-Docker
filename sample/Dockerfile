# Step 1: Use an official Golang image as the base image
FROM golang:1.20

# Step 2: Set the working directory inside the container
WORKDIR /app

# Step 3: Copy Go modules files first to leverage Docker caching
COPY go.mod ./

# Step 4: Download dependencies
RUN go mod download

# Step 5: Copy the rest of the application files
COPY . .

# Step 6: Build the Go application
RUN go build -o main .

# Step 7: Expose the port the app will run on
EXPOSE 8080

# Step 8: Run the application
CMD ["./main"]

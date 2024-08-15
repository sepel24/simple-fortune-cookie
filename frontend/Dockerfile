FROM golang:1.19

# Set destination for COPY
WORKDIR /app

# Download Go modules
COPY go.mod ./
RUN go mod download

# Copy the source code.
COPY . .

# Build
RUN go build -o /frontend

# Expose the port that your Go app listens on
EXPOSE 8080

# Run
ENTRYPOINT ["/frontend"]
FROM golang:1.19

# Set destination for COPY
WORKDIR /app

# Download Go modules
COPY go.mod go.sum ./
RUN go mod download

# Copy the source code.
COPY . .

# Build
RUN go build -o /backend

# Expose the port that your Go app listens on
EXPOSE 9000

# Run
ENTRYPOINT ["/backend"]
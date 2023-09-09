# Server in Go

## Create New Go Module for the project

```bash
go mod init
```

## Write main.go

## Build

```bash
go build -o out
```

## Run

```bash
./out
```

## Build & Run

```bash
go build -o out && ./out
```

## Fileserver

A fileserver is a kind of simple web server that serves static files from the host machine. File servers are often used to serve static assets for a website, like:

- HTML
- CSS
- JavaScript
- Images

1. Create file 'index.html'
2. Add line in 'main.go': `mux.Handle("/", http.FileServer(http.Dir("."))) `

## Custom Handlers

An http.Handler is any type that implements the ServeHTTP method:

```go
type Handler interface {
    ServeHTTP(ResponseWriter, *Request)
}
```

The http.ServeMux is an http.Handler
You use a Handler for more complex use cases, such as:

- Implement custom router
- Middleware
- any other custom logic

You will tipically use a HandlerFunc when you want to implement a simple handler.

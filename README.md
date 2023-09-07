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

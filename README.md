# Simple Go Web Server

This is a basic HTTP server written in Go. It demonstrates how to:

- Serve static files from a `static/` directory
- Handle GET and POST requests
- Process HTML form submissions

## Features

- **Static file server**: Serves files from `./static` at the `/static/` URL path.
- **Hello endpoint**:  
  - `GET /hello` → returns `hello!`  
  - `POST /hello` → confirms a POST request was sent
- **Form handler**:  
  - `POST /form` → accepts form data (`name` and `address`) and prints it back in the response

## Requirements

- [Go](https://go.dev/) 1.18+ installed

## Running the server

From the project root (`go-server/`):

```bash
go run static/main.go
You should see:

Starting server on :8080
The server will now be available at http://localhost:8080.
```
Usage
1. Static files
Any files in the static/ folder are available at /static/...

Example: static/form.html → http://localhost:8080/static/form.html

2. Hello endpoint
# GET
curl http://localhost:8080/hello

# POST
curl -X POST http://localhost:8080/hello
3. Form endpoint
Submit form data (e.g., from an HTML form or curl):

curl -X POST -d "name=Alex&address=123+Main+St" http://localhost:8080/form
Response:

`POST request successful
Name = Alex
Address = 123 Main St
Project Structure`

go-server/
├── static/
│   ├── main.go        # Go server
│   ├── form.html      # Example HTML form
│   └── ...            # Other static assets
License
MIT

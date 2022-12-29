# Developing a Simple Webserver

# AIM:

name:Bodicherla venkata bharadwaj
ref no:22003979

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
```python
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<html>
<head>
</head>
<body>
<hl>Welcome</hl>
<h>BHaradwaj</h>
<h>22003979</h>
</body>
<html>
"""

class HelloHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode)

server_address=('',8000)
httpd = HTTPServer(server_address, HelloHandler)
httpd.serve_forever()
```

## OUTPUT:
![model](/out%20put.png)

## RESULT:
The program is executed succesfully

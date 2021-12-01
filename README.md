# Developing a Simple Webserver
## AIM:

To develop a simple webserver to display about top five programming languages.
## DESIGN STEPS:
### Step 1:HTML content creared

HTML content creation
### Step 2:Design of webserver workflow

Design of webserver workflow
### Step 3:implementation using python code

Implementation using Python code
### Step 4:serving the HTML pages

Serving the HTML pages.
### Step 5:testing the webserver

Testing the webserver
## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1>Welcome</h1>
</body>
</html>
"""
class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8080)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```
## OUTPUT:
CLIENTOUTPUT
![git logo](clientoutput.png)
SERVEROUTPUT
![git logo](serveroutput.png)
## RESULT:
Thus the webserver is developed to display about top five programming languages. 
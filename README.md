# EX01 Developing a Simple Webserver
## Date:18.09.2025

## AIM:
To develop a simple webserver to serve html pages and display the list of protocols in TCP/IP Protocol Suite.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
'''



from http.server import HTTPServer, BaseHTTPRequestHandler

PORT = 8000  

content = 
    
    <html>

        <head>
             <title>TCP/IP Protocol Suite</title>
        <style>
            body { font-family: Arial; background:#f2f2f2; padding:20px; }
            h1 { color:#333; }
            ul { background:#fff; padding:20px; border-radius:10px; }
            li { margin:8px 0; }
        </style>
    </head>
    <body>
        <h1>🌐 TCP/IP Protocol Suite</h1>
        <h2>Application Layer</h2>

        <ul>
            <li>HTTP, HTTPS</li>
            <li>FTP</li>
            <li>SMTP, POP3, IMAP</li>
            <li>DNS</li>
            <li>SSH, Telnet</li>
            <li>SNMP</li>
        </ul>

        <h2> Transport Layer</h2>
        <ul>
            <li>TCP</li>
            <li>UDP</li>
        </ul>

        <h2>Internet Layer</h2>
        <ul>
            <li>IP (IPv4, IPv6)</li>
            <li>ICMP</li>
            <li>ARP</li>
            <li>IGMP</li>
        </ul>

        <h2>Network Access Layer</h2>
        <ul>
            <li>Ethernet</li>
            <li>Wi-Fi</li>
            <li>PPP</li>
            <li>Frame Relay</li>
        </ul>
    </body>
    </html>


class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())

server_address = ('', PORT)  # use PORT variable here
httpd = HTTPServer(server_address, myhandler)
print(f"🚀 My webserver is running at http://localhost:{PORT}")
httpd.serve_forever()

'''
## OUTPUT:
![alt text](<Screenshot (4).png>)
![alt text](<Screenshot (5).png>)
## RESULT:
The program for implementing simple webserver is executed successfully.


Simple Distributed File System
This is a simple implementation of a distributed file system using Flask for communication between nodes and a coordinator.

Overview
The file system consists of three main components:

Node Servers: These are the servers responsible for storing and managing chunks of files. Each node runs a Flask server to handle upload and download requests.

Coordinator: The coordinator acts as the master node in the system. It receives file upload requests from clients, splits files into chunks, and distributes them across available node servers. It also handles file download requests by retrieving chunks from node servers and reassembling them into the original file.

Client: The client script provides a simple interface for users to upload and download files from the file system.

Components
node.py: This script represents a node server. It handles requests to upload chunks of files and associate chunks with filenames.

coordinator.py: The coordinator script manages file uploads and downloads. It distributes chunks across node servers and coordinates the download process.

client.py: The client script provides functions to upload and download files from the file system.

run_all.py: This script starts all necessary servers.

Usage
Start the node servers by running python node.py --port <port_number> for each desired node.

Start the coordinator server by running python coordinator.py.

You can also use the client script directly to upload and download files from the file system.

Run the test scenario by executing python run_all.py.

Requirements
Python 3.x
Flask
Requests

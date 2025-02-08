𝐒𝐢𝐦𝐩𝐥𝐞 𝐃𝐢𝐬𝐭𝐫𝐢𝐛𝐮𝐭𝐞𝐝 𝐅𝐢𝐥𝐞 𝐒𝐲𝐬𝐭𝐞𝐦

This is a simple implementation of a distributed file system using Flask for communication between nodes and a coordinator.

𝐎𝐯𝐞𝐫𝐯𝐢𝐞𝐰
The file system consists of three main components:

𝐍𝐨𝐝𝐞 𝐒𝐞𝐫𝐯𝐞𝐫𝐬: These are the servers responsible for storing and managing chunks of files. Each node runs a Flask server to handle upload and download requests.

𝐂𝐨𝐨𝐫𝐝𝐢𝐧𝐚𝐭𝐨𝐫: The coordinator acts as the master node in the system. It receives file upload requests from clients, splits files into chunks, and distributes them across available node servers. It also handles file download requests by retrieving chunks from node servers and reassembling them into the original file.

𝐂𝐥𝐢𝐞𝐧𝐭: The client script provides a simple interface for users to upload and download files from the file system.

𝐂𝐨𝐦𝐩𝐨𝐧𝐞𝐧𝐭𝐬

node.py: This script represents a node server. It handles requests to upload chunks of files and associate chunks with filenames.

coordinator.py: The coordinator script manages file uploads and downloads. It distributes chunks across node servers and coordinates the download process.

client.py: The client script provides functions to upload and download files from the file system.

run_all.py: This script starts all necessary servers.

𝐔𝐬𝐚𝐠𝐞

Start the node servers by running python node.py --port <port_number> for each desired node.

Start the coordinator server by running python coordinator.py.

You can also use the client script directly to upload and download files from the file system.

Run the test scenario by executing python run_all.py.

𝐑𝐞𝐪𝐮𝐢𝐫𝐞𝐦𝐞𝐧𝐭𝐬
Python 3.x
Flask
Requests


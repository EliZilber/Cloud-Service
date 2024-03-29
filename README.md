# Cloud-Service
I created this cloud service program as a part of my Computer Networks course in the second year of my CS study.
This project was coded using a single thread in Python on top of TCP protocol. 
The service supports both Linux and Windows. 

<li> Cloud files backup services usually offer customers the option to download client software to the computer which allows them to select a folder on the computer and synchronize it automatically with the server at any change and between different computers. </li>

<li>This service lets you create a server from your own, and support multiple customers. At first, the customer defines a folder to sync. The software uploads to the server all the files in the folder for backup and from now on the software monitors any change that takes place in the folder deeply. When such a change is detected, the software updates the server about the change so that the backup on the server will be updated accordingly.</li>

<li>The server can handle several different clients, and every client gets a unique ID letting him connect the service from other devices.</li>

# Compiling and Running
You must have Python 3.10 or higher installed on your machine. Run the server.py file attached to utils.py by the following command in the terminal:

<code> python3 servery.py 12345 </code>

The number 12345 is the port number the server is listening to. You may use another port number if you want to.
Now, run the client.py file attached to utils.py in the computer of the client by the following command in the terminal:

<code> python3 client.py 1.2.3.4 12345 backup_folder 10 </code>

The parameters are the IP address and port number of the server, the name of the backup folder and seconds to wait between connections to the server.

You can also use IDE's like PyCharm of course!

# Extra: Sync Another Device
This part guides you how to connect existing client from another device.
<li>Go to the cache folder in service. Get your id - it is the name of the folder containing your files. </li>
<li> Run the client script in the new computer by typing the following command in terminal: </li>

<code> python3 client.py 1.2.3.4 12345 backup_folder 10  SERIAL_CODE </code>

**Serial Code Retrieval**

To obtain the SERIAL_CODE necessary for registration, follow these steps:

1. **Getting the Serial Code:**
   - The serial number is displayed on the client's command-line interface during registration.

2. **Recovering Lost Serial Code:**
   - If you've disconnected your client and forgotten the serial code:
     - Each user has a dedicated folder on the server, named after their serial code.
     - Navigate to your user folder on the server to retrieve the serial code.

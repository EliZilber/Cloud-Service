# Cloud-Service
I created this cloud service program as a part of my Computer Netorks course in the second year of my CS study.
The program let you backup your files on a server you set. You can also sync folders over different computers and support multiple useres.
This project was coded using a single thread in Python on top of TCP protocol. 
The service supports both Linux and Windows. 

Any change in files in the source folder will be updated in the server. Program should detect all cases - creaion of new file or folder, modifying or deleting. Doing this using the watchdog library.

The program supprorts backup of same files on Every new user gets a random serial code in the server. 

# Compiling and Running
You must have Python 3.10 or higher installed on your machine. Run the server.py file attached to utils.py by the following command in the terminal:

python3 servery.py 12345

The number 12345 is the port number the server is listening to. You may use another port number if you want to.
Now, run the client.py file attached to utils.py in the computer of the client by the following command in the terminal:

python3 client.py 1.2.3.4 12345 backup_folder 10

The parameters are the IP address and port number of the server, the name of the backup folder and seconds to wait between connections to the server.

You can also use IDE's like PyCharm of course!

# Backup of Multiple Computers
To connect another device first go to the cache folder in service. Get your id - it is the name of the folder containing your files.
To connect your 

# How to Compile and Run Code

To compile and run the code, it is recommended to use a virtual machine with `gcc` installed. If you don’t already have a server setup, please contact your instructor for access. Follow these steps to transfer, compile, and run the code on your server.

## Step 1: Setting Up Your Environment
1. **Accessing the Server**: Use PuTTY to connect to your server with the login credentials provided by your instructor.
2. **Transferring Files**: Transfer the `semaphores.c` file to the server using the `pscp` command from your local machine. The syntax is as follows:


pscp [local_file_path] [username]@[hostname]:[remote_directory]
[local_file_path]: Path to process_sync.c on your local machine.
[username]: Your server username.
[hostname]: The server IP address.
[remote_directory]: The directory on the server where you want to place the file.
# Step 2: Compiling the Code
Navigate to the Directory: Use cd to change to the directory where semaphores.c is located on the server.

Compile the Code: Use gcc to compile the file as follows:

bash
Copy code
gcc -o output_filename semaphores.c
output_filename is the name of the output executable file.

# Step 3: Running the Code
To run the executable, use the following command:

bash
Copy code
./output_filename

# cmd challenge
-> Challenges from cmdchallenge.com


## Pushing Files to SFTP via Command Line

This document provides step-by-step instructions for pushing the files `0-first_9_tasks.jpg`, `1-first_9_tasks.jpg`, and `2-first_9_tasks.jpg` to an SFTP (Secure File Transfer Protocol) server using the command line. The SFTP protocol ensures secure and encrypted file transfers between your local machine and the remote server. Please follow the instructions below to complete the file push successfully.

## Prerequisites

Before proceeding with the file push, ensure that you have the following prerequisites in place:

1. Access to the SFTP server: Obtain the necessary credentials (hostname, username, and password) to connect to the SFTP server.
2. Command-line SFTP client: Install a command-line SFTP client on your local machine. The most common command-line SFTP client is OpenSSH, which is available by default on most Linux and macOS systems. For Windows, you can install PuTTY, which includes the `psftp` command-line SFTP client.

## Steps to Push Files to SFTP via Command Line

1. Open a terminal or command prompt on your local machine.

2. Connect to the SFTP server using the following command:
   ```
   sftp username@hostname
   ```
   Replace `username` with your SFTP username and `hostname` with the SFTP server hostname or IP address. If the SFTP server uses a non-default port, add the `-P` option followed by the port number.

3. Enter your SFTP password when prompted.

4. Once connected to the SFTP server, navigate to the desired destination folder where you want to push the files. This folder could be a predefined directory or a directory you create specifically for these files. Use the `cd` command to change directories.

5. On your local machine, locate the directory containing the files `0-first_9_tasks.jpg`, `1-first_9_tasks.jpg`, and `2-first_9_tasks.jpg`. Ensure that you have read permissions for these files.

6. In the terminal or command prompt, use the following command to push the files to the SFTP server:
   ```
   put 0-first_9_tasks.jpg 1-first_9_tasks.jpg 2-first_9_tasks.jpg
   ```
   This command uploads the specified files to the current directory on the SFTP server. If you want to upload them to a different directory, specify the destination path before the file names.

7. Wait for the file transfer to complete. The duration will depend on the file sizes and your internet connection speed. The progress of the file transfer will be displayed in the terminal or command prompt.

8. Once the file transfer is complete, verify that the files `0-first_9_tasks.jpg`, `1-first_9_tasks.jpg`, and `2-first_9_tasks.jpg` are now present in the destination folder on the SFTP server.

9. To disconnect from the SFTP server, use the following command:
   ```
   exit
   ```

Congratulations! You have successfully pushed the files `0-first_9_tasks.jpg`, `1-first_9_tasks.jpg`, and `2-first_9_tasks.jpg` to the SFTP server using the command line.

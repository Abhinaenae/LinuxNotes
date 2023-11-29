# File Permissions in Linux Systems

## Overview
File permissions in Linux dictate how files and directories can be accessed and manipulated. They define who can read, write, and execute files or directories, and they're set for three categories of users: owner, group, and others.

## Three Types of Permissions
- Read (r): Allows a user to view the contents of a file or list the contents of a directory.

- Write (w): Permits a user to modify the contents of a file or create, delete, or rename files within a directory.

- Execute (x): Grants a user permission to execute a file or traverse through a directory.

## Represented by three sets of characters:
- Owner Permissions - The permissions for the file or directory owner.
- Group Permissions - The permissions for users belonging to the file's group.
- Other Permissions - The permissions for users who are neither the owner nor in the group.

  
In the command line, file permissions are displayed as a sequence of ten characters. 
The first character indicates the file type, followed by three sets of three characters each, denoting the read (r), write (w), and execute (x) permissions for owner, group, and others respectively.

## Example
A file named `example.txt` has the following permissions: `-rwxr-x---`

- The first character `-` represents the file type (in this case, a regular file).
- The next three characters `rwx` indicate read, write, and execute permissions for the owner.
- The subsequent three characters `r-x` show read and execute permissions for the group.
- The final three characters `---` signify no permissions for others.

## Setting File Permissions
You can use the `chmod` command to modify file permissions. 

For instance, to grant read, write, and execute permissions to the owner, read and execute permissions to the group, and no permissions to others:
`chmod 750 filename`

## Changing Ownership
You can change the ownership of a file using the `chown` command.
For example, to change the owner of `example.txt` to a user named `newowner` and a group named `newgroup`: `chown newowner:newgroup example.txt`


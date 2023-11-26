# Adding, deleting, modifying users in Linux 

This process involves using specific commands to create or remove user accounts. The [sudo](https://www.sudo.ws/about/intro/) command will be used extensively with these features. Here are the basic steps for adding and deleting users:

## Adding Users:
#### Add a User:

Use the useradd command to create a new user. For instance, to create a user named "newuser":
```
sudo useradd newuser
```
#### Set Password for the New User:

Use the passwd command to set a password for the newly created user:

```
sudo passwd newuser
```

#### Additional Options (Optional):

You can specify additional options when creating a user, such as the home directory or the shell using the -d and -s flags respectively:

```
sudo useradd -d /home/newuser -s /bin/bash newuser
```

## Deleting Users:
#### Delete a User:

Use the userdel command to remove a user. This command alone removes the user but doesn't delete their home directory or mail spool:

```
sudo userdel username
```

#### Delete User with Home Directory and Mail Spool:

To remove a user along with their home directory and mail spool, use the -r flag:

```
sudo userdel -r username
```
One must be cautious when deleting users as their files and data might be permanently lost if the -r flag is used carelessly.

## Modifying User Information:
#### Change User's Home Directory:

Use usermod to modify a user's information. For instance, to change a user's home directory:

```
sudo usermod -d /new/home/directory username
```

#### Change User's Shell:

Similarly, to change a user's default shell:
```
sudo usermod -s /bin/bash username
```

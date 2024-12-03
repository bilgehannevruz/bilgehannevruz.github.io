# Frequently Used Commands (FUC!)

### List All Users
To list all users in iRODS:

1. Open a terminal and connect to the iRODS server.
2. Use the `iadmin lu` command to list all users. For example:
    ```bash
     iadmin lu
    ```


### Create a User
To create a new user in iRODS:

1. Open a terminal and connect to the iRODS server.
2. Use the `iadmin mkuser` command followed by the username and user type. For example:
    ```bash
     iadmin mkuser john rodsuser
    ```


3. Set password for **john**
    ```bash
    iadmin moduser john password SecurePass123
    ```


### List Files with Physical Path
To list files with their physical path in iRODS:
1. Open a terminal and connect to the iRODS server.
2. Use the `ils -L` command to list files with their physical path. For example:
    ```bash
    ils -L /tempZone/home/john
    ```


### List All Resources
To list all resources in iRODS:
1. Open a terminal and connect to the iRODS server.
2. Use the `iadmin lr` command to list all resources. For example:
    ```bash
    iadmin lr
    ```


### List All Zones
To list all zones in iRODS, you can use the `iadmin` command with the `lz` option. This command lists all the zones configured in your iRODS environment.

1. To list all zones in iRODS:
    ```bash
    iadmin lz
    ```

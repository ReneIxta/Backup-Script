# Backup Script

This is a somewhat simple script written in bash to back up files for a given user. 

The insctructions are as follows: 
  * The script takes in three arugments
    - The first argument is either-S or -R. -S is for save and -R for restore.
    - The second argument is where the user account resides. i.e. /home
    - The third and final argument is the directory where the backup files will be stored
 * The -S will create backup tar files for the users in the backup directory
    - This will also create a file called what-is-here in the back up directory
    - This file will contain the following:
      * user name
      * home directory
      * backup date (in epoch seconds)
      * number of non-directory files
      * number of directories
      * total back up sixe in bytes
 * The -R will find all the users in the what-is-here file and unpack it in the /users directory
    - Do a recursive file-by-file check
      * if a file exist in the backup directory and not in the /home directory then that file will be restored
      

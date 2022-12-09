## In this repository is stored my solution of the edX's Final Project - Linux Commands and Shell Scripting.
### Verified certificate : https://courses.edx.org/certificates/9e088d08695c47ad8221b26b2ff3e87d


### _________________________________________________________________________________________________________________________
# Scenario
### You are a lead linux developer at the top-tech company “ABC International INC.” ABC currently suffers from a huge bottleneck - each day, interns must painstakingly access encrypted password files on core servers, and backup those that were updated within the last 24-hours. This introduces human error, lowers security, and takes an unreasonable amount of work.

### As ABC INC’s most trusted linux developer, you have been tasked with creating a script ```backup.sh``` which automatically backs up any of these files that have been updated within the past 24 hours.
# Task 1
#### Download the template file backup.sh by running the command:
 ```wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/Final%20Project/backup.sh```
#### Navigate to  `[TASK 1]` in the code.

#### Set two variables equal to the values of the first and second command line arguments, as follows:

#### Set `targetDirectory` to the first command line argument
#### Set `destinationDirectory` to the second command line argument

# Task 2
#### Display the values of the two command line arguments in the terminal.

# Task 3
#### Define a variable called `currentTS` as the current timestamp, expressed in seconds.

# Task 4
#### 1. Define a variable called `backupFileName` to store the name of the archived and compressed backup file that the script will create.
#### The variable `backupFileName` should have the value `"backup-[$currentTS].tar.gz"`
####  - For example, if `currentTS` has the value `1634571345`, then `backupFileName` should have the value `backup-1634571345.tar.gz`.

# Task 5
#### Define a variable called `origAbsPath` with the absolute path of the current directory as the variable’s value.

# Task 6
#### Define a variable called destAbsPath with value equal to the absolute path of the destination directory.

# Task 7
#### Change directories from the current working directory to the target directory targetDirectory.

# Task 8
#### You need to find files that have been updated within the past 24 hours.
#### This means you need to find all files who’s last modified date was 24 hours ago or less.
#### &nbsp;

#### To do make this easier:

#### Define a numerical variable called `yesterdayT`S as the timestamp (in seconds) 24 hours prior to the current timestamp, `currentTS`

# Task 9
#### Within the `$()` expression inside the `for` loop, write a command that will return all files and directories in the current folder.

# Task 10
#### Inside the `for` loop, you want to check whether the `$file` was modified within the last 24 hours.

# Task 11
##### In the if-then statement, add the ` $file` that was updated in the past 24-hours to the toBackup array.

# Task 12
#### After the for loop, compress and archive the files, using the `$toBackup` array of filenames, to a file with the name `backupFileName`

# Now the file `$backupFileName` is created in the current working directory.
#### Move the file `backupFileName` to the destination directory located at `destAbsPath`.

# Task 15
#### 1 Save the file you’re working on (`backup.sh`) and make it executable.
#### 2 Verify the file is executable using the `ls` command with the `-l` option:

# Task 16
#### 1.Download the following zip file with the wget command:
`wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/Final%20Project/important-documents.zip`
#### 2.Unzip the archive file:
`unzip -DDo important-documents.zip`
#### 3.Update the file’s last modified date to now:
`touch important-documents/*`
#### Test your script using the following command:
`./backup.sh important-documents .`
#### This should have created a file called `backup-[CURRENT_TIMESTAMP].tar.gz` in your current directory

# Task 17
#### Copy the `backup.sh` script into the `/usr/local/bin/` directory.

#### Note: You may need to use `sudo cp` in order to create a file in `/usr/local/bin/`
#### Test the cronjob to see if the backup script is getting triggered by scheduling it for every 1 minute.
#### `sudo service cron start`

#### Once the cron service is started, please check in the directory (`/home/project`) if the tar files are getting created.

#### If yes, then stop the `cron` service using the below command, else it will continue to create tar files every minute.

`sudo service cron stop`

#### Using crontab, schedule your `/usr/local/bin/backup.sh` script to backup the `important-documents` folder every 24 hours to the directory (`/home/project`).



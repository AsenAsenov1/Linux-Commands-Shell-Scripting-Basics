# Linux-Commands-Shell-Scripting-Basics
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
&nbsp;
&nbsp;
#### To do make this easier:

#### Define a numerical variable called `yesterdayT`S as the timestamp (in seconds) 24 hours prior to the current timestamp, `currentTS`


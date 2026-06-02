### Syntax of permissions in **ls** command
**1.** File type 
**2.1** Permissions on the file for the owner, group and other users 
	**2.2** About permissions it looks like this: 
		*r* - user can read the file
		*w* - user can write in the file
		*x* - user can execute the file3. File owner
	**2.3** Binary-Octal method
		A method to give permissions. This is how it looks:

| Binary | Octal | rwx |
| ------ | ----- | --- |
| 000    | 0     | --- |
| 001    | 1     | --x |
| 010    | 2     | -w- |
| 011    | 3     | -wx |
| 100    | 4     | r-- |
| 101    | 5     | r-x |
| 110    | 6     | rw- |
| 111    | 7     | rwx |

**3.** File owner
**4.** User that created the file 
**5.** File size in Bytes 
**6**. Date and time
**7.** File name

### To make files you need to:
touch <name>
mkdir <name>
Renaming files:
mv <file/directory> <renamed file/directory>
Finding files:
find <location> <options>
find / -type f -name *.conf -user root -size +20k -newermt 2020-03-03 -exec ls -al {} \; 2>/dev/null
find /etc/ -name shadow 2>/dev/null
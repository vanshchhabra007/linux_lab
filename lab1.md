We will be walking thourgh basic linux
 terminal commands
 ✅
 1. Navigation Commands
 pwd– Print Working Directory
 Shows the current location in the filesystem.
 (pwd)

![image-1](https://github.com/vanshchhabra007/images-/blob/main/image_1.jpg?raw=true)


ls – List Directory Contents

 The ls command is used to list files and directories in the current working directory.
 flag-a list down all the file and folder including the one which are hidden

  ls -l → Detailed list (permissions, size, date)
 ls -a → Shows hidden files (those starting with .)
 ls -la → Combined

 ![image-2](https://github.com/vanshchhabra007/images-/blob/main/image-2.jpg?raw=true)

  cd – Change Directory
 Moves into a directory.
 cd
 Examples:
 cd Documents        
cd ..               
cd /                
cd ~                
# Go to Documents
 # Go up one level
 # Go to root
 # Go to home directory

 ![image-3](https://github.com/vanshchhabra007/images-/blob/main/image-3.jpg?raw=true)

2. File and Directory Management
 mkdir – Make Directory
 Creates a new folder.
 mkdir new_folder
 touch– Create File
 Creates an empty file.
touch file.txt
 cp– Copy Files or Directories
 cp source.txt destination.txt
 mv – Move or Rename Files
 mv oldname.txt newname.txt
 rm – Remove Files
 rm file.txt          
rm -r folder_name    
# Delete file
 # Delete folder (recursively)

 ![image-4](https://github.com/vanshchhabra007/images-/blob/main/image-4.jpg?raw=true)
 
 3. File Viewing & Editing
 cat– View File Contents
 Displays content in terminal.
 cat file.txt
nano – Edit Files in Terminal
 A basic terminal-based text editor.
 nano file.txt
 Use arrows to move
 CTRL + O to save
 CTRL + X to exit

![image-5](https://github.com/vanshchhabra007/images-/blob/main/image-5.jpg?raw=true)

clear – Clears the Terminal
 clear
 Shortcut: CTRL + L4. System Commands
 echo – Print Text
 Useful for debugging or scripting.
 echo "Hello, World!"
 whoami – Show Current User
 whoami

![image-7](https://github.com/vanshchhabra007/images-/blob/main/image-7.jpg?raw=true)

![image-8](https://github.com/vanshchhabra007/images-/blob/main/image-8.jpg?raw=true)

man – Manual for Any Command
 man ls
 Use q to quit the manual.

5. Searching and Finding
 find – Locate Files
 find . -name "*.txt"
 🔍
 Finds all .txt files in current folder and subfolders.
 grep – Search Inside Files
 grep "hello" file.txt

![image-9](https://github.com/vanshchhabra007/images-/blob/main/image-9.jpg?raw=true)

6. Helpful Shortcuts
 Shortcut
 Tab
 ↑ / ↓
 CTRL + C
 Auto-complete files/folders
 Browse command history
 Stop a running command
 CTRL + L
 Clear screen
 
 7. Bonus: Chaining Commands
 Run multiple commands:
 mkdir test && cd test && touch hello.txt
 Run only if previous command succeeds: &&
 Run regardless of success: ;
 
 Shell Tutorial – File Permissions with
 chmod and chown
 
 1. Understanding File Permissions in Linux
 Each file/directory in Linux has:
 Owner → The user who created the file.
 Group → A group of users who may share access.
 Others → Everyone else.
 Permission Types
 r → Read (4 in numeric)
 w → Write (2 in numeric)
 x → Execute (1 in numeric)

![image-10](https://github.com/vanshchhabra007/images-/blob/main/image-10.jpg?raw=true)

 2. chmod – Change File Permissions
 Syntax
 chmod [options] mode filename
 Modes can be set in numeric (octal) or symbolic form.
 (A) Numeric (Octal) Method
 Each permission is represented as a number:
 Read = 4 Write = 2
 Execute = 1
 Add them up:
 7 = rwx
 6 = rw
5 = r-x
 4 = r--
 0 = --
Example:
 chmod 777 script.sh
 Meaning:
 Owner: 7 → rwx
 Group: 7 → r-w-x
 Others: 7 → r-w-x

![image-11](https://github.com/vanshchhabra007/images-/blob/main/image-11.jpg?raw=true)

![image-12](https://github.com/vanshchhabra007/images-/blob/main/image-12.jpg?raw=true)

 (B) Symbolic Method
 Use u (user/owner), g (group), o (others), a (all). Operators:
 + → Add permission- → Remove permission
 = → Assign exact permission
 Modes can be set in numeric (octal) or symbolic form.

![image-13](https://github.com/vanshchhabra007/images-/blob/main/image-13.jpg?raw=true)

(C) Recursive Changes
 chmod -R 755 /mydir-R → applies changes recursively to all files/subdirectories

 ![image-14](https://github.com/vanshchhabra007/images-/blob/main/image-14.jpg?raw=true)

  3. chown – Change File Ownership
 Syntax
 chown [options] new_owner:new_group filename

 Practice Experiment on chown
 
 1. Create a new user
 sudo useradd -m newuser-m → creates a home directory /home/newuser .
 
 2. Create a new group
 sudo groupadd newgroup
 3. Add the user to the group
 sudo usermod -aG newgroup newuser-aG → append user to the supplementary group (doesn’t remove existing groups).
 
 4. Create a file (as current user, e.g. root or your login user)
 touch testfile.txt
 Check ownership:
 ls -l testfile.txt

 5. Assign ownership of the file to newuser and newgroup
 sudo chown newuser:newgroup testfile.txt
 
 6. Verify ownership
 ls -l testfile.txt
 Output:-rw-rw-r--1 newuser newgroup 0 Aug 20 18:52 testfile.txt

![image-15](https://github.com/vanshchhabra007/images-/blob/main/image-15.jpg?raw=true)


4. Putting It All Together
 Example Scenario
 touch project.sh
 ls -l project.sh
 Output:-rw-r--r-- 1 sameer dev 0 Aug 19 12:00 project.sh
 Now:
 chmod 700 project.sh       

# Only owner has rwx
 chmod u+x,g-w project.sh 
 # Add execute for user, remove write for group
 chown root:admin project.sh
 # Change owner to root and group to admin

 
 5. quick reference

    
 0  ---  no access
 
 1  --x  execute only
 
 2  -w-  write only
 
 3  -wx  write and execute 
 
 4  r-- read only 
 
 5  r-x read + execute
 
 6  rw- read + write
 
 7  rwx  read write and execute 
 























 
 

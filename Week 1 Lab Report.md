# WEEK 1 LAB REPORT



## STEP 1: Install Visual Studio Code

First visit the following link, https://code.visualstudio.com/, and follow steps to install on your own computer. After installing and opening VScode, your screen should look like this:

![Alt text](https://github.com/stevpony/cse15l-lab-reports/blob/305bac610a24431970adef35fc1486762e4a2dca/Screenshot%202023-01-12%20at%203.09.29%20PM.png)

I had previously downloaded VScode for a previous program, so I had skipped this step.


## STEP 2: Remotely Connecting

Open a new terminal inside VScode (on my computer, click the "Terminal" option along the top of the screen, and click "New Terminal." Once in the terminal, type the following command: ssh cs15lwi23abc@ieng6.ucsd.edu, where the "abc" characters should be replaced by your own username (for me, cs15lwi23air). If it asks whether you want to continue or not, type "yes." Then, type in your password and you should be connected. This is what your screen should look like following these steps:

![Alt text](https://github.com/stevpony/cse15l-lab-reports/blob/305bac610a24431970adef35fc1486762e4a2dca/Screenshot%202023-01-12%20at%203.09.57%20PM.png)

## STEP 3: Running Commands

Here are a list of commands to copy or type into the terminal: 
- cd ~
- cd
- ls -lat
- ls -a
- ls <directory> where <directory> is /home/linux/ieng6/cs15lwi23/cs15lwi23air
- cp /home/linux/ieng6/cs15lwi23/public/hello.txt ~/
- cat /home/linux/ieng6/cs15lwi23/public/hello.txt

I used the command ls /home/linux/ieng6/cs15lwi23/cs15lwi23air, which shows me the list of files in my own account directory. I then tried ls /home/linux/ieng6/cs15lwi23/cs15lwi23ajm, the command to show the list of files in another account directory, which I was unable to view as I did not have permission. The command cat /home/linux/ieng6/cs15lwi23/public/hello.txt
prints out the contents of the hello.txt file, "Hello! Welcome to CSE 15L."

![Alt text](https://github.com/stevpony/cse15l-lab-reports/blob/305bac610a24431970adef35fc1486762e4a2dca/Screenshot%202023-01-12%20at%203.10.08%20PM.png)

After completing all these steps, simply use Command + D to exit from the remote server.

# Getting Started with Remote Access
*by Matteo Persiani*

### What you'll need to get started:
* A laptop or desktop with access to the internet which you can download and install files on.

### Step 1: Downloading VScode
1. Start by going to the [VScode download link](https://code.visualstudio.com/download) and downloading the appropriate version of VScode to your computer.
2. Unpack/Run the downloaded file so that VScode opens on your computer (should look similar to the image below).

>![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-01-11%20at%203.15.34%20PM.png)
This is what VScode looks like on my end.

### Step 2: Remotely Connecting
1. With VScode open, navigate to the top of the screen where "Terminal" is written and select "New Terminal".

![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-01-11%20at%205.42.09%20PM.png)

2. Before logging in, you're going to need to reset your password. Go to this [link](https://sdacs.ucsd.edu/~icc/index.php) and login with your TritonLink username PID.
3. Click the link for the Global Password Change Tool.

![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-01-11%20at%208.21.23%20PM.png)

4. Login again with your TritonLink username and PID and set a new password. Your current password should be your TritonLink password.
5. Be sure to select `No` to "Change MyTritonLink password".

![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-01-11%20at%208.22.28%20PM.png)

6. Now we can return to the terminal. In the terminal, type `ssh <username>@ieng6.ucsd.edu` with `<username>` being your username in the format "cs15lwi23..." with ... being your unique part of the username.
7. Enter your password and then your terminal should look similar to the one below.

>![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-01-11%20at%203.21.01%20PM.png)
First time logging in terminal.

>![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-01-11%20at%206.00.09%20PM.png)
Not first time logging in terminal.

### Step 3: Trying Some Commands
* Now you're free to use some commands!
    * `ls`, `ls -a`, `ls -l`, `ls -lat`, `cd`, `pwd`, and `mkdir` are some good ones to get started with.
    * You can also type `help` to bring up a list of some other useful commands.

>![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-01-11%20at%206.41.28%20PM.png)
Terminal after running a few of the commands metioned above.
# Baseline
*by Matteo Persiani*

### 1. Setup Delete any existing forks of the repository you have on your account
* First, I need to delete my old fork. Do do this I'll navigate to the settings tab of lab7 and then scroll down to the "Delete this repository" button and click it.
>![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-02-23%20at%206.44.11%20PM.png)
![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-02-23%20at%206.45.27%20PM.png)

* I also need to delete the lab7 repo from my ieng6 account so to do this I'll type `rm -rf lab7` and then `<enter>`.
>![Image](https://mapersiani.github.io/cse15l-lab-reports/IMG_8292.jpg)
`rm -rf` is a command to delete a directory without any confirmation pop ups.

### 2. Setup Fork the repository
* Next, I'll fork the repository by creating a new fork of lab7. To do this I'll click "Fork" in the top right of the lab7 repository and then "Create fork."
>![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-02-23%20at%206.43.16%20PM.png)
![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-02-23%20at%206.43.45%20PM.png)

### 3. The real deal Start the timer!
* Now I'll start a timer.
>![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-02-23%20at%206.46.24%20PM.png)

### 4. Log into ieng6
* Keys pressed: `<up><up><enter`
>![Image](https://mapersiani.github.io/cse15l-lab-reports/IMG_8291.jpg)
The `ssh cs15lwi23ads@ieng6.ucsd.edu` command gives me remote access to my ieng6 account.

### 5. Clone your fork of the repository from your Github account
* Now I need to clone the forked repo to my ieng6 account. To do this I'll copy the ssh clone code.
>![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-02-23%20at%206.51.15%20PM.png)
* I'll type `git clone` and then `<Ctrl>` + `<V>` to paste the ssh clone link.
>![Image](https://mapersiani.github.io/cse15l-lab-reports/IMG_8293.jpg)
The `git clone git@githum.com:mapersiani/lab7.git` command clones the fork onto my ieng6 account.

### 6. Run the tests, demonstrating that they fail
* Next, I need to cd into the lab7 repository and then run the tests. To do this I'll type `cd lab7` and then `<Ctrl>` + `<R>` then search "javac" to find the command from my history and `<enter>` to run the command. Next is `<Ctrl>` + `<R>` then search "java " to find the next command I need from my history and `<enter>` to run it.
>![Image](https://mapersiani.github.io/cse15l-lab-reports/IMG_8294.jpg)
The `cd lab7` command changes my current working directory to lab7 and `javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java` compiles all the .java files in the current working directory. Then, `java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests` runs the JUnit tester file and displays the errors that were returned.

### 7. Edit the code file to fix the failing test
* 
![Image](https://mapersiani.github.io/cse15l-lab-reports/IMG_8295.jpg)
![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-02-23%20at%207.01.58%20PM.png)
![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-02-23%20at%207.02.21%20PM.png)
### 8. Run the tests, demonstrating that they now succeed
![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-02-25%20at%204.31.12%20PM.jpeg)
### 9. Commit and push the resulting change to your Github account 
![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-02-25%20at%204.32.30%20PM.jpeg)

### Stop the Timer!
* 58 seconds to run all these commands, take screenshots, and write a lab report, not bad.
>![Image](https://mapersiani.github.io/cse15l-lab-reports/Screenshot%202023-02-25%20at%204.39.11%20PM.png)
# Lab Report 4
## Step 4 - Log in to ssh
![Image](logIntoSsh.png)

```
Keys pressed: <ctrl+r> <s> <s> <h> <enter>

The ssh cs15lwi23aqy@ieng6.ucsd.edu command was accessed using ctrl r, and then typing in "ssh", and pressing enter. 
```

## Step 5 - Clone your fork of the repository from your Github account
![Image](gitCloneLab7.png)

```
Keys pressed: <g><i><t><space><c><l><o><n><e><space><ctrl+v><enter>
I typed the command git clone out, and pasted the copied link of the forked repository on Github.
```

## Step 6 - Run the tests, demonstrating that they fail
![Image](runTestsLab7.png)

```
Keys pressed: <ctrl+r><c><d><l><enter><ctrl+r><j><a><v><a><c><enter><ctrl+r><j><a><v><a><ctrl+r><ctrl+r><enter>

I first found the cd lab7 command using ctrl+r to change directories into lab7. Then I used ctrl+r to find the javac command (javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java) to compile the tester. Next, I used ctrl+r again to find the (java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests.java) command to run the tester, which showed that the tests failed. 
```


## Step 7 - Edit the code file to fix the failing test
![Image](fixCodeLab7.png)

```
Keys pressed: <ctrl+r><n><a><enter> (scrolled down>) <right><backspace><2><ctrl+o><enter><ctrl+x>
```

Used the nano command to change the ListExamples.java file. 

## Step 8 - Run the tests, demonstrating that they now succeed
![Image](testsPass7.png)

```
Keys pressed: <ctrl+r><j><a><v><a><ctrl+r><ctrl+r><enter><ctrl+r><j><a><v><a><ctrl+r><ctrl+r><ctrl+r><enter>
```
I used ctrl+r to compile the tester (javac -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar *.java), and then ctrl+r again to run the tests (java -cp .:lib/hamcrest-core-1.3.jar:lib/junit-4.13.2.jar org.junit.runner.JUnitCore ListExamplesTests.java).

## Step 9 - Commit and push the resulting change to your Github account_
![Image](commitLab7.png)
![Image](pushLab7.png)

```
Keys pressed: <g><i><t><space><a><d><d><space<.><enter><g><i><t><space><c><o><m><m><i><t><space><-><m><space><"><f><i><x><e><d><enter><g><i><t><p><u><s><h> 
```


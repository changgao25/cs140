## Exercise: HelloWorld (25 Points)

The objective of this project is to familiarize yourself with 
CLion, the Integrated Development Environment (IDE) we use for 
this class, and the workflow using Git and GitHub.

The first thing you will need to do is accept **the invitation** to this assignment
from GitHub Classroom. 

Be sure that you accept the invitation first and use the URL from
the your new project when you clone it in CLion.

### Writing the code for this Project

Writing the code for this project is very simple. Since the 
objective of this assignment is understanding the workflow, 
the code is given to you. Simply create the one file below 
`main.cc` in CLion
and then copy the content into the files. 

#### main.cc

Copy and paste the following code into this file over any
contents that may already be in the `main.cc` file.

```cpp
/**
 * CS V13 * Assignment: EX01-HelloWorld
 *
 * Statement of code ownership: I hereby state that I have written all of this
 * code and I have not copied this code from any other person or source.
 *
 * @author [CHANGE THIS INFORMATION]
 */
 
#include <iostream>

int main(int argc, char *argv[]) {
    (void) argc;
    (void) argv;

    std::cout << "Hello, World!" << std::endl;
    return EXIT_SUCCESS;
}
```
### Running the code for this project

Running this code should be straightforward. In the drop-down menu in the upper
right-hand corner you should see a *Run Configuration* called `HelloWorld`. Make
sure this configuration is selected and press the play button next to it. In
the **Run** view below the code you should see the output  of running the
program. It should look something like this:

```bash
/Users/username/githubusername/ex01-helloworld/cmake-build-debug/bin/HelloWorld
Hello, World!

Process finished with exit code 0
```
Success! Now you can move on to testing your code.

### Testing the code for this project

Testing the code for this project is similar to running your code as outlined
above. In the drop-down menu in the upper right-hand corner select the
configuration `helloworld_unittest` and press the play button next to it; you
might have to press `All Configurations` to see it. In the **Run** view below
the code you should see the output of running these tests. It should look
something like this:

```bash
C:\Windows\system32\wsl.exe --distribution Ubuntu --exec "/mnt/c/Program Files/JetBrains/CLion 2024.1.3/bin/ttyfix" /bin/bash -c "export GTEST_FILTER='HelloWorldTest.Greet:HelloWorldTest/*.Greet:HelloWorldTest.Greet/*:*/HelloWorldTest.Greet/*:*/HelloWorldTest/*.Greet' && cd '/mnt/c/Users/Kira Minkova/CLionProjects/EX01-HelloWorld-V2/cmake-build-debug' && '/mnt/c/Users/Kira Minkova/CLionProjects/EX01-HelloWorld-V2/cmake-build-debug/helloworld_unittest' --gtest_color=no"
Testing started at 11:29 PM ...
Running main() from /mnt/c/Users/Kira Minkova/CLionProjects/EX01-HelloWorld-V2/cmake-build-debug/_deps/googletest-src/googletest/src/gtest_main.cc

Your unit test score is 20 out of 20
The assignment is worth a total of 25 where the remainder of 5 points
comes from grading related to documentation, algorithms, and other
criteria.

Process finished with exit code 0
```

### Submitting the code for this project
Git >>> Commit .. 
- make sure to write a meaninfull commit message. For example: "First Attempt" or "Fixed a bug(describe it)" and so on. 
- yoou might want to do a right mouse click on the file you want to add to your commit and do Git >> + Add



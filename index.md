# Week 9 Lab Report 5 - Putting it All Together
## Part 1 – Debugging Scenario 
1. Student: I get one test failed. It shows the second test has an IndexOutOfBoundsException according to "java.lang.IndexOutOfBoundsException: Index 3 out of bounds for length 3." Did I make mistake on increasing the index1 and index2? Is my logic of comparing the index to the list size incorrect? 
2. TA: Hi. You logic is correct. According to your sceenshot, there is an IndexOutOfBoundsException in the second test. You can try to draw things out when you are merging {"a", "b", "c"} and {"c", "d", "e"}. You can try to check if you are putting too much elements into the list.

3. 
terminal output

<img width="475" alt="截屏2024-03-11 下午4 36 17" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/9858a4b8-07e7-49d7-820f-dff10d8c34d3"> 

Java file

<img width="982" alt="截屏2024-03-11 下午4 36 51" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/f31d0dca-070b-4de3-855c-858999f1fa1b">

Java tester file

<img width="1006" alt="截屏2024-03-11 下午4 36 59" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/848de44b-24bc-4c48-bb15-76e0b2d1dc34"> 

bash script

<img width="875" alt="截屏2024-03-11 下午7 39 20" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/4734b591-a3b5-4a2e-a520-31cb7f21c407">

The reason of the error is `result.add(list1.get(index1));` instead of `result.add(list2.get(index2));` in line 40. It is a mistake I often make because I will copy and paste the code from the previous line and forget to change it.

## Part 2 – Reflection
I learned that using git add, git commit, git push to make a commit with the changes and push it to Github in the terminal. I also learned using jdb to run the JUnit tests to debug. I can use `stop` to stop the program at specific spot, use `locals` to check the variable, use `print` to print out the variable. The last thing I learned about vim. I can edit the file in terminal using vim by typing different shortcut notation.

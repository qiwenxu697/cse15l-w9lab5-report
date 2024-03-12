# Week 9 Lab Report 5 - Putting it All Together
## Part 1 – Debugging Scenario 
1. Student: I get one test failed. It shows the second test has an IndexOutOfBoundsException according to "java.lang.IndexOutOfBoundsException: Index 3 out of bounds for length 3." Did I make mistake on increasing the index1 and index2? Is my logic of comparing the index to the list size incorrect? 

<img width="475" alt="截屏2024-03-11 下午4 36 17" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/76bb7bc7-3114-4ce8-ad16-5f19bfe53d61">
<img width="982" alt="截屏2024-03-11 下午4 36 51" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/2a1d7acd-94b4-46f8-aeae-abb647a22a6d">
<img width="1006" alt="截屏2024-03-11 下午4 36 59" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/e19e50cc-6641-4670-b4e0-ca06827f21c7">


2. TA: Hi. You logic is correct. According to your sceenshot, there is an IndexOutOfBoundsException in the second test. Can you give an example of how the element in two arrays get merge together?
3. When I merge {"a", "b", "c"} and {"c", "d", "e"}, index1 and index2 initialize as zero. If index1 is less than the size of list1 or index2 is less then the size of list2, the smallest element in either one of the list in location index according to the number of the list. Here, "a" will be added to the result array. Next, "b" will be added. Then "c" will be added. When elements either one of the list are all adds to the result. The remaining elements in the other list will be added to the result. "c", "d", "e" will be added to the result. The reason of the error is `result.add(list1.get(index1));` instead of `result.add(list2.get(index2));` in line 40. (It is a mistake I often make because I will copy and paste the code from the previous line and forget to change it.)

4. The file & directory structure

files structure
<img width="392" alt="截屏2024-03-12 上午11 17 52" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/7a678a9f-f505-46c2-807e-3d61876e0c5e">

directory 
<img width="396" alt="截屏2024-03-12 上午11 17 40" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/267b1d2c-c565-44f0-b221-ae4ecfb0d100">

terminal output

<img width="475" alt="截屏2024-03-11 下午4 36 17" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/9858a4b8-07e7-49d7-820f-dff10d8c34d3"> 

Java file

<img width="982" alt="截屏2024-03-11 下午4 36 51" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/f31d0dca-070b-4de3-855c-858999f1fa1b">

Java tester file

<img width="1006" alt="截屏2024-03-11 下午4 36 59" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/848de44b-24bc-4c48-bb15-76e0b2d1dc34"> 

bash script

<img width="875" alt="截屏2024-03-11 下午7 39 20" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/4734b591-a3b5-4a2e-a520-31cb7f21c407">


## Part 2 – Reflection
I learned that using git add, git commit, git push to make a commit with the changes and push it to Github in the terminal. I also learned using jdb to run the JUnit tests to debug. I can use `stop` to stop the program at specific spot, use `locals` to check the variable, use `print` to print out the variable. The last thing I learned about vim. I can edit the file in terminal using vim by typing different shortcut notation.

# Week 9 Lab Report 5 - Putting it All Together
## Part 1 – Debugging Scenario 
1. Student: I get two test cases failed. It shows an "org.junit.runners.model.TestTimedOutException." Did I make mistake on creating the while loop? Is my logic of comparing the index to the list size incorrect? 

<img width="650" alt="截屏2024-03-12 下午12 46 32" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/fe97392d-4f03-4d4b-a114-7d49441ed9d2">
<img width="943" alt="截屏2024-03-12 下午12 47 26" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/3bd9baaf-4d51-48e3-a038-a48689b8cb55">
<img width="607" alt="截屏2024-03-12 下午12 49 12" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/c75c4fc0-e0ed-4be1-85f5-81a528f113ec">


2. TA: Hi. You logic is correct. According to your sceenshot, it seems that the loop never stop. Can you give an example of how the element in two arrays get merge together?
3. Student: When I merge {"a", "b", "c"} and {"c", "d", "e"}, index1 and index2 initialize as zero. If index1 is less than the size of list1 or index2 is less then the size of list2, the smallest element in either one of the list in location index according to the number of the list. The corresponding index gets increase by one. Here, "a" will be added to the result array. Next, "b" will be added. Then "c" will be added. When elements either one of the list are all adds to the result. The remaining elements in the other list will be added to the result. "c", "d", "e" will be added to the result.
The reason of the error is `index1 += 1;` is needed after line 39.

<img width="695" alt="截屏2024-03-12 下午1 14 46" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/949e8442-d84f-4c8f-a7c7-e94e5fae5abf">

5. The file & directory structure

files structure
<img width="392" alt="截屏2024-03-12 上午11 17 52" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/7a678a9f-f505-46c2-807e-3d61876e0c5e">

directory 
<img width="396" alt="截屏2024-03-12 上午11 17 40" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/267b1d2c-c565-44f0-b221-ae4ecfb0d100">

terminal output

<img width="607" alt="截屏2024-03-12 下午12 49 12" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/c61220ad-d5bb-49e7-9541-cf3da8aeb1de">

Java file

<img width="650" alt="截屏2024-03-12 下午12 46 32" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/7db22621-4fa3-4216-a23b-9cc8e5e9ad9f">

Java tester file

<img width="943" alt="截屏2024-03-12 下午12 47 26" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/d6ff29ea-220a-4b6b-adb7-500ad8319884">

bash script

<img width="988" alt="截屏2024-03-12 下午12 49 44" src="https://github.com/qiwenxu697/cse15l-w9lab5-report/assets/147675962/53d14c29-abe0-40d7-b267-5ad35111e677">

## Part 2 – Reflection
I learned that using git add, git commit, git push to make a commit with the changes and push it to Github in the terminal. I also learned using jdb to run the JUnit tests to debug. I can use `stop` to stop the program at specific spot, use `locals` to check the variable, use `print` to print out the variable. The last thing I learned about vim. I can edit the file in terminal using vim by typing different shortcut notation.

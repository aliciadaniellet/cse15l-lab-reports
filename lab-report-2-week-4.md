# Topic: Debugging
## '3 Examples of Code Changes to Fix Bugs'

---
> ## Example 1: A File with Only Image Link
<img width="1237" alt="Screen Shot 2022-04-28 at 22 48 53" src="https://user-images.githubusercontent.com/86458122/165891230-71d59605-a2e2-401c-9e47-97432b5373b8.png">

[Link](https://github.com/aliciadaniellet/cse15l-lab-reports/files/8549534/test-file2.md) to test file

Symptom discovered by looking at the output of running the failing version of the file at the command line:
<img width="798" alt="Screen Shot 2022-04-28 at 22 36 47" src="https://user-images.githubusercontent.com/86458122/165891142-ded83e77-e0a0-4f36-8c4f-0c94a54bd9df.png">

Conclusion: 
The result is that we still retrieve the image when we only want to get the links, not images. As image link in a MarkDown file has similar format to a normal link, the image link still gets printed. Thus, I added a condition where it should return an empty array if the file only contains an image link.

---

> ## Example 2: A File with No Parentheses 
<img width="1246" alt="Screen Shot 2022-04-28 at 23 48 04" src="https://user-images.githubusercontent.com/86458122/165897025-0fe6617a-b61c-48fd-9edd-26dc1ff8b39a.png">

[Link](/Users/alicia/Documents/GitHub/cse15l-lab-reports/test-file1.md) to test file

Symptom discovered by looking at the output of running the failing version of the file at the command line:
<img width="777" alt="Screen Shot 2022-04-28 at 23 45 06" src="https://user-images.githubusercontent.com/86458122/165897041-e66eac9c-0f5f-4ec7-a414-9482ea3a41cc.png">

Conclusion: 
The result is that the terminal goes through infinite loop because it will continuously search for the next open parentheses. Thus, to fix this error, I added a condition to break the while loop if we cannot find the next open parentheses after the close bracket is found.

 ---

> ## Example 3: A File with No Links
<img width="1260" alt="Screen Shot 2022-04-24 at 05 06 50" src="https://user-images.githubusercontent.com/86458122/164975639-75e56752-08fc-4272-82fa-c5c2c3123adc.png">

[Link](/Users/alicia/Documents/GitHub/cse15l-lab-reports/test-file3.md) to test file

Symptom discovered by looking at the output of running the failing version of the file at the command line:
<img width="658" alt="Screen Shot 2022-04-24 at 05 01 15" src="https://user-images.githubusercontent.com/86458122/164975714-eefa71cc-f8a1-46c3-b6e8-cb9348539dfd.png">

Conclusion:
The result is a StringIndexOutOfBoundsException for the failing version of the file because the file cannot find the next '['. To fix this error, I added an if statement where the condition is to break the while loop when there is no "[" in the file, thus returning an empty array list and the code runs correctly in the terminal.

# Topic: Debugging
## '3 Examples of Code Changes to Fix Bugs'

---
> ## Example 1: A File with Only Image Link


[Link](https://github.com/aliciadaniellet/cse15l-lab-reports/files/8549534/test-file2.md) to test file
<img width="1237" alt="Screen Shot 2022-04-28 at 22 48 53" src="https://user-images.githubusercontent.com/86458122/165891230-71d59605-a2e2-401c-9e47-97432b5373b8.png">

Symptom discovered by looking at the output of running the failing version of the file at the command line:
<img width="798" alt="Screen Shot 2022-04-28 at 22 36 47" src="https://user-images.githubusercontent.com/86458122/165891142-ded83e77-e0a0-4f36-8c4f-0c94a54bd9df.png">

Conclusion: 
The result is that we still retrieve the image when we only want to get the links, not images. As image link in a MarkDown file has similar format to a normal link, the image link still gets printed. Thus, I added a condition where it should return an empty array if the file only contains an image link.

---

> ## Example 2: A File with Blank Line
<img width="1140" alt="Screen Shot 2022-04-24 at 04 50 34" src="https://user-images.githubusercontent.com/86458122/164975202-743cf093-000a-45d5-b0f2-cefcba8e8d6a.png">

[Link](/Users/alicia/Documents/GitHub/cse15l-lab-reports/test-file1.md) to test file

Symptom discovered by looking at the output of running the failing version of the file at the command line:
<img width="660" alt="Screen Shot 2022-04-24 at 04 37 35" src="https://user-images.githubusercontent.com/86458122/164975228-f53800d3-e4f8-43b9-8926-45436e4b7f67.png">

Conclusion: 
The result is an OutOfMemoryError for the failing version of the file because the file will continue to loop until it runs out of memory to search for the next '['. We discovered that there is one extra line which is empty at the end of the file, thus we deleted the line and the code runs correctly in the terminal. 

 ---

> ## Example 3: A File with No Links
<img width="1260" alt="Screen Shot 2022-04-24 at 05 06 50" src="https://user-images.githubusercontent.com/86458122/164975639-75e56752-08fc-4272-82fa-c5c2c3123adc.png">

[Link](/Users/alicia/Documents/GitHub/cse15l-lab-reports/test-file3.md) to test file

Symptom discovered by looking at the output of running the failing version of the file at the command line:
<img width="658" alt="Screen Shot 2022-04-24 at 05 01 15" src="https://user-images.githubusercontent.com/86458122/164975714-eefa71cc-f8a1-46c3-b6e8-cb9348539dfd.png">

Conclusion:
The result is a StringIndexOutOfBoundsException for the failing version of the file because the file cannot find the next '['. To fix this error, we added an if statement where the condition is to break the while loop when there is no "[" in the file, thus returning an empty array list and the code runs correctly in the terminal.

# Topic: Debugging
## '3 Examples of Code Changes to Fix Bugs'

---

> ## Example 1
<img width="1142" alt="Screen Shot 2022-04-24 at 04 07 49" src="https://user-images.githubusercontent.com/86458122/164973530-f4efd5c1-6562-4fda-981f-66170a7cf36d.png">

[Link](https://github.com/aliciadaniellet/cse15l-lab-reports/files/8549534/test-file2.md) to test file

Symptom discovered by looking at the output of running the failing version of the file at the command line:
<img width="647" alt="Screen Shot 2022-04-24 at 04 20 20" src="https://user-images.githubusercontent.com/86458122/164973958-6bc86a51-6028-48a2-a48f-b3baed1b65c9.png">

Conclusion: 
The result is an OutOfMemoryError for the failing version of the file because the file will continue to loop until it runs out of memory to search for the next '['. We discovered that we did not use the proper markdown syntax for the link, thus we corrected the markdown syntax and the code runs correctly in the terminal. 


> ## Example 2
<img width="1140" alt="Screen Shot 2022-04-24 at 04 50 34" src="https://user-images.githubusercontent.com/86458122/164975202-743cf093-000a-45d5-b0f2-cefcba8e8d6a.png">

[Link](https://github.com/aliciadaniellet/cse15l-lab-reports/files/8549589/test-file.md) to test file

Symptom discovered by looking at the output of running the failing version of the file at the command line:
<img width="660" alt="Screen Shot 2022-04-24 at 04 37 35" src="https://user-images.githubusercontent.com/86458122/164975228-f53800d3-e4f8-43b9-8926-45436e4b7f67.png">

Conclusion: 
The result is an OutOfMemoryError for the failing version of the file because the file will continue to loop until it runs out of memory to search for the next '['. We discovered that there is one extra line which is empty at the end of the file, thus we deleted the line and the code runs correctly in the terminal. 


> ## Example 3
<img width="1260" alt="Screen Shot 2022-04-24 at 05 06 50" src="https://user-images.githubusercontent.com/86458122/164975639-75e56752-08fc-4272-82fa-c5c2c3123adc.png">

[Link](https://github.com/aliciadaniellet/cse15l-lab-reports/files/8549613/other-file.md) to test file

Symptom discovered by looking at the output of running the failing version of the file at the command line:
<img width="658" alt="Screen Shot 2022-04-24 at 05 01 15" src="https://user-images.githubusercontent.com/86458122/164975714-eefa71cc-f8a1-46c3-b6e8-cb9348539dfd.png">

Conclusion:
The result is a StringIndexOutOfBoundsException for the failing version of the file because the file cannot find the next '['. To fix this error, we added an if statement where the condition is to break the while loop when there is no "[" in the file, thus returning an empty array list and the code runs correctly in the terminal.

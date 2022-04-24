# Topic: Debugging
## '3 Examples of Code Changes to Fix Bugs'

---

> ## Example 1
<img width="1142" alt="Screen Shot 2022-04-24 at 04 07 49" src="https://user-images.githubusercontent.com/86458122/164973530-f4efd5c1-6562-4fda-981f-66170a7cf36d.png">

[Link](https://github.com/aliciadaniellet/cse15l-lab-reports/files/8549534/test-file2.md) to test file

Symptom discovered by looking at the output of running the failing version of the file at the command line
<img width="647" alt="Screen Shot 2022-04-24 at 04 20 20" src="https://user-images.githubusercontent.com/86458122/164973958-6bc86a51-6028-48a2-a48f-b3baed1b65c9.png">

Conclusion: 
The result is an OutOfMemoryError for the failing version of the file because the file will continue to loop until it runs out of memory to search for the next '['. We discovered that we did not use the proper markdown syntax for the link, thus we corrected the markdown syntax and the code runs correctly in the terminal. 


> ## Example 2

# Lab Report 5

I found the tests with different results by searching it through manually in the test-files folder. 

Link to the test files:
> 494.md
* [link to test file 1](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/494.md)

> 519.md
* [link to test file 2](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/519.md)

---
> ## Test file 1 : 494.md
My output:

![image](https://user-images.githubusercontent.com/86458122/171515128-359562d2-f3d7-4fdf-a670-5e129e3648c5.png)

Provided repository output:

![image](https://user-images.githubusercontent.com/86458122/171515133-c9c2a160-9b9c-4abc-b043-b70c8ded0639.png)

Actual output:

![image](https://user-images.githubusercontent.com/86458122/171515168-ec99e453-7601-4b28-838c-661ffd57aeb9.png)

Both my output and the provided repository output gave the wrong output as the output should actuallty be *[(foo)]*.


Part of my code that has error:


![image](https://user-images.githubusercontent.com/86458122/171515163-30fee906-8244-4ffe-8e2a-687c61101027.png)

Description of bug and how to fix it: I believe that the bug comes from the fact that I do not consider when there is an event where a code is in between more than one complete brackets. A condition of counting the brackets and checking the code between the brackets should be made to fix the error.

---

> ## Test file 2 : 519.md
My output:

![image](https://user-images.githubusercontent.com/86458122/171516706-166ee210-4a79-4844-aed4-c8aafd98c4ae.png)

Provided repository output:

![image](https://user-images.githubusercontent.com/86458122/171516695-fb9ae7c5-7129-4613-b8e7-1ef24a6130c5.png)

Actual output:

![image](https://user-images.githubusercontent.com/86458122/171516705-a27172e3-b035-4f5c-b194-7e2d14631415.png)

Both my output and the provided repository output gave the wrong output as the output should actuallty be an empty bracket *[]*, since there is no resulting link.


Part of my code that has error:


![image](https://user-images.githubusercontent.com/86458122/171516708-1673751b-b75c-43d5-badf-b3b493f05c6e.png)

Description of bug and how to fix it: I believe that the bug comes from this specific part of my code, before the if statement found on the picture above. I should have put a condition where if "!" is found in any index of the substring, the while loop should just break right away.

---


# Lab Report 4

Link to [Markdown Repository](https://github.com/aliciadaniellet/markdown-parser)

Link to [Week 7 Reviewed Respository](https://github.com/aliciadaniellet/ednafiles)

---
> ## Snippet 1
Expected output:

![image](https://user-images.githubusercontent.com/86458122/169418300-9968e4a8-c6b8-4805-8b4e-51d52803e849.png)

Test case for Snippet 1:

![image](https://user-images.githubusercontent.com/86458122/169418305-1e91968b-daea-4e25-95a9-a4d40828d381.png)

Output from *my implementation*:

![image](https://user-images.githubusercontent.com/86458122/169418312-3e5c6c88-29f7-497e-aea5-82f4878a633e.png)

Output from *implementation reviewed in week 7*:

![image](https://user-images.githubusercontent.com/86458122/169418317-3e5fb17e-c01c-473f-950c-e042cd15e6ba.png)

Opinion: I believe that there will be more than just a small (<10) code change that will make my program work for snippet 1. I will need to put a lot of conditions (if statements) considering the backticks positions in order for my program to work. 

---

> ## Snippet 2
Expected output:

![image](https://user-images.githubusercontent.com/86458122/169418432-baf755da-d0b0-40c1-87cd-49358ff9b279.png)

Test case for Snippet 2:

![image](https://user-images.githubusercontent.com/86458122/169418433-e464ee87-674b-4464-9cad-2c44040ae864.png)

Output from *my implementation*:

![image](https://user-images.githubusercontent.com/86458122/169418437-8c60c72e-175c-41e0-938a-b8ab50776a16.png)

Output from *implementation reviewed in week 7*:

![image](https://user-images.githubusercontent.com/86458122/169418439-aca87e6e-ca36-4caf-a61b-c7b79a7b352b.png)

Opinion: I believe that there will be more than just a small (<10) code change that will make my program work for snippet 2. I can make a condition where every open bracket must have a close bracket, and every open parentheses must have a close parentheses. Then I can count the number of nested brackets and nested parentheses. I should then make more conditions in order to be able to retrieve the each link from the nested brackets and parentheses.

---

> ## Snippet 3
Expected output:

![image](https://user-images.githubusercontent.com/86458122/169418464-9c9584dd-e236-48e7-a4bd-111b8907257e.png)

Test case for Snippet 3:

![image](https://user-images.githubusercontent.com/86458122/169418468-0d5da312-7544-4bf9-bcb4-bfdaadae0f78.png)

Output from *my implementation*:

![image](https://user-images.githubusercontent.com/86458122/169418467-f4c419be-bb95-4151-8f7d-8c7852ea5993.png)

Output from *implementation reviewed in week 7*:

![image](https://user-images.githubusercontent.com/86458122/169418470-4e8cac24-fe3d-41b0-bb95-e9be3c912fae.png)

Opinion: I believe that there can just be a small (<10) code change that will make my program work for snippet 3. I can first remove all unwanted spaces and lines in the file, then check if all open bracket has a close bracket and all open parentheses has a close parentheses. I can make a condition to count the number of characters in the string so it does not exceed a certain limit so link will not be retrieved if it exceeds the limit.
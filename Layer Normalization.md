# **BEFORE UNDERSTANDING LAYER NORMALIZATION, LETS HAVE A LOOK AT BATCH NORMALIZATION FIRST:**

![image](https://github.com/user-attachments/assets/1bc3c29e-1b46-4510-8801-d757267fa744)

* **TO FIND THE MEAN AND STD, WE COMPUTE IT COLUMN WISE:**

![image](https://github.com/user-attachments/assets/d5d4430f-2a4d-4aea-bfb5-4203a6043cb6)

--------------------

# **WHY WE CAN'T USE BATCH NORMALIZATION IN SEQUENTIAL DATA AS COMPARED TO LAYER NORMALIZATION?**
**ANSWER: For example, we have 2 sentences, one sentence has 100 words while the other sentence has 30 words, as we need to pad the second sentence to make its length equal to 100 words, due to the presence of unnecessary zeros, the calculated mean and std. will never be correct because they are getting disturbed due to those zeros, so that's why we can't use batch normalization in case of SEQUENTIAL DATA**  
![image](https://github.com/user-attachments/assets/84abe90f-a732-4ad3-88f0-bd1f9a2b58a5)


---------------------------

# **LAYER NORMALIZATION:**


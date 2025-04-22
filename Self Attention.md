In case of WORD EMBEDDINGS, we receive static embeddings. The word static means, they are made once, and used as many time we want. But the problem is that the numerical representation (THE EMBEDDINGS) should be changed as per the context.

* Lets say, after using WORD EMBEDDINGS we receives a vector [0.9, 0.3] --> 0.9 indicates (FRUIT) while 0.3 indicates (technology)

* Now i want to convert my sentences to numerical form, but as my sentences are more biased towards the technology rather than fruits, the vector [0.9, 0.3] cannot change dynamically to lets say [0.5, 0.8], so to fix this problem we use `SELF ATTENTION`

* `NOW SELF ATTENTION WILL PROVIDE US contextual embeddings RATHER THAN static embeddings`

* `IT TAKES static embeddings & RETURNS contextual embeddings`  

![image](https://github.com/user-attachments/assets/e46f23ad-372b-435c-b9d3-515b6893188c)


---------------------

Let's say we have these 2 sentences:

* If we use static embeddings, the value for the word BANK will always be same, although it is being used in different contexts
  
![image](https://github.com/user-attachments/assets/f9c23d95-a6c4-4e27-a26e-d07224a5ff07)

* `THE SOLUTION IS TO ASSIGN NUMBERS TO EACH WORD BASED ON ITS CONTEXT, WE CAN READ IT LIKE: [the new_embedding of money is 0.7 times the old_embedding of money]  TO DO THIS, WE NEED TO PERFORM DOT PRODUCT`

![image](https://github.com/user-attachments/assets/8be6f83a-a823-4f31-b07d-bb0f1bba7846)

--------------------

![image](https://github.com/user-attachments/assets/d5a156a5-c274-4042-b161-827da85a85a7)
![image](https://github.com/user-attachments/assets/67afc6cd-1e04-4fca-9d08-16f7522a2f46)








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



---------------------------

The above operation can be executed in parallel:

* ``NOTE: THERE IS NO LEARNING IN THIS PROCESS BECAUSE THERE ARE NO WEIGHTS/BIASES INVOLVED IN IT --- DUE TO THIS REASON, THIS APPROACH IS GENERATING ONLY [GENERAL EMBEDDINGS], THEY ARE NOT TASK SPECIFIC EMBEDDINGS``

* ``TO MAKE THE EMBEDDINGS -- TASK SPECIFIC, WE NEED TO INTRODUCE LEARNABLE PARAMETERS``
![image](https://github.com/user-attachments/assets/f30f8658-0d33-49a0-abb8-837262e9ed2a)


-------------------------

In the above approach, the GREEN, PINK & BLUE BOXES are acting as QUERY, KEY & VALUE

* ``GREEN ASKS PINK, TELL ME HOW MUCH SIMILARITY IS BETWEEN YOU AND ME``

* ``This is how we will replace the boxes with the appropriate vectors (QUERY, KEY & VALUE)``
![image](https://github.com/user-attachments/assets/0754e12b-fcf4-40c5-ae24-fdfb53d1e781)

----------------------

TO GET THOSE 3 NEW VECTORS (QUERY, KEY & VALUE) WE NEED TO USE SOME TECHNIQUE TO MAKE 3 NEW VECTORS FROM 1 OLD VECTOR. THIS TECHNIQUE COULD BE [linear transformation], WHERE WE MULTIPLY A VECTOR WITH A MATRIX.

* ``But what should be the values inside those matrices? --- we will initialize them with random values and backpropagation will give us the best values``

![image](https://github.com/user-attachments/assets/92e68792-176c-4281-95b3-aaa338c4b9ac)

----------------------

BELOW IS THE FINAL WORKFLOW TO GET THE CONTEXTUAL EMBEDDINGS:

``WHILE READING, REFER THE 3RD LAST IMAGE``

* ``We take our General Word Embeddings (yellow box), DOT PRODUCT it with the matrices to get 3 new vectors (QUERY, KEY & VALUE), we then applied SOFTMAX on the GREEN & PINK vectors and then performed WEIGHTED SUM TO GET CONTEXTUAL EMBEDDINGS``

![image](https://github.com/user-attachments/assets/03b4f342-d77e-4f05-a1f0-e1da9f0f4b98)

----------------------



![image](https://github.com/user-attachments/assets/e7fa6225-0420-428c-9ed5-dc50c14ab624)


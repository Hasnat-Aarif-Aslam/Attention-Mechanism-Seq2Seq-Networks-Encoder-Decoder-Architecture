# **Why Positional Encoding Is Needed:**

* The core attention mechanism looks at the entire input sequence as a set of vectors—it doesn’t know which word comes first, second, or third. Without any extra information, it treats “I love you” the same as “you love I.”

* In natural language (and many other sequences), the order of items matters. “The cat chased the mouse” ≠ “The mouse chased the cat.” To distinguish these, the model needs to know each token’s position.

-------------

* **We could use sine curve for this problem, but due to its periodic nature, there are still chances that different words could have same sine value (IF DIFFERENT POSITIONS HAVE THE SAME VALUES, IT MEANS THEIR POSITIONS ARE ALSO SAME, BUT WE DONT WANT THIS)**

![image](https://github.com/user-attachments/assets/edf5bff7-a93a-4838-a2e0-4ac6b83ad522)

* We can concatenate the values at the end of the embedding vector
  
![image](https://github.com/user-attachments/assets/5ee44289-957b-4721-bc14-bcb529fb8275)

----------------

* **To solve the periodic nature problem, we can use 1 more trignometric function to reduce the likeliness of getting the same values**

* **Let's say we used sin and cos functions, now we will get 2 values for each word's position (ONE FROM SIN AND ONE FROM COS). It means we now have a vector for each position**

* BUT THERE ARE STILL CHANCES THAT WE MIGHT GET THE SAME VALUES FOR DIFFERENT POSITIONS.

![image](https://github.com/user-attachments/assets/8e4b4753-797a-45ec-9bbb-77b741d260a8)

------------------

* TO HANDLE THE LIKELINESS, WE CAN FURTHER ADD MORE CURVES:

* ``As we have 4 functions now, our vector will have 4 values for each word``

![image](https://github.com/user-attachments/assets/807b2bc4-4907-446c-a89c-cee99bcc459e)
![image](https://github.com/user-attachments/assets/2773b22e-c650-40ef-835e-b0b5436aade9) 

-----------------

* ``SIMILARLY WE CAN INCREASE THE FUNCTIONS AS MUCH AS WE WANT TO REDUCE THE PROBABILITY FURTHER``


-----------------------------

``**THIS IS HOW THE ORIGINAL POSITIONAL ENCODING IF DONE:**``

![image](https://github.com/user-attachments/assets/1487c3ed-af59-40ab-a041-a59b76caf1b8)

* RATHER THAN CONCATENATION, WE PERFORM VECTOR ADDITION BETWEEN THE EMBEDDING AND POSITIONAL ENCODED VECTOR TO GET THE SAME DIMENSION VECTOR (1,6 IN OUR CASE), IF WE USE CONCATENATION, IT WILL INCREASE THE DIMENSIONALITY -- LEADING TO AN INCREASE IN THE PARAMETERS
![image](https://github.com/user-attachments/assets/3c50a5a6-69eb-4e8a-8828-4f01e8dcf1db)

---------------

# **BUT HOW TO CALCULATE THE POSITIONAL ENCODED VALUES?**
  
![image](https://github.com/user-attachments/assets/718da9fc-72d7-4922-893f-34805bb77d88)

![image](https://github.com/user-attachments/assets/37efa077-5c47-4275-9208-4b27ecff0ed4)

----------------------

``THIS IS HOW THE 128-DIMENSIONAL POSITIONAL ENCODED VECTOR FOR 50 WORDS LOOKS LIKE USING A HEATMAP:``
![image](https://github.com/user-attachments/assets/c4d09c49-88b7-450b-989e-bd36b247d9d3)



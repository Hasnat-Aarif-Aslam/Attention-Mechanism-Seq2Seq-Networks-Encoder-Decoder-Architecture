**Before understanding Multi Head Attention, the Self Attention has 1 limitation:**
* It can model only one pattern of relationships at a time.

For example, the below sentence has two meanings, but SELF ATTENTION can capture only one pattern at a time

![image](https://github.com/user-attachments/assets/0ea8a686-8549-4343-97b6-4bd748514c96)

--------------------------

**This is how SELF ATTENTION works:**
* We can clearly see that there is only 1 set of weights due to which it capture only one pattern of relationships at a time.
  
![image](https://github.com/user-attachments/assets/037b122c-e372-44eb-af2d-1fe895d7efc6)

When it comes to MULTI-HEAD ATTENTION:
* We use multiple set of weights


* **``2 set of weights for embedding_money and 2 for embedding_bank``**
![image](https://github.com/user-attachments/assets/0b5e65be-a711-439f-8d9c-bd7fc1fd0041)

* **``Performing the next operations twice, once with (1st set of Q, K and V) and (once with 2nd set of Q, K and V)``**
![image](https://github.com/user-attachments/assets/3fc9e477-2702-4ab9-87d1-bafb1843ef62)

* **``Similarly for embedding_bank``**
![image](https://github.com/user-attachments/assets/fbc203c5-fb9f-4fbb-8d3e-6cd3b09f1518)

* **WE CAN USE AS MUCH PARALLEL ATTENTION LAYERS AS WE WANT**
![image](https://github.com/user-attachments/assets/fd7566bb-6b56-4dee-adde-a250bf7dc71e)



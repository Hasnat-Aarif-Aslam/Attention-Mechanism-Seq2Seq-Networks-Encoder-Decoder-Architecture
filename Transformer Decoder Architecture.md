# **Architecture of Decoder**
* These 4 steps happen first:

![image](https://github.com/user-attachments/assets/a577fd80-d82b-42be-9b88-36d53afdfd99)

# **We are focusing on that how ``DECODER`` works during ``TRAINING``, We already know that it behaves like a ``NON-AUTOREGRESSIVE-MODEL`` during ``TRAINING``** 
* ``5 more decoer layers indicates that as per the paper they used a total of 6 ENCODERS and 6 DECODERS``
* ``Lets say there are total of 50000 samples present in the dataset, to find how many neurons there will be in the FFNN, it depends on the vocabulary (unique words) present in the HINDI dataset (as we are doing ENGLISH -> HINDI translation, so vocabulary of HINDI). Lets say there are 10k unique words, so there will be 10k neurons in FFNN``

![image](https://github.com/user-attachments/assets/6bf87b88-6623-4a91-bbbb-46fb665be3e1)
![image](https://github.com/user-attachments/assets/d5da73cf-b225-4572-bc48-ba27b32d39f9)
![image](https://github.com/user-attachments/assets/16e59b24-0c87-4c43-9a75-747a53de9412)
![image](https://github.com/user-attachments/assets/e15cab21-abe5-4641-8826-faefdb90f14a)
![image](https://github.com/user-attachments/assets/0ed31364-1da7-4acc-bf57-081e1d2ff3ce)
![image](https://github.com/user-attachments/assets/98e1d350-fb6d-4cc1-921e-ae760a14ad04)
![image](https://github.com/user-attachments/assets/c4aaebe7-b5b5-47f1-8796-391cfea557bd)
![image](https://github.com/user-attachments/assets/1ee617bb-aaf5-4463-891a-041bfca9a5d3)
![image](https://github.com/user-attachments/assets/74c8c53b-9a77-40c0-a777-176ee079a027)
![image](https://github.com/user-attachments/assets/9dd83877-1544-4c92-98b3-10f279f90e9b)




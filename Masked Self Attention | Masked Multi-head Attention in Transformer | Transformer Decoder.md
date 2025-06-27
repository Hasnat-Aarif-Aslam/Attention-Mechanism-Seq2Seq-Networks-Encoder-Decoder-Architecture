# **GOLDEN WORDS: ALL SEQ-TO-SEQ MODELS ARE AUTO-REGRESSIVE MODELS**

``AUTO-REGRESSIVE MODELS: A CLASS OF MODELS THAT GENERATE DATA POINTS IN A SEQUENCE CONDITIONING EACH NEW POINT ON THE PREVIOUSLY GENERATED DATA POINTS.``

# **CAN YOU GIVE US A PROOF?**
* Even in the simplest ENCODER-DECODER model, we need to (give the model previously generated output token as an input, so that it can understand and generate the next word based on it) in the DECODER

![image](https://github.com/user-attachments/assets/45bc1568-df5f-4c3e-8a96-4b113dd5759b)
-----------------------------

# **The change in the behaviour, AUTO-REGRESSIVE & NON-AUTO-REGRESSIVE is just due to MASKED SELF-ATTENTION**

![image](https://github.com/user-attachments/assets/7ae2751d-39e3-4f2c-8164-8e84a9fedc1d)

-----------------------------

# **WHY KEEPING INFERENCE AS AUTO-REGRESSIVE AND TRAINING AS NON-AUTO-REGRESSIVE?**
* **INFERENCE: Let's say we input a sentence (I am fine) in ENCODER, now we need to have its translation. The encoder will give us some CONTEXT-VECTOR, which will  be given to the DECODER, BUT DURING INFERENCING, WE NEED TO GIVE THE DECODER EACH OUTPUT TOKEN AS AN INPUT SO IT CAN UNDERSTAND AND GENERATE THE NEXT WORD, so here we strictly need to follow ``AUTO-REGRESSIVE BEHAVIOUR``**

![image](https://github.com/user-attachments/assets/60d09f31-bdd8-46da-ae71-eb3c7215161f)

* **TRAINING: DURING TRAINING, WE CAN EITHER MAKE IT BEHAVE AS AN AUTO-REGRESSIVE/NON-AUTO-REGRESSIVE MODEL --> as we know that during training we use the concept of ``TEACHER FORCING (Rather than giving the decoder generated word during training, we always give it the correct word from our training data so it can fastly learn its mistakes during backpropagation)``, as we don't need to wait and input the previously generated word, so we don't need to follow AUTO-REGRESSIVE behaviour ``(AS FOLLOWING THE AUTO-REGRESSIVE BEHAVIOUR CAUSES A HUGE INCREASE IN TRAINING TIME)``**

![image](https://github.com/user-attachments/assets/1a0912b4-deeb-425e-b265-960c7d6371ae)


---------------------------------

# **Masked Self-Attention**

* ``During Self-Attention process, as we know the equation looks like this -- WE NEED 0.8% THIS WORD, 0.1% THIS WORD AND 0.1% THIS WORD TO CALCULATE THE CONTEXTUAL EMBEDDING OF THAT WORD. SIMILARLY FOR OTHRE WORDS``

* ``The problem here is that when we have only the first word, we are trying to calculate the 0.1% and 0.1% too (CALCULATING THE VALUES FOR THE FUTURE WORDS), this future words calculation causes the DATA LEAKAGE.``

* ``So we need to do something to make the values for these words zero -- when calcualting the CONTEXTUAL EMBEDDING of FIRST WORD -- we should calculate the value for first word only, when calculating the value for second word, we should only use the first and second word and vice versa`` **TO DO THIS, CHECK THE 4th IMAGE**

# BELOW IS THE SAME PREVIOUS SELF ATTENTION PROCESS:

![image](https://github.com/user-attachments/assets/fd312c01-082b-43b2-bfcf-96a44110c1d7)

![image](https://github.com/user-attachments/assets/d90a3c7d-be03-44ba-b5f3-cfa58f3544dc)

![image](https://github.com/user-attachments/assets/32ab4a3a-d9a7-4d86-bebd-afc3a0625d9c)

**HERE WE CAN SEE, WE JUST ADDED A MASK (A MATRIX OF THE SAME SIZE) WITH -inf VALUES AT THE PLACE WHERE WE NEED TO MAKE THE VALUES ZERO**

![image](https://github.com/user-attachments/assets/33d3107e-491a-4ea2-b0f1-b3bfcb65e59e)




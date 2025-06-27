**What it does: Uses a small neural network (an “additive” MLP) to compare the decoder’s current state with each encoder output, producing a score for each source token.**

* **As discussed before, we want to calculate the alpha's_ ``AKA, ALIGNMENT SCORES``.**

* ``TOTAL ALPHA'S: WORDS IN INPUT SENTENCE * WORDS IN OUTPUT SENTENCE``

* ``RATHER THAN PROVIDING ONLY CONTEXT VECTOR TO DECODER, THE DECODER HAS ACCESS TO ALL THE ALIGNMENT SCORES (EXAMPLE: c_1, c_2, c_3, c_4) TO FIND WHICH WORD AT ENCODER LEVEL IS MORE IMPORTANT DURING DECODING``

![image](https://github.com/user-attachments/assets/5472ade3-fdba-4046-9a55-80519430e958)

----------

 
# **Bahdanau Attention**

* **h_0, h_1, h_2, h_3 are 4-d vectors, similarly s_0, s_1, s_2, s_3 is also 4-d**
 
* **To calculate alignment scores, we need to input s_0 to s_3 and h_0 to h_3 to an ANN ``(ALIGNMENT MODEL)`` to find the values for alignment scores**

![image](https://github.com/user-attachments/assets/e4a70c95-43ac-475c-9299-bf27f490a28b)

* **we will input that 4x8 matrix into ANN ``(ALIGNMENT MODEL)``, which will give us 4*1 matrix, ``(These will be the alignment scores [alpha_])``. Now we will use them to calculate ```c_1, c_2, c_3, c_4`` values**

![image](https://github.com/user-attachments/assets/3e1a520b-4b48-4a4b-b6c2-85796b9b26ed)

 

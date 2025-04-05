**Lets say we have small encoder-decoder architecture, it has two issues:**

* **Lets say we have a big paragraph (>25 words), as a human try to look at it, then close your eyes and translate it into hindi without opening your eyes, ``(We will fail to do so because its difficult for us to process and remember things in one sight)`` This is the same issue with the Encoder-Decoder, when it tries to create a context vector based on that paragraph, there is too much burden on it to represent a something huge in very less set of numbers due to which it fails to remember things accurately**

* **Second is, when this context vector goes to Decoder, the decoder does not know which word it exactly needs to generate the translation, For example: (I will do it) (Ma karun ga), the decoder does not knows that to translate ``do into karun`` it only needs the word ``do``, so if there will be some technique that helps it focus on those necessary words only, then it can boost the performance ``here comes the Attention Mechanisms!``**

![image](https://github.com/user-attachments/assets/2668b468-cb30-490c-9a07-bba6d1065ba9)

---------

* **In case of Vanilla E-D, we need two things at every time step: ``[y_i - 1, s_i - 1]`` ``y_i - 1 is previous output of decoder, s_i - 1 previous hidden state of decoder``**

* **In case of Attention Mechanism, we need three things at every time step: ``[y_i - 1, s_i - 1, c_i]`` ``y_i - 1 is previous output of decoder, s_i - 1 previous hidden state of decoder, c_i tells that at current time step of decoder, which hidden state of Encoder is useful``**

* ``c_i is a vector as there could be more than 1 important words for a current time step, for example: c_i --> [h1, h2] it means these 2 hidden states are useful for the current time step``

* ``c_i WILL BE CALCULATED USING WEIGHTED SUM``

 
![image](https://github.com/user-attachments/assets/c5569d9d-0dff-41a8-b6b3-668a80ac257f)

-----------

* To identify which hidden state/states are important ``c_1``, we need weighted sum, it will use ANN as a function to get the values for alpha_

![image](https://github.com/user-attachments/assets/9113cca7-e56a-4d84-a557-18899999caeb)

------------

* To calculate c_i, we will use s_i and h_i which will give us alpha_, so we will form the complete equation and get the value as shown for c_2:
  
![image](https://github.com/user-attachments/assets/935c8a0f-563f-416e-a415-fa6f60e2a888)

------------

# ``We can also plot these alpha's, because they are showing the importance:``

![image](https://github.com/user-attachments/assets/7a6c9c35-c112-42f3-ba98-a82ea04fef78)



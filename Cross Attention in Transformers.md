# **Multi-Head-Attention:**

![image](https://github.com/user-attachments/assets/4e1191e4-2bc4-43f4-9200-198fd0426a0f)

# **Cross-Attention**

![image](https://github.com/user-attachments/assets/e05d6971-5a77-48b1-8822-640419eb9e41)


# **What is Self Attention?**
* When we want to find the similarity among the words of the same sequence.

Example: In the sentence “The dog chased the cat,” when focusing on “dog,” self-attention lets the model look at “The,” “dog,” “chased,” “the,” and “cat” — all within that one sentence — to build its understanding.


# **What is Cross Attention?**
* When we want to find the similarity among the words of two different sequences.

Example: In a translation model, when generating the French word for “dog,” cross-attention lets the French decoder look at the English encoder’s outputs (“The,” “dog,” “chased,” “the,” “cat”) to decide which source words are most relevant.

![image](https://github.com/user-attachments/assets/44ebfb36-1642-43fb-83a5-c07632635f9a)


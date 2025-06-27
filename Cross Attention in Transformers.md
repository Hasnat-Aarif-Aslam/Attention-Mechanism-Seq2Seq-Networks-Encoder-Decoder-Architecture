# **Multi-Head-Attention:**

![image](https://github.com/user-attachments/assets/4e1191e4-2bc4-43f4-9200-198fd0426a0f)

# **Cross-Attention**

![image](https://github.com/user-attachments/assets/e05d6971-5a77-48b1-8822-640419eb9e41)


# **What is Self-Attention?**
* When we want to find the similarity among the words of the same sequence.

Example: In the sentence “The dog chased the cat,” when focusing on “dog,” self-attention lets the model look at “The,” “dog,” “chased,” “the,” and “cat” — all within that one sentence — to build its understanding.

![image](https://github.com/user-attachments/assets/aa2a3dc7-af5e-4a3e-a3ce-ad436bd29a08)


# **What is Cross Attention?**
* When we want to find the similarity among the words of two different sequences.

Example: In a translation model, when generating the French word for “dog,” cross-attention lets the French decoder look at the English encoder’s outputs (“The,” “dog,” “chased,” “the,” “cat”) to decide which source words are most relevant.

![image](https://github.com/user-attachments/assets/44ebfb36-1642-43fb-83a5-c07632635f9a)

# **Differences in Self Vs. Cross Attention**
**Inputs:**
* Self-Attention only needs a  single sequence embeddings/contextual embeddings
* Cross-Attention needs both sequences so it can draw a relationship between two different sequence embeddings/contextual embeddings

![image](https://github.com/user-attachments/assets/3007cd4b-3213-49fe-9609-876a734b405c)

**Processing (Self-Attention):**

![image](https://github.com/user-attachments/assets/85addb34-58bd-4f78-9757-e884928e0fd6)
![image](https://github.com/user-attachments/assets/69d953fa-991e-4585-9d17-8f7ba8ce7e8f)

**Processing (Cross-Attention):**
* As we know, it uses both sequences (in our case, Hindi & English), so the QUERY vector will be created based on the OUTPUT SEQUENCE (HINDI in our case) while the KEY & VALUE vectors will be created based on the INPUT SEQUENCE (ENGLISH in our case)
* The rest of the procedure is same as Self-Attention.
![image](https://github.com/user-attachments/assets/002b67c0-d63f-4e14-b438-b34c105ae2ee)
![image](https://github.com/user-attachments/assets/044ec463-9a09-4da2-bdc0-6e1d09685ede)

![image](https://github.com/user-attachments/assets/7dcf3846-311f-4565-a6d0-e61850bd28d9)
* So the two arrows from the same line are the (KEY & VALUE) vectors, while that single arrow is (QUERY) vector

**Self-Attention Vs. Cross Attention (Output):**

![image](https://github.com/user-attachments/assets/0dfacf65-0581-4d35-b12c-d375f994f076)

**Example to understand Self-Attention:**

![image](https://github.com/user-attachments/assets/98018607-ce42-4128-83c4-a32d2b9ab8f8)

**Example to understand Cross Attention:**

![image](https://github.com/user-attachments/assets/1df46ac3-459e-4f0d-a7fc-972ebb278ac4)



# **Use Cases:**
* Cross-attention is specifically used where we have two different types of sequences.
* Used in Machine Translation tasks, Q&A Systems
* Multi Modal Data (image-text), (text-image), (text-speech) etc.






# **TWO MAJOR DIFFERENCES IN BAHDANAU VS LUONG ATTENTION:**



* **In case of Luong Attention, ``WE USE CURRENT DECODER'S HIDDEN STATE [s_i] RATHER THAN PREVIOUS HIDDEN STATE OF DECODER [s_i - 1]``. This way, we will have more updated information**

![image](https://github.com/user-attachments/assets/427cca11-5cdc-4862-b7da-4a43a22d076f)

* **Rather than using ANN ``ALIGNMENT MODEL`` TO CALCULATE ALIGNMENT SCORES ``WHICH CASUES UN-NECESSARY COMPUTATION, WE CAN USE DOT PRODUCT`` IF 2 VECTORS ARE SIMILAR, THE DOT PRODUCT WILL BE HIGHER; OTHERWISE, IT WILL BE LOWER**

![image](https://github.com/user-attachments/assets/c2ea214c-d6ef-4b59-8a86-60e2d182f771)

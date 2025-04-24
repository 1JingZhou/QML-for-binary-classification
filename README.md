# QML-for-binary-classification
Implement quantum machine learning (QML) using Pennylane on the Iris and MNIST datasets.

## Iris
For the Iris dataset, only the first 100 samples (i.e., the first two categories) are used. The classification task is implemented using 2 qubits and 4 layers, with each layer consisting of a data encoding component and a parameterized component. Both components have three rotational gates R_X, R_Y, R_Z. To match the number of parameters (n_param = 2 * 4 * 3 = 24), the features (dim = 4) are repeated 6 times.

Loss

![Iris-loss](https://github.com/user-attachments/assets/e8ca23f7-d135-49aa-a4cb-581fa547b18c)

Accuracy

![Iris-acc](https://github.com/user-attachments/assets/d147d73d-89d5-4434-9252-7a4a7ddcf9f1)


## MNIST
For the MNIST dataset, samples with labels "1" and "9" are chosen. This task is implemented using 9 qubits and 10 num_layers. The data encoding component and parameterized component are the same as that in Iris. To match the number of parameters (n_param = 9 * 10 * 3 = 270), the features (resize the figures to (1, 16, 16)) are padded and reshaped to (10, 9, 3).

Loss

![Mnist-loss](https://github.com/user-attachments/assets/595765c5-9ef7-4fb0-8bb5-32c6a07ed1c2)

Accuracy

![Mnist-acc](https://github.com/user-attachments/assets/946e9e8e-83ff-4dc8-932d-6855bb5a0902)

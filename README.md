import matplotlib.pyplot as plt
from sklearn.datasets import fetch_openml
import numpy as np

# Here we are loading the MNIST Dataset
mnist = fetch_openml('mnist_784', version=1)
Xraw, Yraw = mnist['data'], mnist['target']

# Here we are conerting to integers as they are in string format
Yraw = Yraw.astype(np.int8)



fig, axs = plt.subplots(2, 5, figsize=(10, 5))
axs = axs.ravel()  # Flatten the axes array for easier indexing

# Here Iterate through digits 0 to 9 and plot one random example for each
for digit in range(10):
    # Find all indices where the current digit is present
    digit_where = np.where(Yraw == digit)[0]

    # Randomly select one index
    random_index = np.random.choice(digit_where)

    # Access data using .iloc[] to ensure consistent indexing between Xraw and Yraw
    image = Xraw.iloc[random_index].values.reshape(28, 28)

    # Plot the image
    axs[digit].imshow(image, cmap='gray')
    axs[digit].set_title(f"Digit: {digit}")
    axs[digit].axis('off')

plt.tight_layout()
plt.show()

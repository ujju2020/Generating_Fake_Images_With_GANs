# Generating_Fake_Images_With_GANs
The Jupyter notebook file "Generating_Fake_Images_With_GANs.ipynb" demonstrates the implementation and training of a Generative Adversarial Network (GAN) to generate fake images, using the MNIST dataset (handwritten digits).

### Summary of the content:

1. **Initial Setup and Libraries**:
   - Imports TensorFlow and Keras libraries, along with other necessary tools like `numpy`.
   - Loads and preprocesses the MNIST data, normalizing the pixel values to the range [-1, 1].

2. **Model Definitions**:
   - **Generator Network**:
     - A sequential model generates fake images from random noise, ending with a `tanh` activation to rescale output to match the preprocessed data range.
   - **Discriminator Network**:
     - A sequential model classifies images as real or fake, ending with a `sigmoid` activation.

3. **Compilation**:
   - The **Discriminator** is compiled with binary cross-entropy loss.
   - The **Generator** is combined with the Discriminator (fixed weights) to form the GAN model, which is compiled to optimize Generator performance.

4. **Training Logic**:
   - A custom function `train` runs the training loop:
     - Each epoch divides the training data into batches.
     - Trains the Discriminator on real and fake (generated from noise) samples.
     - Trains the Generator by optimizing it to fool the Discriminator.
   - Outputs the loss values for both networks for monitoring progression.

5. **Execution**:
   - Calls the `train` function for 50 epochs with a batch size of 128 to train the GAN.

6. **Generated Logs**:
   - Includes detailed logs showing the loss values of the Generator and Discriminator over batches and epochs.

You can view the notebook to explore the exact code for GAN architecture and training [here](https://github.com/ujju2020/Generating_Fake_Images_With_GANs/blob/main/Generating_Fake_Images_With_GANs.ipynb).

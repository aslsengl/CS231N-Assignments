# CS231N - Deep Learning for Computer Vision

I am self-studying Stanford's CS231N course through the publicly available lecture videos on YouTube. As part of my learning journey, I decided to implement all the assignments from scratch using only NumPy — without copying the official solutions.

The goal is not just to complete the assignments, but to deeply understand every line of code: why each formula works, what each matrix operation does, and how the pieces fit together.

## Progress

### ✅ Assignment 1 - Image Classification Pipeline

#### Q1: k-Nearest Neighbor (kNN)
- Computed L2 distances using two loops, one loop, and fully vectorized (no loops)
- Vectorized version is **67x faster** than the naive double loop
- Used 5-fold cross-validation to find the best value of k
- Achieved ~27% accuracy on CIFAR-10

#### Q2: Softmax Classifier
- Implemented Softmax loss and gradient from scratch
- Understood why we use -log(probability) as loss
- Trained weight matrix W using Gradient Descent
- Achieved ~35% accuracy on CIFAR-10

#### Q3: Two-Layer Neural Network
- Implemented full forward and backward pass manually
- Added ReLU activation to learn non-linear decision boundaries
- Understood backpropagation step by step
- Achieved ~50% accuracy on CIFAR-10

#### Q4: Image Features
- Implemented HOG (Histogram of Oriented Gradients) to capture edges and shapes
- Implemented Color Histogram to capture color distribution
- Showed that hand-crafted features outperform raw pixels
- Achieved ~38% accuracy even with simple kNN classifier

#### Q5: Fully Connected Network
- Redesigned the network with a modular layer structure
- Each layer has its own forward and backward functions
- Easy to stack any number of layers
- Deeper networks capture more complex patterns

### ✅ Assignment 2 - Deep Learning Techniques

#### Q1: Batch Normalization
- Implemented forward and backward pass from scratch
- Showed vanishing gradient problem with deep networks
- Batch Norm keeps std=1.0 across all layers
- Faster training: loss dropped to 0.61 vs 0.97 without BN

#### Q2: Dropout
- Implemented Inverted Dropout (forward + backward)
- Demonstrated overfitting problem visually
- Dropout reduces gap between train and validation loss
- p=0.5 → %50 of neurons randomly disabled during training

#### Q3: Convolutional Neural Networks (CNN)
- Implemented Conv layer and MaxPool from scratch
- Showed CNN uses 113x fewer parameters than FC layers
- Different filters detect different features (edges, colors, corners)
- Pipeline: Image → Conv → ReLU → Pool → FC → Score

#### Q4: Network Visualization
- Filter Visualization: what each CNN filter detects
- Saliency Maps: which pixels affect the decision (dLoss/dX)
- Class Visualization: Gradient Ascent to generate "ideal" images

#### Q5: RNN & Image Captioning
- Implemented RNN step: h_t = tanh(Wx@x + Wh@h_(t-1) + b)
- Built Image Captioning pipeline: CNN → RNN → caption
- Trained to generate "a cat sat <END>" correctly
- Learned Backpropagation Through Time (BPTT)

## Key Things I Learned
- How to think about images as vectors of numbers
- Why vectorization matters (speed and clarity)
- The intuition behind Gradient Descent and Backpropagation
- How loss functions measure how wrong a model is
- Why features like HOG work better than raw pixels
- How adding layers increases a network's expressive power
- How Batch Normalization stabilizes deep network training
- Why Dropout prevents overfitting
- How CNNs share parameters across spatial locations
- How to visualize what a neural network has learned
- How RNNs handle sequential data with hidden states

## Tech Stack
- Python
- NumPy
- Matplotlib

## Course
- 🎥 Lectures: [CS231N YouTube](https://www.youtube.com/playlist?list=PL3FW7Lu3i5JvHM8ljYj-zLfQRF3EO8sYv)
- 📚 Course website: [cs231n.github.io](https://cs231n.github.io)

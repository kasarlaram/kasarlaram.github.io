# Machine Learning Model – Teachable Machine

## a. How Teachable Machine Uses Machine Learning

Teachable Machine is a simple interface built on top of a **pre-built neural network** (typically a convolutional neural network for images, and similar architectures for audio or pose data).

It works as follows:

- You choose a **machine-learning task** such as image, sound, or pose classification.
- You create multiple **classes (labels)**, for example *Cat* and *Dog*.
- For each class, you provide **training examples** using a webcam, uploaded images, sounds, or poses.
- Behind the scenes, Teachable Machine **fine-tunes a pre-trained model** using your data.
- The model learns patterns such as shapes, colors, textures, frequencies, or joint positions that are associated with each label.
- When you click **Train**, the system runs an **optimization algorithm** (such as gradient descent) to adjust the model’s internal weights so predictions match the labeled data.
- After training, when new input is provided, the model outputs **probabilities** for each class and selects the most likely one.

In this way, Teachable Machine can solve **arbitrary classification problems** by learning an automatic mapping from **input → predicted class** using labeled examples.

---

## b. Application Created Using Teachable Machine

The application created using Teachable Machine is an **image-classification app called “Pet Pals.”**

The app classifies images captured from a webcam or uploaded by the user as either:

- **Cat**
- **Dog**

---

## c. Problem the Application Is Intended to Solve

This application demonstrates how a **machine-learning image classifier** can distinguish between **two visually similar categories** without relying on manually coded rules.

Practically, it serves as a **learning and demonstration tool**, showing how adjusting the training data affects model accuracy and performance in real time.

---

## d. Why This Application Was Chosen

This application was chosen for several reasons:

- **Intuitive** – The difference between cats and dogs is easy for users to understand.
- **Easy data collection** – Images can be quickly collected using a webcam or existing photos.
- **Educational value** – It clearly demonstrates key machine-learning concepts such as training data quality, overfitting, and generalization.
- **Engaging** – Users can experiment with different images, backgrounds, or pets and immediately see how the model responds.

---

## e. URL to the Application or Exported Model

After training and exporting the model using **Export Model → Upload my model**, Teachable Machine generates a public URL similar to the one below:

https://teachablemachine.withgoogle.com/train/image

*(Replace this link with your actual exported model or application URL.)*

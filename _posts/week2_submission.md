# Week 2 Submission

## 1. Data Splitting – "Homework vs. Final Exam"

Imagine you’re teaching a kid to do math.

You give them **homework problems** to practice on.

Later, you give them a **test** to see if they really understand it.

In machine learning, we do the same thing with data:

- **Training set = homework**  
  This part of the data is what the computer *learns* from. It sees the examples and adjusts itself to do better and better.

- **Test set = final exam**  
  This part of the data is kept hidden until the end. We use it once the learning is done to check:
  > "Can this model handle new, never-seen examples?"

If we didn’t split the data and just tested on the same examples it learned from, it’d be like letting a student bring the answer key to the exam — it would look smart, but we wouldn’t know if it actually learned anything useful.

---

## 2. Model Evaluation – "Did it do a good job?"

Once the model has learned, we need to ask:

> **"How good is it, really?"**

This is like grading that final exam. We compare:

- What the model **predicted**
- What **actually happened** in real life

Then we use simple scores (called **metrics**) to describe how well it did.

### Examples of Metrics

**For predicting numbers (e.g., house prices):**
- On average, how far off were we?

**For yes/no predictions (e.g., "Will this customer cancel?")**
- **Accuracy** – How often were we right overall?
- **Precision** – When we said "yes," how often was it truly yes?
- **Recall (Sensitivity)** – Out of all the real "yes" cases, how many did we catch?

Model evaluation is the step where we **grade the model** and decide whether it is good enough to trust in the real world or needs improvement.

---

## 3. Real-World Application: Insurance Pricing with Machine Learning

One concrete application from the Nationwide materials is **using machine learning to price insurance more accurately**, especially **auto insurance rates**.

### a. How Machine Learning Improves or Replaces Existing Solutions

Traditionally, insurers use **generalized linear models (GLMs)** and other classical statistical methods to set prices. These approaches:

- Struggle with **complex, non-linear relationships**
- Handle only limited interaction effects at a time

Machine learning models (such as **random forests** and **gradient boosting**) can:

- Capture complex, multi-way interactions
- Use far more data and variables simultaneously
- Produce **more accurate risk predictions**, leading to better pricing

In an internal white paper example, applying machine learning to **5.4 million rows** of auto injury claim data improved pricing accuracy by approximately **32.86%**, measured using the **Gini coefficient**, a standard predictive power metric.

Machine learning does not merely replace traditional methods; it **extends them** by handling more complexity and improving predictive performance.

---

### b. Development vs. Active Use

This application is **actively used** in the insurance industry and at Nationwide:

- A full **proof-of-concept** was developed using real insurance data
- Multiple state insurance departments (OH, IA, TN, IL, WI, OR, MI) were engaged to support regulatory filings
- Nationwide’s **Machine Learning Reference Architecture** and tooling (such as Model Factory) support the full model lifecycle, from design to **deployment and production use**

This shows that machine learning-based insurance pricing is already operational and continuing to expand.

---

## 4. Ethical Considerations: Fairness and Discrimination

One major ethical concern is **fairness and discrimination**.

Machine learning models learn patterns from **historical data**. If this data contains past biases, models may:

- Learn biased patterns
- Hide them within complex mathematical structures
- **Reproduce or amplify** unfair outcomes in current pricing

Even if protected attributes like race are not directly included, models may rely on **proxy variables** such as:

- Location
- Vehicle type
- Job category

These proxies can correlate strongly with protected characteristics, potentially leading to:

- Certain groups paying more than their true risk justifies
- Reduced access to essential products like auto insurance

Because insurance pricing directly affects people’s livelihoods and mobility, fairness concerns are a **serious ethical issue**, not merely a technical challenge.

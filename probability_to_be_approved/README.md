
# Probability of Passing Multiple-Choice Exams by Luck

This notebook aims to analyze the **probability of passing multiple-choice exams purely by guessing**, using the **binomial distribution**.

## 📌 Objective

Calculate the probability of a candidate passing under different test scenarios, varying:

- The number of answer choices per question (2 to 5).
- The minimum number of correct answers required to pass (5 or 6).
- Total number of questions (fixed at 10).

## 📊 Methodology

We use the binomial distribution to calculate:

- Probability of getting exactly *k* correct answers.
- Probability of getting *k* or more correct answers (i.e., passing).

## 📚 Evaluated Scenarios

1. **3 choices per question**, minimum of 5 correct answers to pass.
2. **4 choices per question**, minimum of 5 correct answers to pass.
3. **5 choices per question**, minimum of 5 correct answers to pass.
4. **Increased cutoff score to 6 correct answers** (with 3, 4, and 5 choices).
5. **True/False exam** (2 choices), with passing scores of 5 or 6.

## 📈 Results

- The **chance of passing drops drastically** as the number of choices or the passing score increases.
- Exams with more choices are **much harder to pass by guessing**.
- Increasing the cutoff score also **significantly reduces the probability of passing by luck**.

## 🧮 Tools Used

- `pandas` for data manipulation and display.
- `scipy.stats.binom` for binomial probability calculations.

## ✅ Conclusion

Well-designed exams — with more answer choices and stricter passing criteria — **minimize the probability of passing by chance**, encouraging real preparation from candidates.

## 📎 Connect with Me

If you found this project useful or want to collaborate, feel free to reach out via [LinkedIn](https://www.linkedin.com/in/nathanferig/).

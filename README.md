# NLP-HW-2
# Sai Kumar Reddy Uppula - 700773349
# question 5 and programming question 

# Bigram Language Model (MLE)

This project implements a **Bigram Language Model** using **Maximum Likelihood Estimation (MLE)**.  
It builds **unigram** and **bigram** counts from a small training corpus, computes **bigram probabilities**, and calculates the **probability of a sentence** under the bigram model.

---

## What the Code Does

Given a training corpus of sentences (with `<s>` and `</s>` tokens), the program:

1. **Reads the training corpus** (hardcoded in `main()`).
2. **Tokenizes** each sentence by whitespace.
3. Computes:
   - **Unigram counts**: `C(w)`
   - **Bigram counts**: `C(w_{i-1}, w_i)`
4. Estimates bigram probabilities with MLE:

\[
P(w_i \mid w_{i-1}) = \frac{C(w_{i-1}, w_i)}{C(w_{i-1})}
\]

5. Implements a function to compute **sentence probability** as a product of bigram probabilities:

\[
P(\text{sentence}) = \prod_{i=2}^{n} P(w_i \mid w_{i-1})
\]

6. Tests the model on the two sentences:
   - `<s> I love NLP </s>`
   - `<s> I love deep learning </s>`
7. Prints:
   - unigram and bigram counts
   - each bigram probability used in scoring
   - total sentence probability
   - which sentence is preferred and why

---

## Files

- `bigram_lm.py` (or whatever you name your Python file): contains the full implementation.

---

## Requirements

- Python 3.8+ (recommended)
- No extra libraries needed (only uses Python standard library)

---

## How to Run

1. Save the code in a file, for example:
   - `bigram_lm.py`

2. Run:

```bash
python bigram_lm.py

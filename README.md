# Analyzing the Impact of Length Normalization on BM25 and Cosine Similarity

## Overview

This project evaluates the effects of incorporating length normalization on document ranking for BM25 and Cosine Similarity methods. Using three distinct queries, the study compares the precision and ranking changes caused by length normalization, providing insights into the effectiveness of these methods in text retrieval and similarity evaluation.

---

## Queries

1. **Economic Growth Policy**
2. **National Security Defense**
3. **God Bless America**

---

## Results Summary

### BM25 Method

#### Without Length Normalization
- **Economic Growth Policy:** Hoover, Taft, Truman, Bush, Harding
- **National Security Defense:** Truman, Reagan, Adams, Harrison, Roosevelt
- **God Bless America:** Trump, Reagan, Bush, Obama (2013), Obama (2009)

#### With Length Normalization
- **Economic Growth Policy:** Bush, Truman, Eisenhower, Reagan, Hoover
  - Similarity increased from 2.3 to 3.1 for the first document.
- **National Security Defense:** Roosevelt, Bush, Obama, Eisenhower, Truman
  - Similarity decreased from 3.26 to 2.3 for the first document.
- **God Bless America:** Roosevelt, Trump, Clinton, Bush, Obama (2013)
  - Similarity increased from 3.23 to 3.59 for the first document.

#### Precision
- **Economic Growth Policy:** Decreased from 0.66 to 0.33.
- **National Security Defense:** Consistent at 1.0.
- **God Bless America:** Consistent at 1.0.

---

### Cosine Similarity Method

#### Without Length Normalization
- **Economic Growth Policy:** Hoover, Truman, Taft, Reagan, Harding
- **National Security Defense:** Truman, Reagan, Adams, Monroe, Pierce
- **God Bless America:** Trump, Clinton, Nixon, Biden, Bush

#### With Length Normalization
- Rankings remained unchanged, but precision improved.

#### Precision
- **Economic Growth Policy:** Improved from 0.66 to 1.0.
- **National Security Defense:** Consistent at 1.0.
- **God Bless America:** Consistent at 0.6.

---

## Observations

1. **BM25 with Length Normalization:**
   - Precision for "Economic Growth Policy" declined, indicating over-normalization for shorter documents.
   - Precision for "National Security Defense" and "God Bless America" remained consistent, highlighting stability for certain query types.

2. **Cosine Similarity with Length Normalization:**
   - Precision for "Economic Growth Policy" improved significantly, achieving perfect relevance (1.0).
   - Rankings for all queries were unaffected, demonstrating robustness in similarity scoring.

---

## Conclusion

- **BM25**: Length normalization can improve similarity scores but may negatively affect precision for some queries due to its bias toward longer documents.
- **Cosine Similarity**: More consistent and efficient in improving precision, especially for queries requiring exact matches.
- **Recommendation**: Cosine Similarity with length normalization is the preferred method for tasks emphasizing text-query similarity, whereas BM25 remains a strong option for search engine-style text retrieval.

---

## Code and Results

Detailed implementations and results are available in the accompanying notebook `VectorSpace.ipynb`.

---

## Questions?

Feel free to reach out for further information or collaboration opportunities.

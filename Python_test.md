**Problem: Word Frequency Analysis**

You are given a list of sentences as strings, and your task is to perform a word frequency analysis. You need to create a function `word_frequency(sentences)` that takes a list of sentences as input and returns a dictionary where each key is a unique word in the sentences, and the corresponding value is a list of sentence indices where that word appears.

The sentences are provided as a list of strings, and they may contain punctuation and capitalization. You should consider words as case-insensitive, meaning "Word" and "word" should be treated as the same word. Additionally, you should ignore common English stop words (e.g., "the," "and," "is," "in," etc.).

Your function should:

1. Tokenize each sentence into words, ignoring punctuation.
2. Convert all words to lowercase.
3. Exclude common stop words.
4. Create a dictionary where each unique word is a key and the corresponding value is a list of sentence indices (0-based) where that word appears.

For example, given the following input:

```python
sentences = [
    "The quick brown fox jumps over the lazy dog.",
    "A quick brown dog jumps over a lazy cat.",
    "The dog and the cat are friends.",
    "The fox and the dog are not friends."
]
```

Your function should return the following output:

```python
{
    'quick': [0, 1],
    'brown': [0, 1],
    'fox': [0, 3],
    'jumps': [0, 1],
    'lazy': [0, 1],
    'dog': [0, 1, 2, 3],
    'cat': [1, 2],
    'friends': [2],
    'not': [3]
}
```
In the output, 'quick' appears in sentences 0 and 1, 'brown' appears in sentences 0 and 1, 'fox' appears in sentences 0 and 3, and so on.

Your solution should be efficient and handle large input lists of sentences.

**Note:**
- You can use the `re` module in Python to help with text preprocessing and tokenization.
- You can find a list of common English stop words online for exclusion.
- You may assume that sentences are separated by periods ('.') and have no other punctuation apart from spaces and periods.

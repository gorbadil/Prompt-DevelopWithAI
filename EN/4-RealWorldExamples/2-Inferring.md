# Inferring

Making use of LLMs to infer information from text, i.e. text analysis, is another common use case. A common use case is sentiment analysis, such as grouping e-commerce reviews by sentiment. Beyond this, LLMs have diverse real-world applications, including customer service automation, market research, fraud detection, compliance monitoring, speech-to-text transcription, and anomaly detection. These applications demonstrate the versatility of LLMs in extracting valuable insights from text data, automating processes, and enhancing decision-making across different sectors. By leveraging LLMs, businesses can improve operational efficiency, gain deeper customer insights, and tackle complex challenges in areas such as cybersecurity and regulatory compliance

## Example

Imagine you are running a famous e-commerce store with thousands of reviews. You want to group the reviews by the sentiment of the review. You can use LLMs to infer the sentiment of the review.

Here are some prompts showing the use of inferrence:

```
What is the sentiment of this text which is delimited with tripple backticks. Your output must be a single word.

"""Horrible product. They charged me twice the price and it broke after a week. I will never buy from them again."""
```

The output from this prompt is negative.

Another example:

```
Identify a list of emotions that the writer of the following review is expressing. Include no more than 5 items in the list. Format your answers as a list of lower-case words separated by commas.

"""I am so happy with this product. It is the best thing I have ever bought. I will definitely buy from them again."""
```

Output: happy, satisfied, pleased, content, enthusiastic

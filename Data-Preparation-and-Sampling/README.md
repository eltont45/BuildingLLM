# Module 1
## Data Preparation and Sampling
### Tokenization
In this notebook, we start with using [The Verdict](https://www.eastoftheweb.com/short-stories/UBooks/Verd.shtml)
short story by Edith Wharton. We start by tokenizing the text. Tokenization in the LLM context is the process of
breaking down text into smaller units called "tokens" to it easier to analyze and process. There are three main
ways of tokenization which are: whole word tokens (whole words are used as tokens), subword tokens (words are
broken down into subwords), and character tokens (words are broken down into characters). Typically we use a
subword tokener because subwords retain the similarity between words. The tokens are then given token IDs. We have
special context tokens like <|endoftext|> which make it easier for the LLM to recognize when a new text from a different
source is beginning.
### Byte Pair Encoding
Byte pair encoding (BPE) is a subword tokenization algorithm used to train LLMs such as GPT-2 and GPT-3. BPE works by
repeatedly merging most frequent pair of bytes (aka subword units) in a corpus to create new, longer tokens. This leads to
reduced vocabulary that efficiently represent a text source. Using the BPE algorithm also solves the problem of facing
unfamiliar words during tokenization unlike whole word tokenization which will run into errors when faced with an unknown
word.
 

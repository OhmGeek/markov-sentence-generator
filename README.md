# Markov Sentence Generator
This is the Markov Sentence Generator forked from @hrs. It is now written in an Object Oriented manner, which is useful when deploying with Flask/using other apps.

NOTE: The code itself was modified in the middle of a hackathon, and as such the quality of the code itself isn't that great. This is something I plan to improve on.

## What it does?
This program generates a sentence's worth of "real-looking" text using a Markov model and sample textual training input.  Given some sample text from which to build a model, the program prints out a sentence based on a Markov chain.

## How to use it?
First, create an object:

```
gen = SentenceGenerator()
```

Then you can train it by giving it the list of words specified from a filename:
Warning: horrible code incoming.

```
gen.buildMapping(gen.wordlist(filename),markovLength)
```
The Markov Length defaults to 1 which is the fastest, although increasing this value may generate more realistic text. Markov length of 6 or more is probably pointless though, as you will probably end up getting out complete sentences anyway.

You can then generate a sentence based on a Markov length and an input word:
Warning: slightly redundant parameter incoming

```
gen.genSentence(markovLength,inputWord)
```

##  Sample text

The texts of *Portrait of the Artist as a Young Man* and *Leaves of Grass* (in `snippet.txt`) are taken from Project Gutenberg.  The usual copyright headers had to be removed so that they could serve as useful sample input, but naturally all the rights and restrictions of a Gutenberg book still apply.

## Uses of this:

As part of the Local Hack Day 2016 (Durham), this was used to generate words from a person's tweets.

## Acknowledgements

Thanks to @hrs for creating this original code.

# The unwritten ezāfe

*Work in progress. What ships is the rule classifiers in `ghazal_nlp/ezafe.py`.*

About a quarter of unmarked silent-ه junctions carry an ezāfe nobody wrote, so
unmarked text can't serve as "no ezāfe" examples.

## Learning from the marks

Marked junctions are positives, unmarked ones unlabelled (Elkan and Noto). A
positive-unlabelled model of P(marked | context) per source, over 2.1M
junctions from Wikipedia, Wikisource, books and Ganjoor, with nested context
cells (next word's class, the word after, punctuation, then the words).

On the 175 development sites: the rules 84.0%, the learned model 76.0% to
84.0% depending on the prior. When it says ezāfe it's right 97% of the time,
but it finds only 63% of them.

## Asking the metre

In verse, if every reading of a line in its metre agrees on a junction, that's
a free label. On 40 Ganjoor sites the metre decided 12 (16 with the weight
lexicon), and 9 of 12 (13 of 16) matched my labels. Every miss was a missed
ezāfe: an ezāfe and a hiatus glide often sound the same.

## Next

- A noun and adjective lexicon, so `junction` stops treating every unknown
  word as a noun.
- The metre's answers as a review queue, not as training labels.
- The model's counts rebuilt on a public corpus.

# Translationese

*Work in progress.*

Does translated Persian leave a surface trace that native Persian doesn't?

## So far

Three matched comparisons of translations against native modern prose (one
with Hedayat's Kafka beside Hedayat's own prose), and two controls a detector
must not pass: native newspaper prose and classical prose, each against native
modern prose. Every text clipped to 220 tokens. AUC:

| | fixed native profile | register-conditioned | function-word rate |
|---|---:|---:|---:|
| translation corpus vs native | 0.391 | 0.534 | 0.908 |
| modern translation vs native | 0.522 | 0.567 | 0.680 |
| all translation vs native | 0.591 | 0.589 | 0.661 |
| control: newspaper vs native | 0.544 | 0.450 | 0.309 |
| control: classical vs native | 0.735 | 0.454 | 0.519 |

Nothing beats its controls. Translations do use more function words in every
matched arm, but two native registers of the same decade separate about as
well.

## Next

- Machine translation, which may leave a different trace.
- Whether the feeling that a text "reads translated" is measurable, rather than
  where the text came from.

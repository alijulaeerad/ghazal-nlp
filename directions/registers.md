# Registers from function words

*Work in progress.*

Function words say how a text is put together, whatever it's about. A
parliamentary transcript, a ghazal, a legal code and an encyclopedia entry use
کز، بدو، مزبور، لذا at very different rates. The idea: one closed-class
profile per register, a document goes to the nearest one, and it gets a score
for how typical it is there.

## So far

2,125 held-out documents, ten register labels, closed-class rates only:
accuracy 0.636, macro-F1 0.548.

| register | F1 |
|---|---:|
| religious | 0.913 |
| legal | 0.882 |
| reference | 0.804 |
| parliamentary | 0.761 |
| verse | 0.717 |
| literary-classical | 0.580 |
| translated | 0.330 |
| literary-modern | 0.249 |
| newspaper | 0.246 |
| literary-qajar | 0.000 |

- Institutional registers are easy; literary ones aren't. Modern fiction and
  newspaper prose look the same, and so do Qajar prose and Qajar translation.
- Authors cross registers: pulling modern scholarship (فروغی، کسروی) out of
  "literary" took modern fiction from 0.249 to 0.690.
- What each register over-uses is readable: parliamentary قبل ×5.4 («قبل از
  دستور»), verse تو ×3.5 and ای ×3.2, legal یا ×3.1.
- The labels come from titles, collections and authors, so part of the score
  is recognising collections.

## Next

- Labels rebuilt on a current corpus, with their rules published.
- The profiles (fit, attribute, atypicality) as a stdlib tool.
- Atypicality as a quality signal: "unusual for its own register".

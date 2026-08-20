---
name: genomics-theory-mining
description: >
  Dig up a classic genomics or population-genetic theory and test it
  against modern data. Use when the user wants old-theory mining,
  forgotten models, Muller ratchet, gene balance, nearly-neutral,
  hitchhiking, Hill-Robertson, Ohno WGD, or a revival paper that
  is not a methods benchmark.
---

# genomics-theory-mining

The paper is the old math plus a new test, not a review with extra adjectives.
Find the original, list the assumptions, then say which modern data can break them.

## When to use

- A user names a "forgotten" or "classic" theory and asks if it still holds.
- A grapevine / clonal / polyploid fact looks like an old model with the wrong organism.
- Someone wants a revival paper, not another tool comparison.

Do not use this for a methods bake-off, a database build, or a literature dump.

## Order

1. **Name the theory in one sentence** (what it predicts, not who is famous).
2. **Read the original paper**, not the 2010s review that cites it. Quote the claim and the year.
3. **Write the assumption list.** Sexual panmixia? Infinite sites? Diploid? Stable Ne? No structure? No clones?
4. **Mark which assumptions fail in the study system** (Vitis: clones, vegetative propagation, high TE, mixed ploidy, capture / aDNA missingness).
5. **Pick the modern test.** One dataset, one statistic, one falsifier. If you cannot name the falsifier, you do not have a paper.
6. **Cite the original math.** Do not rename the theory. Do not invent a "generalized X".

## Theories worth mining (starter list)

| Theory | Original (start here) | What usually dies in plants / clones |
|--------|-----------------------|--------------------------------------|
| Muller's ratchet | Muller 1964; Felsenstein 1974 | Sexual recombination assumed; clones and somatic lineages change the clock |
| Nearly-neutral | Ohta 1973, 1992 | Ne is not one number in a cultivar collection |
| Hitchhiking / sweeps | Maynard Smith and Haigh 1974 | Clonal background and relatedness fake a sweep |
| Hill-Robertson | Hill and Robertson 1966 | Interference needs a real recombination map, not a chip skeleton |
| Gene balance / dosage | Ohno 1970; Birchler and Veitia 2007 | WGD and tandem NLRs are not the same "dosage" |
| Cost of males / Kondrashov | Kondrashov 1988 | Does not map onto grafted clones |
| Infinite-sites / Watterson | Kimura 1969; Watterson 1975 | Recurrent TE and gene conversion violate it |
| Neutral theory baseline | Kimura 1968 | Still the null; not a conclusion |

This list is a door, not a canon. If the original is not on the desk, stop.

## Plant / Vitis checks

- Filter clones before any "population" statistic that assumes unrelated sexuals.
- Do not treat a cultivar panel as Ne.
- Somatic mutation and germline mutation are different clocks. Say which one you measured.
- Plastid / TE / graph coordinates are not interchangeable with a 12X SNP panel.
- aDNA samples project onto a modern panel; they do not redefine the theory.

## Note shape (write this, then the draft)

```
Theory:
Original paper (year):
One-sentence prediction:
Assumptions:
Which fail here:
Modern data / statistic:
What would falsify it:
What we will not claim:
```

## Red lines

- Do not cite a review as the source of the theory.
- Do not apply a sexual-diploid model to clones and call it a test.
- Do not invent citations, years, or the original equation.
- Do not turn this into a 50-theory catalog. One theory per job.
- No unpublished genotypes or private site coordinates in the public note.

Related: `plant-lit-review`, `vitis-popgen`, `grapevine-adna`, `vitis-pangenome`.

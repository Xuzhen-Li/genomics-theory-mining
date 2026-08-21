# Tajima-Nei distance

```
Theory: Tajima-Nei 1984 nucleotide distance (unequal
  substitution rates)
Original paper (year): Tajima F, Nei M. 1984. Estimation
  of evolutionary distance between nucleotide sequences.
  Mol Biol Evol 1(3):269-285 (1 April 1984).
  DOI 10.1093/oxfordjournals.molbev.a040317 PMID 6599968.
  EuropePMC HTML opened
  (https://europepmc.org/article/MED/6599968): Tajima F,
  Nei M, Center for Demographic and Population Genetics,
  University of Texas, Houston 77225; 01 Apr 1984;
  Molecular Biology and Evolution 1(3):269-285; DOI;
  PMID; abstract. A formula for the average number of
  nucleotide substitutions per site (delta) between two
  homologous DNA sequences that allows unequal rates of
  substitution among different nucleotide pairs (equal-
  input model). Simulations: a reasonably good estimate
  for a wide range of substitution patterns as long as
  delta is equal to or smaller than 1. Inapplicable cases
  are rarer than for other then-recent methods (insulin
  genes). A companion method estimates nucleotide changes
  due to deletion and insertion; globin genes: the number
  of changes per site increases with evolutionary time
  but the pattern is quite irregular. Distinct from
  filled Tajima 1989 (Tajima D as pi versus theta_W; not
  a pairwise distance). Distinct from filled Kimura 1980
  (this wave; transition / transversion K80, not unequal-
  rate delta). Distinct from filled Nei 1972 / 1978
  (allele-frequency distance, not nucleotide delta).
  Distinct from filled Zuckerkandl and Pauling 1962 /
  1965. Jukes and Cantor 1969 was not opened.
One-sentence prediction: Pairwise nucleotide distance is
  Tajima-Nei delta when substitution rates among
  nucleotide pairs are unequal and delta is at most 1.
Assumptions: homologous DNA sequences, not chip
  genotypes; clone IBS is not a homologous pair; dual
  domestication is not one delta; somatic clone age is
  not evolutionary time.
Which fail here: grafted clones are not diverged
  homologous sequences. A cultivar panel is not two
  species. Clone IBS fakes delta. Dual domestication is
  two origins.
Modern data / statistic: whether wild / cultivar sequence
  pairs after clone + IBD filters give a Tajima-Nei
  delta (unequal-rate; delta <= 1) versus clone copies
  or two origins.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris after
  clone + IBD filters. Vondras 2019 / Roach 2018 as
  clone-clock companions. Use as the Tajima-Nei-distance
  contrast, not as a published grape delta analysis. Do
  not invent a grape Tajima-Nei-distance paper.
What would falsify it: pairwise delta is not a Tajima-
  Nei substitution clock after clone filter (clone
  copies, or two origins). Tajima D remains the 1989
  job. K80 remains Kimura 1980. Allele-frequency D
  remains Nei 1972 / 1978.
What we will not claim: that Tajima 1989 is this paper
  (already filled). That Kimura 1980 is this paper. That
  Jukes and Cantor 1969 is the source. That Dong 2023
  fitted Tajima-Nei delta. That clone age is
  evolutionary time.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification

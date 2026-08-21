# Kimura two-parameter distance

```
Theory: Kimura 1980 two-parameter nucleotide distance
  (K80 / K2P)
Original paper (year): Kimura M. 1980. A simple method
  for estimating evolutionary rates of base substitutions
  through comparative studies of nucleotide sequences.
  J Mol Evol 16(2):111-120 (1 December 1980 on EuropePMC;
  DOI issue date). DOI 10.1007/bf01731581 PMID 7463489.
  EuropePMC HTML opened
  (https://europepmc.org/article/MED/7463489): Kimura M;
  01 Dec 1980; Journal of Molecular Evolution
  16(2):111-120; DOI; PMID; abstract. Pairwise nucleotide
  differences are type I (transition: both purines or both
  pyrimidines) or type II (transversion: purine versus
  pyrimidine). With P and Q the fractions of sites of
  type I and type II, evolutionary distance per site is
  K = -(1/2) ln [(1-2P-Q) square root of 1-2Q]. Rate per
  year is k = K/(2T). Third-position synonymous component
  is K'S = -(1/2) ln (1-2P-Q). Globin examples: synonymous
  substitutions occur at much higher rates than amino-
  acid-altering substitutions. Distinct from filled
  Kimura 1968 (neutral substitution rate as a molecular
  null; not this transition / transversion distance).
  Distinct from filled Kimura 1955 (forward drift
  diffusion). Distinct from filled Kimura 1969 infinite-
  sites. Distinct from filled Zuckerkandl and Pauling
  1962 / 1965 (clock as linear divergence; not the K80
  formula). Distinct from filled Tajima and Nei 1984
  (this wave; unequal rates among nucleotide pairs).
  Jukes and Cantor 1969 was not opened as a lockable
  claim page (book chapter); not the source.
One-sentence prediction: Pairwise sequence distance is
  Kimura's K from transition fraction P and transversion
  fraction Q; synonymous K exceeds amino-acid-altering K.
Assumptions: homologous nucleotide sequences, not chip
  genotypes; T is germline divergence time, not clone
  age; a cultivar pair is not two species; dual
  domestication is not one T.
Which fail here: grafted clones skip the germline T in
  k = K/(2T). A cultivar collection is not two diverged
  sequences. Clone IBS fakes P and Q. Dual domestication
  is human choice, not a K80 clock.
Modern data / statistic: whether wild / cultivar sequence
  pairs after clone + IBD filters give a Kimura-1980 K
  (transitions versus transversions; synonymous faster
  than replacement) versus clone copies or two origins.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris after
  clone + IBD filters. Vondras 2019 / Roach 2018 as
  clone-clock companions (somatic age is not T). Use as
  the K80 contrast, not as a published grape K80
  analysis. Do not invent a grape K80 paper.
What would falsify it: pairwise K is not a Kimura-1980
  clock after clone filter (clone copies, or two origins).
  Neutral substitution rate remains Kimura 1968. The
  linear clock remains Zuckerkandl-Pauling. Unequal-rate
  distance remains Tajima-Nei 1984.
What we will not claim: that Kimura 1968 is this paper
  (already filled). That Kimura 1955 is this paper. That
  Jukes and Cantor 1969 is the source (chapter not
  opened). That Dong 2023 fitted K80. That clone age is
  T.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification

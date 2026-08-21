# Kimura stochastic drift

```
Theory: Kimura 1955 stochastic random genetic drift
  (complete diffusion solution)
Original paper (year): Kimura M. 1955. Solution of a
  process of random genetic drift with a continuous
  model. Proc Natl Acad Sci USA 41(3):144-150
  (15 March 1955). DOI 10.1073/pnas.41.3.144
  PMID 16589632 PMCID PMC528040. EuropePMC HTML opened
  (https://europepmc.org/article/MED/16589632): Kimura M,
  Department of Genetics, University of Wisconsin;
  01 Mar 1955; PNAS 41(3):144-150; DOI; PMID; PMC; no
  abstract there. EuropePMC PDF opened
  (https://europepmc.org/articles/PMC528040?pdf=render):
  Motoo Kimura; communicated by Sewall Wright,
  15 November 1954; Contribution No. 84 of the National
  Institute of Genetics, Mishima-shi, Japan. Random
  genetic drift in finite populations from random sampling
  of gametes. Fisher and Wright had treated the state of
  steady decay; the complete time-dependent solution
  showing how the process leads to that state was missing.
  Under a continuous (diffusion) model, with selection,
  migration, and mutation absent and non-overlapping
  generations, the gene-frequency density of unfixed
  classes is expanded in Gegenbauer polynomials with
  exponential decay e^{-i(i+1)t/4N}. Heterozygosity
  decreases exactly at the rate 1/(2N) per generation:
  H_t = H_0 e^{-t/2N}. The distribution of unfixed classes
  becomes nearly flat after about 2N generations when the
  process starts at p = 0.5. Distinct from filled Kimura
  1968 (neutral substitution rate at the molecular level;
  not this time-dependent frequency distribution).
  Distinct from filled Kimura and Weiss 1964 stepping-
  stone (spatial correlation; not panmictic drift).
  Distinct from filled Kimura and Crow 1964 infinite-
  alleles. Distinct from filled Kimura 1969 infinite-
  sites. Distinct from filled Kingman 1982 coalescent
  (sample genealogy; not the 1955 forward diffusion).
  Distinct from filled Wright 1931 (island math; not the
  complete drift solution). Distinct from filled Ewens
  1972 sampling formula.
One-sentence prediction: In a finite panmictic population
  without selection, mutation, or migration, the gene-
  frequency distribution of unfixed classes follows
  Kimura's diffusion solution and heterozygosity decays
  as e^{-t/2N}.
Assumptions: a random-mating diploid population of
  effective size N; clones are not that population; a
  cultivar panel is not N; dual domestication is not one
  Wright-Fisher trajectory; somatic clone age is not t
  in generations of random mating.
Which fail here: grafted clones skip the random sampling
  of gametes that generates the 1955 process. A cultivar
  collection is not N. Clone IBD fakes heterozygosity.
  Dual domestication is human choice, not drift time.
Modern data / statistic: whether wild-sample heterozygosity
  / unfixed-class frequency after clone + IBD filters
  follows a Kimura-1955 drift trajectory (H_t = H_0
  e^{-t/2N}), versus clone copies or two domestication
  centres.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris after
  clone + IBD filters. Use as the drift contrast, not as
  a published Kimura-1955 analysis. Vondras 2019 / Roach
  2018 as clone-clock companions (somatic age is not
  Wright-Fisher t). Do not invent a grape drift-trajectory
  paper.
What would falsify it: heterozygosity is not a Kimura-1955
  drift trajectory after clone filter (clone copies, or
  two origins). Neutral substitution rate remains Kimura
  1968. Sample genealogies remain Kingman 1982. Spatial
  correlation remains Kimura-Weiss 1964.
What we will not claim: that Kimura 1968 is this paper
  (already filled). That Kimura and Weiss 1964 is this
  paper. That Kingman 1982 is this paper. That Wright
  1931 is this paper. That Dong 2023 fitted a 1955
  diffusion. That clone age is Wright-Fisher t.
```

---

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification

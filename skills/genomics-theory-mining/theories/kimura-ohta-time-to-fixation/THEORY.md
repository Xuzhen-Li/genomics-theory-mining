# Kimura-Ohta time to fixation

```
Theory: Kimura-Ohta mean time to fixation (4Ne
  generations for a rare neutral)
Original paper (year): Kimura M, Ohta T. 1969. The
  average number of generations until fixation of a
  mutant gene in a finite population. Genetics
  61(3):763-771 (March 1969; EuropePMC 01 Mar 1969).
  DOI 10.1093/genetics/61.3.763 PMID 17248440
  PMCID PMC1212239. EuropePMC HTML opened
  (https://europepmc.org/article/MED/17248440): Kimura M,
  Ohta T, National Institute of Genetics, Mishima, Japan;
  01 Mar 1969; Genetics 61(3):763-771; DOI; PMID; PMC;
  no abstract there. Seed-lock PDF
  (https://europepmc.org/articles/PMC1212239?pdf=render):
  Contribution No. 692; received 26 July 1968;
  Genetics 61:763-771 March 1969. Diffusion solution
  for the mean time to fixation excluding loss, and
  separately the mean time to loss excluding fixation.
  For a selectively neutral mutant, ti(p) = -4Ne
  (1-p)/p * ln(1-p); at the limit p -> 0, ti(0) = 4Ne.
  Summary: a single mutant gene, if selectively neutral,
  takes about 4Ne generations until fixation in a
  population of effective size Ne (cases of loss
  excluded). Monte Carlo checks for neutrality and
  genic selection. Distinct from filled Kimura 1968
  (neutral substitution rate equals mutation rate; not
  the 4Ne waiting time). Distinct from filled Kimura
  1955 (forward drift diffusion / heterozygosity decay).
  Distinct from filled Kimura 1969 infinite-sites.
  Distinct from filled Ohta 1972 / 1973 (nearly-neutral
  rate versus Ne; not time to fixation). Distinct from
  filled Kimura and Crow 1964 infinite-alleles. Kimura
  and Ohta 1971 Nature was opened on EuropePMC; no
  abstract / no claim text; not used.
One-sentence prediction: A rare neutral mutant takes
  about 4Ne generations to fixation if the loss cases
  are excluded.
Assumptions: a finite sexual Wright-Fisher population
  with a meaningful Ne; a cultivar panel is not that
  Ne; clone age is not the fixation clock; dual
  domestication is not one N; grafted cuttings skip
  the substitution process.
Which fail here: a cultivar collection is not Ne.
  Grafted clones skip the 4Ne walk. Dual domestication
  is two origins. Human choice is not the paper's
  fixation. Clone-private SNPs are not substitutions
  on their way to fixation.
Modern data / statistic: whether a rare neutral
  variant's sojourn / fixation time after clone + IBD
  filters is about 4Ne generations, versus clone age
  or two origins.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild versus cultivar
  Ne contrast after clone + IBD filters. Vondras 2019
  / Roach 2018 as clone-clock companions (somatic age
  is not 4Ne). Use as the 4Ne-time contrast, not as a
  published grape time-to-fixation analysis. Do not
  invent a grape 4Ne paper.
What would falsify it: fixation / sojourn time is not
  about 4Ne after clone filter (clone age, or two
  origins). Neutral substitution rate remains Kimura
  1968. Drift diffusion remains Kimura 1955. Nearly-
  neutral rate-versus-Ne remains Ohta 1972 / 1973.
What we will not claim: that Kimura 1968 is this paper
  (already filled). That Kimura 1955 is this paper.
  That Ohta 1972 / 1973 is this paper. That Kimura and
  Ohta 1971 is the source (no claim text). That Dong
  2023 estimated a 4Ne sojourn. That clone age is 4Ne
  generations.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification

# Fu-Li tests

```
Theory: Fu-Li tests (external versus internal mutations)
Original paper (year): Fu YX, Li WH. 1993. Statistical tests
  of neutrality of mutations. Genetics 133(3):693-709
  (1 March 1993). DOI 10.1093/genetics/133.3.693 PMID 8454210
  PMCID PMC1205353. EuropePMC HTML opened (Fu YX, Center for
  Demographic and Population Genetics, University of Texas,
  Houston; Li WH; 01 Mar 1993; Genetics 133(3):693-709; DOI;
  PMID; PMC; abstract). Mutations in a sample genealogy are
  external (on external branches) or internal (on internal
  branches). Under neutrality the expected number of external
  mutations equals theta = 4 Ne mu, independent of sample
  size; external counts deviate under selection while internal
  counts are less affected. Several tests of the all-mutations-
  neutral hypothesis follow from those properties and from
  two common theta estimates. Distinct from filled Tajima 1989
  (pi versus theta_W; no external/internal split). Distinct
  from filled Watterson 1975 (S as a theta estimator) and
  filled Kimura 1969 infinite-sites. Distinct from filled
  HKA 1987 and filled Fay and Wu 2000 H (this wave; derived
  high-frequency excess, not external-branch counts).
One-sentence prediction: Selection (or a non-neutral
  demography that mimics it) shows up first as a deviation
  of external mutations from theta; internal mutations stay
  closer to the neutral expectation.
Assumptions: a random sample of DNA sequences from one
  population; the genealogy is Kingman-like, not a clone
  pedigree; external mutations are not clone-private SNPs;
  chips are not forced-biallelic loci.
Which fail here: a cultivar panel is not a random sample.
  Clone IBD fakes external mutations. Cuttings skip the
  sexual genealogy. Dual domestication is not one population.
  SNP chips are biallelic.
Modern data / statistic: Fu-Li D / F (or an external-versus-
  internal analogue) on Dong-class WGS after clone + IBD
  filters, versus the neutral theta expectation. Tajima and
  Fay-Wu remain other jobs.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild versus cultivar /
  other Vitis after clone + IBD filters. Use as a Fu-Li-
  style test, not as a published grape Fu-Li paper. Do not
  invent a grape Fu-Li paper.
What would falsify it: external versus internal counts do
  not reject neutrality after clone + IBD filters, OR
  clone-private SNPs are treated as external mutations
  (they are not). One-sample Tajima D is the 1989 job;
  derived high-frequency excess is the Fay-Wu job.
What we will not claim: that Tajima 1989 is this paper
  (already filled). That Fay and Wu 2000 is this paper.
  That Watterson 1975 is this paper. That Dong 2023 ran
  Fu-Li tests. That a chimera layer is an external branch.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification

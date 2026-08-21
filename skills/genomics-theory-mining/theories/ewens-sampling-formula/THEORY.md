# Ewens sampling formula

```
Theory: Ewens sampling formula
Original paper (year): Ewens WJ. 1972. The sampling theory of
  selectively neutral alleles. Theoretical Population Biology
  3(1):87-112. DOI 10.1016/0040-5809(72)90035-4 PMID 4667078.
  EuropePMC HTML landing opened (author, title, year, venue,
  volume, issue, pages, DOI, PMID). ScienceDirect HTML timed
  out this wave; lock from the EuropePMC page. The paper
  begins a sampling theory of a sample of genes from a
  selectively neutral locus, including a test that the
  alleles are indeed selectively neutral. Karlin and McGregor
  1972 Theor Popul Biol 3:113-116 is the same-issue addendum
  (PMID 4667073), not the source.
  Distinct from filled Kimura and Crow 1964 infinite-alleles
  (each mutation is a new allele; IBS is IBD). 1972 is the
  sampling distribution of allele-count configurations under
  that model.
  Distinct from filled Kingman 1982 coalescent.
One-sentence prediction: Under selective neutrality and
  infinite-alleles mutation, the configuration of allele
  counts in a sample follows Ewens's sampling formula; the
  number of types is a sufficient statistic for theta.
Assumptions: a random sample of genes from one locus;
  selective neutrality; infinite-alleles mutation; samples
  are not clones or first-degree cuttings; chips are not
  forced-biallelic.
Which fail here: a cultivar panel is not a random haploid
  sample. Clone IBD fakes allele identity. SNP chips are
  biallelic. Pedigree repeats are not new alleles.
Modern data / statistic: allele-count configuration (or
  haplotype-count configuration) in wild V. sylvestris
  after clone + IBD filters, versus the Ewens null.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild sylvestris subset.
  Use as a configuration test after clone + IBD filters,
  not as a published Ewens analysis. Do not invent a grape
  Ewens-sampling paper.
What would falsify it: the configuration is not Ewens after
  clone + IBD filters, OR clone IBS is treated as the allele
  sample (it is not).
What we will not claim: that Kimura and Crow 1964 is this
  paper (different job). That Dong 2023 fitted Ewens's
  formula. That a cultivar PCA is a neutral sample.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification

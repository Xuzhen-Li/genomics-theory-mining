# GC-biased gene conversion

```
Theory: GC-biased gene conversion
Original paper (year): Galtier N, Piganeau G, Mouchiroud
  D, Duret L. 2001. GC-content evolution in mammalian
  genomes: the biased gene conversion hypothesis.
  Genetics 159(2):907-911.
  DOI 10.1093/genetics/159.2.907 PMID 11693127
  PMC1461818. Short letter; it is the paper that names
  the hypothesis. Wave 2 dropped gBGC for lack of a
  single original; this is that lock.
  Not the source: Eyre-Walker A. 1993. Recombination and
  mammalian genome evolution. Proc R Soc Lond B
  252:237-243 (precursor: recombination and GC, not the
  named BGC hypothesis). Eyre-Walker 1999 Genetics
  152:675-683 (selection on silent GC). Marais 2003
  Trends Genet 19:330-338 (review).
One-sentence prediction: Meiotic gene conversion is
  biased toward G/C, so GC (and the W-to-S fixation
  rate) rises where recombination is high, mimicking
  directional selection for GC.
Assumptions: meiotic gene conversion; a known
  recombination map; the GC / W-to-S pattern is sexual
  / meiotic, not methylation-driven C-to-T.
Which fail here: gBGC is a meiotic transmission bias.
  Grafted clones have no meiosis between cuttings. A
  chip skeleton is not a recombination map (same map
  requirement as BGS / Hill-Robertson). Vitis GC is
  also driven by methylation-associated C-to-T
  (Vondras 2019).
Modern data / statistic: GC and W-to-S fixation bias
  in recombination-rate bins on a real Vitis map,
  after clone + IBD filters and after gene-density
  and mutability (CpG / methylation) control.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655) as the WGS panel on
  a real Vitis recombination map. Do not invent a
  grape recombination-map paper; the map is a
  requirement, as in the BGS note.
What would falsify it: GC and the W-to-S fixation
  bias are not higher in high-recombination bins once
  gene density and mutability (CpG / methylation)
  are controlled.
What we will not claim: that a chip GC track is gBGC.
  That Eyre-Walker 1993 or Marais 2003 is the named
  source. That clone methylation C-to-T is conversion.
```

## Later additions
Keep follow-on material in this folder, not in a shared dump:
- `reviews/` — related reviews (not the original paper)
- `research/` — modern tests and follow-ups
- `scripts/` — verification

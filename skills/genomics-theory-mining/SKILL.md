---
name: genomics-theory-mining
description: >
  Dig up a classic genomics or population-genetic theory and test it
  against modern data. Use when the user wants old-theory mining,
  forgotten models, Muller ratchet, background selection, Meselson,
  BDM, DDC, Baker, isolation by distance, gene balance, nearly-neutral,
  hitchhiking, Hill-Robertson, Ohno WGD, or a revival paper that
  is not a methods benchmark.
---

# genomics-theory-mining

The paper is the old math plus a new test, not a review with extra adjectives.
Find the original, list the assumptions, then say which modern data can break them.
Filled notes live in `theories.md` (seventeen notes: eight first wave, nine second wave). One theory per job.

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

## Worked example 1 (lead): Muller's ratchet in clonal / somatic lineages

```
Theory: Muller's ratchet
Original paper (year): Muller HJ. 1964. The relation of recombination to
  mutational advance. Mutat Res 1:2-9. DOI 10.1016/0027-5107(64)90047-8
  PMID 14195748. (PubMed sometimes prints volume 106; venue is vol. 1.)
Named and simulated: Felsenstein J. 1974. The evolutionary advantage of
  recombination. Genetics 78(2):737-756. DOI 10.1093/genetics/78.2.737
  PMID 4448362 PMC1213231. Finite N is required; infinite populations
  show no ratchet.
One-sentence prediction: Without recombination, the class of genomes
  carrying the fewest deleterious mutations is eventually lost by drift
  and cannot be restored, so load ratchets upward.
Assumptions: finite N; mostly deleterious mutations; no (or rare)
  back-mutation / compensatory recombination; asexual or non-recombining
  transmission of the whole haplotype.
Which fail here: grape cultivars are grafted clonal lineages, not
  panmictic sexuals. Meristems, chimeras, and diplontic selection can
  hide or purge load. Somatic clock != germline clock. Structural
  mutations and TEs are part of the load, not just SNPs.
Modern data / statistic: clone-private coding variants and their
  predicted deleteriousness among vegetatively propagated cultivars.
Lead test bed (not a proof): Vondras AM et al. 2019. The genomic
  diversification of grapevine clones. BMC Genomics 20:972.
  DOI 10.1186/s12864-019-6211-2 PMC6907202. Fifteen Zinfandel clones;
  heterozygous mutations richest in repetitive intergenic / methylated
  cytosine; clones accumulate putatively deleterious exonic variants.
Second test (structural, not SNP-only): Carbonell-Bejerano P et al.
  2017. Catastrophic unbalanced genome rearrangements cause somatic
  loss of berry color in grapevine. Plant Physiol 175:786-801.
  DOI 10.1104/pp.17.00715 PMC5619900. Tempranillo Blanco vs Tinto;
  hemizygous deletion of 313 genes including the color locus;
  chromothripsis-like. A SNP-only ratchet test is incomplete.
Plant asexual comparator: Lovell JT et al. 2017. Mutation accumulation
  in an asexual relative of Arabidopsis. PLoS Genet 13(1):e1006550.
  DOI 10.1371/journal.pgen.1006550. Apomictic Boechera retain more
  mutations at conserved sites than sympatric sexuals.
What would falsify it: clone-private coding mutations are NOT enriched
  for deleterious classes, OR the least-loaded haplotype class is
  continually restored (back-mutation, gene conversion, or diplontic
  replacement). Vondras is a test bed, not a demonstration that the
  ratchet has clicked to extinction.
What we will not claim: that grape clones are doomed; that Pol epsilon
  proofreading defects cause the grape ratchet (see hunch below); that
  a cultivar panel is Ne.
```

**TESTABLE HUNCH, not a result:** if leading-strand DNA polymerase epsilon
proofreading is leaky in shoot meristems, the somatic SNV rate rises and a
ratchet-style load should click faster. No published grape Pol-e x clone
result was verified for this skill. Do not write the hunch as a finding.

Sister clone clocks (lineage, not ratchet proof): Roach MJ et al. 2018.
PLoS Genet 14(11):e1007807 (15 Chardonnay clones; 1620 high-confidence
markers). Carrier G et al. 2012. PLoS ONE 7(3):e32973 (Pinot noir; TE
insertions dominate scored polymorphism). Callipo P et al. 2026. Genome
Biol DOI 10.1186/s13059-026-04184-x (23 Pinot noir clones; SNPs/SVs
depleted from coding sequence; CG/CHG methylation reconstructs clone
trees). Zhou Y et al. 2019. Nat Plants 5:965-979 (SVs accrue as recessive
heterozygotes in clonal lineages).

## Dossier (filled; one modern falsifier each)

| Theory | Original (verified) | Prediction | Dies in plants / clones | One modern falsifier |
|--------|---------------------|------------|-------------------------|----------------------|
| Muller ratchet | Muller 1964 Mutat Res 1:2-9; Felsenstein 1974 Genetics 78:737-756 | Least-loaded class is lost and not restored | Sexual recombination; somatic != germline | Vondras 2019 clone-private coding load not deleterious-enriched, or least-loaded class restored |
| Nearly-neutral | Ohta 1973 Nature 246:96-98 | Slightly deleterious fix when \|Nes\| < 1; faster in small Ne | A cultivar collection is not one Ne | Dong 2023 3525-accession WGS: load / dN/dS does not scale with wild vs cultivar Ne |
| Hitchhiking | Maynard Smith and Haigh 1974 Genet Res 23:23-35 | Linked diversity collapses around a sweep | Clonal IBD and pedigree fake a sweep | Dong 2023 color / sex / flavor peaks vanish after clone + IBD filters (caution dataset, not a proof) |
| Hill-Robertson | Hill and Robertson 1966 Genet Res 8:269-294 | Linked selected loci interfere; recombination helps | Chip skeleton is not a recombination map | Selection efficacy not weaker in low-recombination bins on a real Vitis map |
| Gene balance / dosage | Ohno 1970 book; Birchler and Veitia 2007 Plant Cell 19:395-402 | Stoichiometric regulators are dosage-sensitive; WGD retains them | Tandem NLRs are not the same dosage as WGD | Jaillon 2007 palaeo-hexaploid ohnologs: TF / signaling genes not preferentially retained vs tandem NLRs |
| Neutral theory (null) | Kimura 1968 Nature 217:624-626 | Most substitutions are drift of neutrals | Treating "neutral" as a conclusion | Clone-private coding SNPs are systematically adaptive, not a drift null |
| Infinite-sites | Kimura 1969 Genetics 61:893-903; Watterson 1975 Theor Popul Biol 7:256-276 | Each mutation hits a new site; theta from S | Recurrent TE and gene conversion | Carrier 2012 / Vondras 2019: recurrent TE or same-site hits make pi != theta_W |
| McClintock TE | McClintock 1950 PNAS 36:344-355 | Mobile loci generate new mutable alleles | Scoring only SNPs | Method-fair genome-wide census: TE insertions negligible vs SNPs (Carrier 2012 scored the opposite in Pinot) |
| Background selection | Charlesworth, Morgan and Charlesworth 1993 Genetics 134:1289-1303 | Linked neutral diversity falls where deleterious mutation is purged | Chip skeleton is not a recombination map | Diversity not reduced in low-recombination bins on a real Vitis map after gene-density control |
| Meselson effect | Mark Welch and Meselson 2000 Science 288:1211-1215 (test, not a 1960s original) | Alleles diverge without sex | Grape clones are heterozygous diploids with rare sex; Roach 2018 inbreeding cuts the other way | Haplotype divergence in old clones is not higher than sexual wilds after standing heterozygosity |
| Organelle ratchet | Muller 1964 applied to organelles; Lynch 1996 Mol Biol Evol 13:209-220 (animal mt tRNA) | Non-recombining plastid / mt load ratchets | No locked grape plastid popgen paper | Plastid assemblies / haplotypes: organelle coding not excess-deleterious vs nuclear after mu correction |
| BDM incompatibilities | Dobzhansky 1937 Genetics and the Origin of Species (book) | Hybrid inviability is two-locus (or more) | Cultivar x cultivar is not a species cross | Hybrid inviability in vinifera x riparia / rupestris / amurensis maps to a single locus |
| DDC / subfunctionalization | Force et al. 1999 Genetics 151:1531-1545 | Ohnologs partition ancestral subfunctions | Retention is not partitioned expression | Jaillon 2007 ohnolog pairs do not show partitioned expression / function vs random retention |
| Selfish DNA | Doolittle and Sapienza 1980 Nature 284:601-603; Orgel and Crick 1980 Nature 284:604-607 | TEs persist by self-replication | Some copies are domesticated | TE insertions systematically adaptive / domesticated, not mostly insertion-class load (Carrier 2012 / Vondras 2019) |
| Baker's law | Baker 1955 Evolution 9:347-349 | Self-compatible colonists establish after long-distance dispersal | A vineyard is not an island; some sylvestris already carry H haplotypes | Wild sylvestris hermaphrodite at the same rate as cultivars, or sex-locus sweep vanishes after IBD filter |
| Isolation by distance | Wright 1943 Genetics 28:114-138 | Similarity declines with geographic distance | Rivers and humans move vines | IBD slope is zero in wild sylvestris after river / human transport |
| Diplontic selection | Klekowski 1988 Mutation, Developmental Selection, and Plant Evolution (book) | Meristem cell-lineage competition purges somatic load | Recessives and chimeras evade the filter | Clone-private coding mutations not depleted vs intergenic after mutational-opportunity correction |

Seventeen filled notes (eight first wave, nine second wave). Long form in `theories.md`. One theory per job.

Kondrashov 1988 (cost of males) is on the door list but was not filled: it does not map onto grafted clones.
Muller 1942 was not locked on a publisher page and is not cited for BDM.
Flor 1971 is a review and was not used as a theory source.

## Plant / Vitis checks

- Filter clones before any "population" statistic that assumes unrelated sexuals.
- Do not treat a cultivar panel as Ne.
- Somatic mutation and germline mutation are different clocks. Say which one you measured.
- Plastid / TE / graph coordinates are not interchangeable with a 12X SNP panel.
- aDNA samples project onto a modern panel; they do not redefine the theory.
- A real recombination map is required for background selection and Hill-Robertson. A chip skeleton is not that map.
- Standing heterozygosity and ancestral inbreeding (Roach 2018) are not the Meselson effect.
- Wild sylvestris geography is the isolation-by-distance test; a cultivar PCA is not.
- Hermaphroditism is the Baker test (Dong 2023 SDR on chromosome 2), not VviAGL11.
- Diplontic selection in meristems is a caveat on the ratchet, not a replacement theory.

## Sources to open first (fetched)

- Muller 1964: https://doi.org/10.1016/0027-5107(64)90047-8
- Felsenstein 1974: https://doi.org/10.1093/genetics/78.2.737 (PMC1213231)
- Ohta 1973: https://doi.org/10.1038/246096a0
- Maynard Smith and Haigh 1974: https://doi.org/10.1017/s0016672300014634 (PMID 4407212)
- Hill and Robertson 1966: https://doi.org/10.1017/s0016672300010156
- Kimura 1968: https://doi.org/10.1038/217624a0
- Kimura 1969: https://doi.org/10.1093/genetics/61.4.893
- Watterson 1975: https://doi.org/10.1016/0040-5809(75)90020-9
- McClintock 1950: https://doi.org/10.1073/pnas.36.6.344
- Birchler and Veitia 2007: https://doi.org/10.1105/tpc.106.049338 (PMC1867330)
- Vondras 2019: https://doi.org/10.1186/s12864-019-6211-2 (PMC6907202)
- Carbonell-Bejerano 2017: https://doi.org/10.1104/pp.17.00715 (PMC5619900)
- Roach 2018: https://doi.org/10.1371/journal.pgen.1007807
- Carrier 2012: https://doi.org/10.1371/journal.pone.0032973
- Dong 2023: https://doi.org/10.1126/science.add8655 (PMID 36862793)
- Zhou 2019: https://doi.org/10.1038/s41477-019-0507-8
- Jaillon 2007: https://doi.org/10.1038/nature06148
- Lovell 2017: https://doi.org/10.1371/journal.pgen.1006550
- Charlesworth, Morgan and Charlesworth 1993: https://doi.org/10.1093/genetics/134.4.1289 (PMID 8375663 PMC1205596)
- Mark Welch and Meselson 2000: https://doi.org/10.1126/science.288.5469.1211 (PMID 10817991)
- Lynch 1996: https://doi.org/10.1093/oxfordjournals.molbev.a025557 (PMID 8583893)
- Force et al. 1999: https://doi.org/10.1093/genetics/151.4.1531 (PMID 10101175 PMC1460548)
- Doolittle and Sapienza 1980: https://doi.org/10.1038/284601a0 (PMID 6245369)
- Orgel and Crick 1980: https://doi.org/10.1038/284604a0 (PMID 7366731)
- Baker 1955: https://doi.org/10.1111/j.1558-5646.1955.tb01544.x (also 10.2307/2405656)
- Wright 1943: https://doi.org/10.1093/genetics/28.2.114 (PMID 17247074 PMC1209196)
- Klekowski 1988 book: https://doi.org/10.7312/klek92068

## Red lines

- Do not cite a review as the source of the theory.
- Do not apply a sexual-diploid model to clones and call it a test.
- Do not invent citations, years, or the original equation.
- Do not turn this into a 50-theory catalog. One theory per job.
- No unpublished genotypes or private site coordinates in the public note.
- Label Pol-e x ratchet as a TESTABLE HUNCH, never as a grape result.
- Do not cite Mark Welch and Meselson 2000 as a 1960s original.
- Do not invent a grape plastid popgen paper or a grape BDM map.
- Do not write VviAGL11 as the sex gene (Dong 2023 SDR is chromosome 2).

Related: `plant-lit-review`, `vitis-popgen`, `grapevine-adna`, `vitis-pangenome`.

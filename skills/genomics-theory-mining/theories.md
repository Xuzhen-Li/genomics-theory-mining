# Theory notes (filled)

One theory per job. Original paper first. Assumptions, plant/clonal caveats, one modern falsifier.
Do not treat this file as a literature review. Related skill: `plant-lit-review` is the review workflow; this is the revival test.

Citations below were checked against publisher / PubMed / PMC pages. If a paper is not here, it was dropped or left unverified.

---

## Muller's ratchet

```
Theory: Muller's ratchet
Original paper (year): Muller HJ. 1964. The relation of recombination to
  mutational advance. Mutation Research 1:2-9.
  DOI 10.1016/0027-5107(64)90047-8 PMID 14195748.
Named / simulated: Felsenstein J. 1974. The evolutionary advantage of
  recombination. Genetics 78(2):737-756.
  DOI 10.1093/genetics/78.2.737 PMID 4448362 PMC1213231.
One-sentence prediction: In a finite population without recombination, the
  class of genomes with the fewest deleterious mutations is eventually lost
  by drift and cannot be rebuilt, so mutational load ratchets upward.
Assumptions: finite N; mutations mostly deleterious; back-mutation rare;
  no sex / no recombination that restores the least-loaded haplotype.
Which fail here: Vitis cultivars are vegetatively propagated clones (grafted
  meristems), not asexual animals in the Muller sense. Chimeras and diplontic
  selection can hide or purge load. Somatic clock != meiotic clock. Load is
  SNP + SV + TE, not SNPs alone.
Modern data / statistic: clone-private coding variants and predicted
  deleteriousness among vegetatively propagated cultivars.
Lead test bed (not a proof): Vondras AM et al. 2019. The genomic
  diversification of grapevine clones. BMC Genomics 20:972.
  DOI 10.1186/s12864-019-6211-2 PMC6907202. Fifteen Zinfandel clones;
  heterozygous mutations richest in repetitive intergenic / methylated
  cytosine; clones accumulate putatively deleterious exonic variants.
Second test (structural): Carbonell-Bejerano P et al. 2017. Catastrophic
  unbalanced genome rearrangements cause somatic loss of berry color in
  grapevine. Plant Physiol 175:786-801. DOI 10.1104/pp.17.00715
  PMC5619900. Tempranillo Blanco vs Tinto; hemizygous deletion of 313
  genes including the color locus; chromothripsis-like. SNP-only tests
  miss this class of load.
Plant asexual comparator: Lovell JT, Williamson RJ, Wright SI, McKay JK,
  Sharbel TF. 2017. Mutation accumulation in an asexual relative of
  Arabidopsis. PLoS Genet 13(1):e1006550.
  DOI 10.1371/journal.pgen.1006550. Apomictic Boechera accumulate more
  mutations at conserved sites than sympatric sexuals.
What would falsify it: clone-private coding mutations are not enriched for
  deleterious classes, OR the least-loaded haplotype class is continually
  restored (back-mutation, gene conversion, meristem replacement).
What we will not claim: that grape clones are doomed; that Vondras proved
  the ratchet; that Pol epsilon proofreading defects cause a grape ratchet.
```

TESTABLE HUNCH, not a result: leaky Pol epsilon proofreading in meristems
would raise the somatic SNV rate and should speed a ratchet-style click.
No verified grape Pol-e x clone paper was found. Do not publish the hunch
as a finding.

Sister clocks (lineage reconstruction, not ratchet proof):
- Roach MJ et al. 2018. Population sequencing reveals clonal diversity and
  ancestral inbreeding in the grapevine cultivar Chardonnay. PLoS Genet
  14(11):e1007807. DOI 10.1371/journal.pgen.1007807. 15 clones; 1620 markers.
- Carrier G et al. 2012. Transposable elements are a major cause of somatic
  polymorphism in Vitis vinifera L. PLoS ONE 7(3):e32973.
  DOI 10.1371/journal.pone.0032973.
- Callipo P, Robinson H, Schmidt M, Voss-Fels KP. 2026. A dual
  genome-methylome map of clonal evolution in grapevine. Genome Biology.
  DOI 10.1186/s13059-026-04184-x. 23 Pinot noir clones; SNPs/SVs depleted
  from coding sequence; CG/CHG methylation reconstructs clone trees.
- Zhou Y, Minio A, Massonnet M, Solares E, Lv Y, Beridze T, Cantu D,
  Gaut BS. 2019. The population genetics of structural variants in
  grapevine domestication. Nat Plants 5:965-979.
  DOI 10.1038/s41477-019-0507-8. SVs accrue as recessive heterozygotes
  in clonal lineages.

---

## Nearly-neutral theory

```
Theory: Nearly-neutral theory
Original paper (year): Ohta T. 1973. Slightly deleterious mutant
  substitutions in evolution. Nature 246:96-98.
  DOI 10.1038/246096a0 PMID 4585855.
  (Ohta 1992 Annu Rev Ecol Syst 23:263-286 is a later synthesis, not
  the source of the theory.)
One-sentence prediction: Mutations with |Nes| near 1 are fixed or lost
  by the joint action of drift and weak selection; substitution is faster
  when Ne is small.
Assumptions: a meaningful Ne; Wright-Fisher-like transmission; fitness
  effects drawn such that a large class is slightly deleterious.
Which fail here: a cultivar collection is not one Ne. Clonal census,
  nursery bottlenecks, and dual domestication (table vs wine) split Ne
  across histories. Somatic mutations are not substitutions in the Ohta
  sense until they are transmitted.
Modern data / statistic: wild vs cultivar nucleotide diversity and
  0-fold / 4-fold (or dN/dS) ratios on a broad Vitis WGS panel.
What would falsify it: load or dN/dS does not rise where Ne is smaller
  (wild vs cultivated; wine vs table) after clones are filtered.
Dataset: Dong Y et al. 2023. Dual domestications and origin of traits
  in grapevine evolution. Science. DOI 10.1126/science.add8655
  PMID 36862793. 3525 cultivated and wild accessions; use as an Ne
  contrast, not as a single population.
What we will not claim: that a 12X chip panel of wine clones estimates Ne.
```

---

## Hitchhiking / sweeps

```
Theory: Genetic hitchhiking
Original paper (year): Maynard Smith J, Haigh J. 1974. The hitch-hiking
  effect of a favourable gene. Genetical Research 23(1):23-35.
  DOI 10.1017/s0016672300014634 PMID 4407212.
One-sentence prediction: A strongly favoured substitution reduces
  heterozygosity at linked sites, more so when recombination is low.
Assumptions: sexual recombination map; the favoured allele spreads in a
  population of unrelated individuals; linked sites start near equilibrium.
Which fail here: clones and first-degree pedigrees produce long IBD
  that looks like a sweep. Cultivar relatedness is not a selective sweep.
Modern data / statistic: haplotype homozygosity or diversity dips around
  domestication loci after clone and kinship filters.
Caution dataset (not a proof of Maynard Smith-Haigh): Dong et al. 2023
  Science (DOI 10.1126/science.add8655). 3525-accession WGS reports
  domestication-trait peaks (berry color, hermaphroditism, muscat,
  palatability). Relatedness among cultivars can fake those peaks.
What would falsify it: a candidate sweep around color / sex / flavor
  disappears once clones and IBD / pedigree are removed, or the dip is
  no deeper than matched unselected regions of equal relatedness.
What we will not claim: that Dong 2023 demonstrated hitchhiking.
```

---

## Hill-Robertson interference

```
Theory: Hill-Robertson effect
Original paper (year): Hill WG, Robertson A. 1966. The effect of linkage
  on limits to artificial selection. Genetical Research 8:269-294.
  DOI 10.1017/s0016672300010156.
One-sentence prediction: In finite populations, linked selected loci
  interfere with each other's response to selection; recombination
  reduces that interference.
Assumptions: finite N; two (or more) selected loci; a known recombination
  rate; sexual transmission.
Which fail here: a SNP-chip skeleton is not a recombination map. Clonal
  lineages have no meiotic recombination between cuttings. Interference
  in a grafted clone is not the Hill-Robertson experiment.
Modern data / statistic: efficacy of selection (dN/dS, load, or
  polymorphism) binned by recombination rate on a real Vitis map, in
  sexually derived wild or seedling material (not clone-vs-clone).
What would falsify it: selection efficacy is not weaker in
  low-recombination bins after accounting for gene density and
  mutability.
What we will not claim: that clone SNP density along a chip is
  interference.
```

Felsenstein 1974 (above) already ties this effect to the Fisher-Muller
argument and to the ratchet. Same original math; different job.

---

## Gene balance / dosage (Ohno WGD)

```
Theory: Gene balance / dosage after duplication
Original paper (year): Ohno S. 1970. Evolution by Gene Duplication.
  Springer-Verlag. DOI 10.1007/978-3-642-86659-3.
  Modern statement: Birchler JA, Veitia RA. 2007. The gene balance
  hypothesis: from classical genetics to modern genomics. Plant Cell
  19(2):395-402. DOI 10.1105/tpc.106.049338 PMID 17293565 PMC1867330.
One-sentence prediction: Stoichiometric regulators (transcription
  factors, signaling) are dosage-sensitive; whole-genome duplication
  retains them, while tandem duplicates of the same genes are poorly
  tolerated.
Assumptions: the "dose" is gene copy number in a balanced karyotype;
  aneuploidy != polyploidy; ohnologs can be told from tandem copies.
Which fail here: Vitis is palaeo-hexaploid but not a recent polyploid.
  Hemizygous SVs in clones change dose without WGD. Tandem NLR arrays
  are not the same dosage problem as an ohnolog transcription factor.
Modern data / statistic: retention of TF / signaling ohnologs vs tandem
  NLRs in the grape palaeo-hexaploid gene set.
Dataset: Jaillon O et al. 2007. The grapevine genome sequence suggests
  ancestral hexaploidization in major angiosperm phyla. Nature
  449:463-467. DOI 10.1038/nature06148 PMID 17721507. Three ancestral
  genomes; no recent WGD.
Clone-dose companion: Zhou et al. 2019 Nat Plants 5:965-979
  (DOI 10.1038/s41477-019-0507-8) and Carbonell-Bejerano et al. 2017
  (hemizygous deletion of 313 genes). SVs change dose inside a clone.
What would falsify it: Vitis ohnologs of TF / signaling genes are not
  preferentially retained relative to tandem NLR expansions.
What we will not claim: that every grape gene family expansion is
  dosage balance.
```

---

## Neutral theory (null)

```
Theory: Neutral theory of molecular evolution
Original paper (year): Kimura M. 1968. Evolutionary rate at the
  molecular level. Nature 217:624-626.
  DOI 10.1038/217624a0 PMID 5637732.
One-sentence prediction: Most nucleotide substitutions are the random
  fixation of mutations whose fitness effect is negligible; the
  substitution rate equals the neutral mutation rate.
Assumptions: a large class of truly neutral mutations; substitutions
  counted on an evolutionary (germline / sexual) clock.
Which fail here: "neutral" is the null, not a conclusion. Somatic
  clone SNPs are not substitutions. Methylation-driven C-to-T in
  repeats inflates the apparent clock.
Modern data / statistic: site-frequency or dN/dS of clone-private
  coding SNPs versus intergenic / fourfold sites (Vondras 2019;
  Roach 2018; Callipo 2026).
What would falsify it as a null: clone-private coding SNPs are
  systematically adaptive (not drift / nearly-neutral) after
  mutational-opportunity correction.
What we will not claim: that finding "mostly intergenic SNPs" proves
  Kimura 1968. That is the expected mutational target, not a test.
```

---

## Infinite-sites / Watterson

```
Theory: Infinite-sites model and theta from segregating sites
Original paper (year): Kimura M. 1969. The number of heterozygous
  nucleotide sites maintained in a finite population due to steady
  flux of mutations. Genetics 61(4):893-903.
  DOI 10.1093/genetics/61.4.893.
  Estimator: Watterson GA. 1975. On the number of segregating sites
  in genetical models without recombination. Theor Popul Biol
  7(2):256-276. DOI 10.1016/0040-5809(75)90020-9 PMID 1145509.
One-sentence prediction: Each mutation hits a new site, so the number
  of segregating sites estimates 4Ne mu (theta_W) and should match
  pairwise diversity (pi) under neutrality.
Assumptions: infinite sites; no recurrent mutation; no recombination
  in the Watterson 1975 derivation; Wright-Fisher sample of unrelated
  gametes.
Which fail here: TE insertions hit the same families repeatedly.
  Gene conversion and hemizygosity create apparent recurrent SNPs.
  Clone samples are not a random sexual sample.
Modern data / statistic: pi versus theta_W, and recurrent TE insertion
  counts, on clone and cultivar WGS.
Datasets: Carrier et al. 2012 PLoS ONE 7(3):e32973 (147 mobile-element
  insertion events in Pinot noir; TE rate exceeded SNP/indel in the
  scored interval). Vondras et al. 2019 BMC Genomics 20:972 (thousands
  of TE insertions among Zinfandel clones).
What would falsify it: recurrent same-site or same-element events are
  rare enough that pi still equals theta_W after clones are filtered.
What we will not claim: that every TE insertion invalidates Watterson
  on fourfold SNPs. State the site class.
```

---

## McClintock TE (Vitis extra)

```
Theory: Mobile loci generate new mutable alleles
Original paper (year): McClintock B. 1950. The origin and behavior of
  mutable loci in maize. Proc Natl Acad Sci USA 36(6):344-355.
  DOI 10.1073/pnas.36.6.344.
One-sentence prediction: Chromosome-breakage-associated mobile elements
  (Ac/Ds in maize) change position and create new unstable alleles.
Assumptions: the mutability is caused by transposition, not by a
  static SNP; the element can be recovered at the new site.
Which fail here: scoring only SNPs on a 12X panel hides the TE clock.
  Methylation both silences TEs and raises C-to-T in the same repeats
  (Vondras 2019), so "repeat SNPs" are not independent of TEs.
Modern data / statistic: clone-private TE insertion rate versus SNP
  rate in the same cultivar.
Lead test: Carrier et al. 2012 PLoS ONE 7(3):e32973. In Pinot noir,
  insertion polymorphism from mobile elements was the largest scored
  mutational class (147 events; 35.2 / Mb).
Companion: Vondras et al. 2019 (TE insertions plus methylation-driven
  transitions). Zhou et al. 2019 (SVs, including TE-associated, accrue
  as heterozygotes in clones).
What would falsify it: in a genome-wide, method-fair census, clone
  polymorphism is SNP-dominated and TE insertions are negligible.
What we will not claim: that every berry-color sport is a TE
  (Carbonell-Bejerano 2017 is a rearrangement, not a TE proof).
```

---

## Background selection

```
Theory: Background selection
Original paper (year): Charlesworth B, Morgan MT, Charlesworth D. 1993.
  The effect of deleterious mutations on neutral molecular variation.
  Genetics 134(4):1289-1303. DOI 10.1093/genetics/134.4.1289
  PMID 8375663 PMC1205596.
One-sentence prediction: Selection against recurrent deleterious alleles
  reduces linked neutral diversity; the reduction is strongest with
  little or no recombination (and in asexuals or selfers) and is an
  exponential function of the deleterious mutation rate in that segment.
Assumptions: a meaningful recombination map; mutation-selection
  balance at many linked loci; the observed diversity is sexual /
  meiotic, not clone-IBD.
Which fail here: a SNP-chip skeleton is not a recombination map.
  Grafted clones have no meiosis between cuttings. Gene density and
  mutability covary with recombination and can fake a BGS dip.
Modern data / statistic: nucleotide diversity in recombination-rate
  bins on a real Vitis map, after gene-density and mutability control,
  in sexually derived wild or seedling material (not clone-vs-clone).
What would falsify it: diversity is not reduced in low-recombination
  bins after gene-density (and mutability) control.
What we will not claim: that a clone SNP-density track is background
  selection. That is the Hill-Robertson / hitchhiking caution again.
```

Same map requirement as Hill-Robertson. Different job: BGS is the
deleterious-linked null for a diversity dip, not interference among
selected loci.

---

## Meselson effect (allelic divergence in asexuals)

```
Theory: Meselson effect (allelic divergence without sex)
Original paper (year): Mark Welch DB, Meselson M. 2000. Evidence for
  the evolution of bdelloid rotifers without sexual reproduction or
  genetic exchange. Science 288(5469):1211-1215.
  DOI 10.1126/science.288.5469.1211 PMID 10817991.
  This is the molecular TEST of allelic divergence, not a 1960s
  original. Do not cite it as the source of asexuality theory.
One-sentence prediction: After long enough without sex or genetic
  exchange, formerly allelic haplotypes become highly divergent and
  the genome lacks pairs of closely similar sequences.
Assumptions: obligate asexuality for a deep time; no ameiotic
  homogenization; the two copies started as alleles, not ohnologs.
Which fail here: grape cultivars are heterozygous diploids with rare
  sex in the pedigree, not bdelloids. Standing heterozygosity from
  the last outcross is not Meselson divergence. Roach 2018 reports
  ancestral inbreeding in Chardonnay, which cuts the opposite way
  (too little, not too much, haplotype divergence).
Modern data / statistic: haplotype / allelic divergence in old
  vegetatively propagated clones versus sexual wild Vitis, after
  subtracting standing heterozygosity at the last sexual node.
Caution dataset: Roach MJ et al. 2018. PLoS Genet 14(11):e1007807
  (DOI 10.1371/journal.pgen.1007807). 15 Chardonnay clones; ancestral
  inbreeding. Use as a CAUTION, not as a Meselson demonstration.
What would falsify it: haplotype divergence in old clones is not
  higher than in sexual wilds after accounting for standing
  heterozygosity.
What we will not claim: that a grape clone is an ancient asexual;
  that Flot 2013 bdelloid genomics is a Vitis result (dropped).
```

---

## Organelle / plastid Muller ratchet

```
Theory: Muller ratchet in non-recombining organelles
Original paper (year): Muller HJ. 1964. The relation of recombination
  to mutational advance. Mutat Res 1:2-9.
  DOI 10.1016/0027-5107(64)90047-8 PMID 14195748.
  Organelle application (locked): Lynch M. 1996. Mutation accumulation
  in transfer RNAs: molecular evidence for Muller's ratchet in
  mitochondrial genomes. Mol Biol Evol 13(1):209-220.
  DOI 10.1093/oxfordjournals.molbev.a025557 PMID 8583893.
  Lynch 1996 is animal mitochondrial tRNA, not a chloroplast paper
  and not a grape paper.
One-sentence prediction: A non-recombining organelle haplotype cannot
  restore a least-loaded class once it is lost, so mildly deleterious
  substitutions accumulate relative to a recombining nuclear control.
Assumptions: no (or rare) organelle recombination / paternal leakage
  that rebuilds the clean class; a nuclear comparison with a known
  mutation-rate difference; the organelle sample is not one clone.
Which fail here: plastid inheritance in Vitis is typically maternal,
  but biparental leakage and intracellular gene conversion are not
  ruled out by a haplotype label. A cultivar collection is not Ne.
  No grape plastid population-genetic paper was locked for this skill.
Modern data / statistic (dataset type only): complete plastid
  assemblies or haplotype alignments of Vitis, scored for coding
  load or tRNA-stem stability versus nuclear genes after a
  mutation-rate correction.
What would falsify it: plastid coding / tRNA sites are not
  excess-deleterious relative to nuclear genes after mutation-rate
  correction, OR a least-loaded plastid class is continually restored.
What we will not claim: that Lynch 1996 measured grape plastids;
  that a published grape chlorotype paper is a ratchet test (none
  was locked). Do not invent a Vitis plastid popgen citation.
```

---

## Bateson-Dobzhansky-Muller incompatibilities

```
Theory: Bateson-Dobzhansky-Muller hybrid incompatibilities
Original paper (year): Dobzhansky T. 1937. Genetics and the Origin
  of Species. Columbia University Press. Book. Isolating mechanisms
  and hybrid incompatibility as two-locus (or multi-locus) products
  of divergence, not a single substitution that is unfit in the
  ancestor.
  Muller 1942 was not locked on a publisher page and is not cited.
  Bateson 1909 was not locked as the two-locus source and is not cited.
One-sentence prediction: Hybrid inviability or sterility is caused
  by incompatible alleles at two or more loci that never co-occurred
  in either parent lineage.
Assumptions: the parents are diverged populations / species; the
  hybrid phenotype is genetic, not graft incompatibility or virus;
  a single-locus model can be rejected.
Which fail here: a cultivar x cultivar cross is not a species cross.
  Rootstock "failure" can be soil, virus, or graft, not BDM.
  Unreduced gametes and ploidy in Vitis hybrids are not two-locus
  epistasis.
Modern data / statistic (dataset type only): Vitis interspecific
  hybrids (V. vinifera x V. riparia / V. rupestris / V. amurensis)
  or a mapping family from those crosses, scored for inviability /
  sterility QTL. No grape BDM mapping paper was locked.
What would falsify it: hybrid inviability maps to a single locus,
  not two-locus (or multi-locus) BDM.
What we will not claim: that every failed vinifera x American
  rootstock cross is a Dobzhansky incompatibility.
```

---

## DDC / subfunctionalization

```
Theory: Duplication-degeneration-complementation (subfunctionalization)
Original paper (year): Force A, Lynch M, Pickett FB, Amores A,
  Yan YL, Postlethwait J. 1999. Preservation of duplicate genes by
  complementary, degenerative mutations. Genetics 151(4):1531-1545.
  DOI 10.1093/genetics/151.4.1531 PMID 10101175 PMC1460548.
One-sentence prediction: Complementary degenerative mutations
  partition ancestral subfunctions so both duplicates are required;
  preservation need not wait for a new function.
Assumptions: independently mutable subfunctions (often regulatory);
  ohnologs can be told from tandem copies; "partitioned" is scored
  against the ancestral expression / function, not against a
  present-day singleton.
Which fail here: Vitis is palaeo-hexaploid; many "ohnologs" are
  old. Retention by dosage balance (Ohno / Birchler) is a different
  job. Tandem NLR arrays are not DDC.
Modern data / statistic: partitioned expression or function in
  palaeo-hexaploid ohnolog pairs versus randomly retained pairs.
Dataset: Jaillon O et al. 2007. Nature 449:463-467.
  DOI 10.1038/nature06148 PMID 17721507. Three ancestral genomes;
  no recent WGD. Use the ohnolog set. Do not invent a grape
  expression-atlas paper.
What would falsify it: ohnolog pairs do not show partitioned
  expression or function versus randomly retained pairs.
What we will not claim: that every retained grape duplicate is
  DDC (gene-balance is the alternative filled note).
```

---

## Selfish DNA

```
Theory: Selfish DNA
Original papers (year): Doolittle WF, Sapienza C. 1980. Selfish
  genes, the phenotype paradigm and genome evolution. Nature
  284:601-603. DOI 10.1038/284601a0 PMID 6245369.
  Orgel LE, Crick FHC. 1980. Selfish DNA: the ultimate parasite.
  Nature 284:604-607. DOI 10.1038/284604a0 PMID 7366731.
  Same issue; cite both. Neither is a review of the other.
One-sentence prediction: Sequences can spread because they replicate
  inside the genome; no organismal function is required to explain
  their existence.
Assumptions: transposition (or other non-phenotypic survival) is
  demonstrated; "function" is not assumed from presence.
Which fail here: a few TE insertions are domesticated (promoters,
  color sports). Domestication of some copies does not make the
  insertion class adaptive. Scoring only SNPs hides the TE clock.
Modern data / statistic: clone-private TE insertions versus
  adaptive / domesticated annotations in the same cultivar.
Datasets: Carrier et al. 2012 PLoS ONE 7(3):e32973 (147 mobile-
  element insertion events in Pinot noir; TE the largest scored
  class). Vondras et al. 2019 BMC Genomics 20:972 (TE insertions
  among Zinfandel clones).
What would falsify it: TE insertions are systematically
  domesticated or adaptive, not mostly insertion-class load.
What we will not claim: that McClintock 1950 is the selfish-DNA
  paper (different job: mutable alleles). That every berry-color
  sport is a TE (Carbonell-Bejerano 2017 is a rearrangement).
```

---

## Baker's law

```
Theory: Baker's law (self-compatible colonists)
Original paper (year): Baker HG. 1955. Self-compatibility and
  establishment after long-distance dispersal. Evolution
  9(3):347-349. DOI 10.1111/j.1558-5646.1955.tb01544.x
  (also 10.2307/2405656). Pages are sometimes listed 347-348.
One-sentence prediction: After long-distance dispersal, uniparental
  (self-compatible or hermaphrodite) colonists establish more
  readily than self-incompatible or obligately outcrossing ones.
Assumptions: a true colonization step with a mate-finding problem;
  the self-compatible state is derived in the colonists, not
  already fixed in the source.
Which fail here: a nursery or a grafted vineyard is not an oceanic
  island. Humans move both sexes and cuttings. Wild V. sylvestris
  is dioecious; cultivated V. vinifera is mostly hermaphrodite,
  but some wild accessions already carry hermaphrodite haplotypes.
Modern data / statistic: frequency of hermaphrodite sex-locus
  genotypes in wild sylvestris versus cultivars, and whether the
  chromosome-2 sex-determination-region (SDR) sweep survives
  clone and IBD filters.
Dataset: Dong Y et al. 2023. Science. DOI 10.1126/science.add8655
  PMID 36862793. Dual domestications; SDR on chromosome 2;
  hermaphrodite haplotypes (H1, H2 and rarer H types) from
  recombination between male (M) and female (f). Some sylvestris
  accessions in that panel already carry H haplotypes. Use as a
  caution dataset, not a proof of Baker 1955.
What would falsify it: wild sylvestris is already hermaphrodite
  at the same rate as cultivars, OR the sex-locus sweep vanishes
  after IBD / clone filters.
What we will not claim: that VviAGL11 is the sex gene (that name
  is used for seedlessness, not the SDR). That Dong 2023 proved
  Baker's law.
```

---

## Isolation by distance

```
Theory: Isolation by distance
Original paper (year): Wright S. 1943. Isolation by distance.
  Genetics 28(2):114-138. DOI 10.1093/genetics/28.2.114
  PMID 17247074 PMC1209196.
One-sentence prediction: Under limited dispersal, genetic
  similarity declines with geographic distance; the slope is set
  by the neighborhood size.
Assumptions: isolation-by-distance in a continuous or stepping-
  stone sexual population; distance is geographic, not river-km
  or road-km unless you model those as the dispersal kernel;
  samples are not clones or cultivars.
Which fail here: humans and rivers move grapevines. A cultivar
  panel has no geography in the Wright sense. feral vines are
  not wild sylvestris.
Modern data / statistic: isolation-by-distance slope (FST or
  relatedness versus kilometers) in wild V. sylvestris, after
  dropping cultivars, feral escapes, and clones.
Dataset: Dong et al. 2023 Science (DOI 10.1126/science.add8655).
  3525-accession WGS includes wild sylvestris. Use the wild
  subset as a geography test, not the cultivar cloud.
What would falsify it: the isolation-by-distance slope is zero
  after accounting for river and human transport.
What we will not claim: that a wine-region PCA is Wright 1943.
```

---

## Diplontic selection (optional extra)

```
Theory: Diplontic / developmental selection in meristems
Original paper (year): Klekowski EJ. 1988. Mutation, Developmental
  Selection, and Plant Evolution. Columbia University Press.
  DOI 10.7312/klek92068. Book. Cell-lineage competition in
  meristems can purge or fix somatic mutations before they become
  the shoot.
One-sentence prediction: Within a growing plant, cell lineages
  that carry deleterious somatic mutations lose meristem space, so
  the transmitted shoot is cleaner than the raw somatic mutation
  rate.
Assumptions: a structured meristem (layers, initials); a fitness
  effect at the cell or sector level; the mutation is visible to
  that competition (many recessives are not).
Which fail here: grape shoots are chimeric; a sport can be a
  layer-restricted mutant that diplontic selection did not purge.
  Recessive load is invisible in a diploid meristem. Nursery
  selection on cuttings is not Klekowski's cell-lineage filter.
Modern data / statistic: clone-private coding mutations versus
  intergenic / fourfold sites in the same vegetatively propagated
  cultivar (Vondras 2019; Callipo 2026 reports SNPs/SVs depleted
  from coding sequence — a test bed, not a proof).
Companion: Carbonell-Bejerano et al. 2017 (layer-visible
  rearrangement that survived as a color sport).
What would falsify it: clone-private coding mutations are not
  depleted relative to intergenic sites after mutational-
  opportunity correction, OR chimeric load is freely transmitted.
What we will not claim: that coding depletion in Callipo 2026
  proved diplontic selection (constraint and methylation are
  alternatives). That diplontic selection cancels Muller's ratchet
  (it is a caveat in that note, not a replacement).
```

---

## Coalescent (Kingman)

```
Theory: Kingman coalescent
Original paper (year): Kingman JFC. 1982. The coalescent.
  Stochastic Processes and their Applications 13(3):235-248.
  DOI 10.1016/0304-4149(82)90011-4. Continuous-time Markov
  chain on a sample of n members from a large haploid
  population; binary mergers only.
One-sentence prediction: Genealogies of a random sample from
  a large haploid population are binary trees with exponential
  waiting times (the n-coalescent); they are not multiple-merger
  or pedigree stars.
Assumptions: large haploid (or effective-haploid) population;
  a random sample of unrelated individuals; Kingman (binary)
  mergers, not Lambda / multiple-merger coalescents.
Which fail here: Vitis cultivars are grafted clones and close
  pedigrees. A clone panel is not a random sexual sample.
  Identity-by-descent among cuttings produces star-like or
  multiple-merger genealogies that are not Kingman.
Modern data / statistic: inferred tree shape or multiple-merger
  signal in clone and first-degree pedigree samples versus a
  clone-filtered wild sexual sample.
Datasets: Roach et al. 2018 PLoS Genet 14(11):e1007807
  (15 Chardonnay clones; ancestral inbreeding). Vondras et al.
  2019 BMC Genomics 20:972 (15 Zinfandel clones). Dong et al.
  2023 Science (DOI 10.1126/science.add8655) already dropped
  IBS clones before population analyses; that filter is the
  first step, not a Kingman proof.
What would falsify it: clone / pedigree samples still yield
  Kingman (binary, unrelated) genealogies after relatedness
  is scored.
What we will not claim: that every grape tree that is not
  binary disproves Kingman in wild sylvestris. State the
  sample class.
```

---

## Infinite-alleles

```
Theory: Infinite-alleles model
Original paper (year): Kimura M, Crow JF. 1964. The number
  of alleles that can be maintained in a finite population.
  Genetics 49(4):725-738. DOI 10.1093/genetics/49.4.725
  PMID 14156929 PMC1210609.
One-sentence prediction: Each mutation creates a new allele,
  so identity-by-state is identity-by-descent; the effective
  number of alleles is 4Ne u + 1 under neutrality.
Assumptions: an astronomically large allelic state space;
  back-mutation / recurrent mutation negligible; a finite
  sexual population with a meaningful Ne.
Which fail here: SNP chips ascertain a finite, recurrent
  state space (mostly biallelic). Same-site SNPs and TE
  family insertions are recurrent. A cultivar collection
  is not one Ne. Identity-by-state among clones is not
  identity-by-descent in the Kimura-Crow sense.
Modern data / statistic: recurrent same-site or same-element
  events, and IBS versus IBD, on cultivar chips or WGS
  after clone filters.
Datasets: Carrier et al. 2012 PLoS ONE 7(3):e32973 (recurrent
  TE insertions in Pinot noir). Vondras et al. 2019 BMC
  Genomics 20:972 (TE plus methylation-driven transitions
  among Zinfandel clones). Dong et al. 2023 Science (WGS;
  they already used IBS to collapse clone genotypes).
  Do not invent a grape chip-ascertainment paper.
What would falsify it: identity-by-state on Vitis chips
  (or WGS SNPs) behaves as infinite-alleles after clones
  are filtered — recurrent SNPs and ascertainment are
  rare enough not to matter.
What we will not claim: that infinite-alleles is the same
  job as infinite-sites (that note is already filled).
```

---

## Molecular clock

```
Theory: Molecular clock
Original paper (year): Zuckerkandl E, Pauling L. 1962.
  Molecular disease, evolution, and genic heterogeneity.
  In: Kasha M, Pullman B, eds. Horizons in Biochemistry.
  Academic Press, New York / London. Chapter begins p. 189
  (next chapter p. 229 in the 1962 volume table of contents;
  archive scan of the book). Book chapter.
  Expanded statement: Zuckerkandl E, Pauling L. 1965.
  Evolutionary divergence and convergence in proteins.
  In: Bryson V, Vogel HJ, eds. Evolving Genes and Proteins.
  Academic Press. pp. 97-166.
  DOI 10.1016/B978-1-4832-2734-4.50017-6.
  (Zuckerkandl and Pauling 1965 J. Theor. Biol. 8:357-366,
  "Molecules as documents of evolutionary history", is a
  different paper and is not cited as the clock source.)
One-sentence prediction: Sequence difference between
  lineages accumulates roughly linearly with elapsed time
  on a germline / sexual clock, so divergence dates
  molecules.
Assumptions: a roughly constant substitution rate on the
  clock being dated; substitutions, not somatic SNPs;
  the compared lineages share a sexual / meiotic clock.
Which fail here: somatic mutation in grafted clones is
  not the germline clock. Methylation-driven C-to-T in
  repeats inflates the clone clock. A cultivar panel is
  not elapsed speciation time.
Modern data / statistic: somatic SNV / SV rate among
  vegetatively propagated clones versus divergence among
  sexual wild sylvestris on the same site classes.
Datasets: Vondras et al. 2019 BMC Genomics 20:972 and
  Roach et al. 2018 PLoS Genet 14(11):e1007807 (clone
  clocks). Wild contrast: Dong et al. 2023 Science
  (sylvestris subset). Callipo et al. 2026 Genome Biol
  is a sister clone / methylome clock only, not a
  germline-clock proof.
What would falsify it: the somatic clone clock equals
  the germline / sexual clock (Vondras / Roach versus
  wild sylvestris) on matched site classes.
What we will not claim: that a clone tree dated in
  years since planting is Zuckerkandl-Pauling.
```

---

## McDonald-Kreitman

```
Theory: McDonald-Kreitman test
Original paper (year): McDonald JH, Kreitman M. 1991.
  Adaptive protein evolution at the Adh locus in
  Drosophila. Nature 351:652-654.
  DOI 10.1038/351652a0 PMID 1904993.
One-sentence prediction: Under neutrality, the ratio of
  replacement to synonymous differences fixed between
  species equals the ratio of replacement to synonymous
  polymorphisms within species; excess fixed replacements
  reject neutrality (MK alpha).
Assumptions: "fixed differences" are substitutions
  between species or diverged populations; polymorphisms
  are within a sexual population; clones are not a species.
Which fail here: clone-private variants are not
  substitutions. A cultivar panel is not Drosophila
  melanogaster versus simulans. Domestication loci are
  not automatically between-species fixed differences.
Modern data / statistic: MK tables at domestication
  loci after clone and IBD filters, counting only
  variants that are fixed between wild sylvestris and
  cultivated groups (not clone-private SNPs).
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). 3525-accession WGS;
  domestication-trait peaks exist. Do not invent a
  published grape MK paper.
What would falsify it: MK alpha on clone-private
  variants is treated as meaningful (it is not), OR
  after clone / IBD filters, grape MK does not reject
  neutrality at domestication loci.
What we will not claim: that Dong 2023 computed MK
  alpha. That clone-private missense SNPs are
  substitutions.
```

---

## Tajima's D

```
Theory: Tajima's D
Original paper (year): Tajima F. 1989. Statistical
  method for testing the neutral mutation hypothesis
  by DNA polymorphism. Genetics 123(3):585-595.
  DOI 10.1093/genetics/123.3.585 PMID 2513255
  PMC1203831.
One-sentence prediction: Under the neutral mutation
  model, theta from pairwise differences (pi) equals
  theta from segregating sites (theta_W); D measures
  that difference and is near zero at equilibrium.
Assumptions: a random sexual sample; infinite sites;
  no relatedness structure that inflates rare or
  shared haplotypes; the sample is one population.
Which fail here: cultivar panels are clones and
  pedigrees. Relatedness and recent bottlenecks
  produce strongly negative D that looks like a
  sweep. A chip skeleton is not a random sample
  of sites.
Modern data / statistic: genome-wide or
  domestication-locus Tajima's D in cultivar panels
  before versus after clone and IBD / pedigree
  filters, versus wild sylvestris.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). They already
  collapsed IBS clones. Use as a relatedness caution,
  not as a published Tajima result. Do not invent
  a grape Tajima paper.
What would falsify it: strongly negative D in
  cultivar panels vanishes after clone + IBD
  filters (relatedness, not a sweep).
What we will not claim: that negative D in wine
  clones is a selective sweep. That is the
  hitchhiking caution again.
```

---

## Mutation accumulation

```
Theory: Mutation accumulation
Original paper (year): Mukai T. 1964. The genetic
  structure of natural populations of Drosophila
  melanogaster. I. Spontaneous mutation rate of
  polygenes controlling viability. Genetics
  50(1):1-19. DOI 10.1093/genetics/50.1.1
  PMID 14191352 PMC1210633. Chromosomes sheltered
  from selection accumulate viability-reducing
  mutations.
  Plant comparator (not the original): Lovell JT
  et al. 2017. Mutation accumulation in an asexual
  relative of Arabidopsis. PLoS Genet 13(1):e1006550.
  DOI 10.1371/journal.pgen.1006550.
One-sentence prediction: When selection is relaxed,
  mildly deleterious mutations accumulate and mean
  fitness / viability declines; the least-loaded
  class is not restored.
Assumptions: a sheltered chromosome or asexual
  lineage; mutations are mostly deleterious;
  fitness is scored on the sheltered haplotype,
  not on a chimeric shoot.
Which fail here: grape clones are diploid meristems
  with diplontic selection and chimeras. Somatic
  load is not a Mukai second-chromosome cage.
  Nursery selection on cuttings is not relaxed
  in the Mukai sense.
Modern data / statistic: clone-private coding
  load and predicted deleteriousness after
  diplontic / chimera correction, versus
  intergenic / fourfold sites.
Lead test bed (not a proof): Vondras et al. 2019
  BMC Genomics 20:972. Companion structural load:
  Carbonell-Bejerano et al. 2017 Plant Physiol
  175:786-801. Plant asexual comparator: Lovell
  2017 (Boechera).
What would falsify it: clone-private load is not
  enriched for deleterious classes after diplontic
  / chimera correction, OR the least-loaded class
  is continually restored.
What we will not claim: that Vondras proved Mukai
  in grape. That this note replaces Muller's
  ratchet (different job: MA is the experiment;
  the ratchet is the irreversible loss of the
  least-loaded class).
```

---

## Genetic draft

```
Theory: Genetic draft (pseudohitchhiking)
Original paper (year): Gillespie JH. 2000. Genetic
  drift in an infinite population. The
  pseudohitchhiking model. Genetics 155(2):909-919.
  DOI 10.1093/genetics/155.2.909 PMID 10835409
  PMC1461093. Names "genetic draft" for the
  stochastic effects of linked substitutions at
  a closely linked neutral locus.
  (Gillespie 2001 Evolution 55:2161-2169 is a
  later population-size paper, not the naming
  source.)
One-sentence prediction: Recurrent selected
  substitutions induce drift-like stochasticity
  at linked neutral sites even when N is infinite;
  the coalescent has a random number of branches
  at nodes and the frequency spectrum departs
  from the equilibrium neutral model.
Assumptions: recurrent sweeps (not one hitchhiking
  event); a recombination map; the diversity
  pattern is sexual / meiotic, not clone-IBD.
Which fail here: a SNP-chip skeleton is not a
  recombination map. Clone IBD looks like draft.
  Background selection is the deleterious-linked
  null for the same diversity dip (already filled).
  A single domestication sweep is hitchhiking
  (Maynard Smith and Haigh), not draft.
Modern data / statistic: diversity versus
  recombination on a real Vitis map, after gene-
  density control and clone / IBD filters, in
  sexually derived wild or seedling material.
What would falsify it: the linked diversity
  pattern in Vitis is explained by recombination
  / background selection, not by recurrent sweeps
  / draft.
What we will not claim: that a cultivar diversity
  dip is Gillespie draft. That draft replaces
  hitchhiking or BGS (three different jobs).
```

---

## Introgression / hybrid swarm

```
Theory: Introgressive hybridization / hybrid swarm
Original paper (year): Anderson E. 1949.
  Introgressive Hybridization. John Wiley and
  Sons, New York. Book. Pp. ix + 109 (locked from
  the 1950 Nature review of the book). Repeated
  backcrossing moves genes from one species into
  another; hybrid swarms are the visible mix.
One-sentence prediction: After hybridization,
  repeated backcrossing leaves geographically
  clinal tracts of heterospecific ancestry, not
  a one-off F1.
Assumptions: the parents are distinguishable
  populations / species; tracts are ancestry,
  not shared IBD among relatives; geography
  is the test, not a cultivar PCA.
Which fail here: humans move vines. Cultivar
  relatedness and clones fake introgression
  tracts. A nursery hybrid is not a hybrid
  swarm. Feral vines are not wild sylvestris.
Modern data / statistic: putative introgression
  tracts and their geographic cline in wild
  sylvestris or in clone-filtered cultivated
  groups, after IBD / clone filters.
Caution dataset (not a proof of Anderson 1949):
  Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). TreeMix and
  D-statistics report gene flow from Syl-W into
  CG3-CG6 after CG1-related Western Asia
  domesticates entered Europe (~11-18% Syl-W
  in those groups; a further pulse into CG6).
  They already collapsed IBS clones. Relatedness
  among remaining cultivars can still fake
  tracts. Use as CAUTION.
What would falsify it: putative introgression
  tracts vanish after IBD / clone filters, or
  they are not geographically clinal.
What we will not claim: that Dong 2023 proved
  Anderson 1949. That a CG1-to-Syl-W arrow is
  the paper's TreeMix result (the reported
  edges run from Syl-W into cultivated groups).
```

---

## Haldane's rule

```
Theory: Haldane's rule
Original paper (year): Haldane JBS. 1922. Sex
  ratio and unisexual sterility in hybrid animals.
  Journal of Genetics 12(2):101-109.
  DOI 10.1007/BF02983075. IAS Journal of Genetics
  page locked: "When in the F1 offspring of a
  cross between two animal species or races one
  sex is absent, rare, or sterile, that sex is
  always the heterozygous sex."
One-sentence prediction: In animal interspecific
  hybrids, the sex that is absent, rare, or
  sterile is the heterozygous (digametic) sex.
Assumptions: a heterogametic sex (XX/XY or
  ZW/ZZ) whose sex chromosomes are unpaired in
  one sex; the sterility is that sex, not both;
  the cross is an animal hybrid.
Which fail here: this does not map onto Vitis
  SDR. Grape is not XX/XY or ZW in the Haldane
  sense. Sex is a small sex-determination region
  on chromosome 2 (Dong 2023); wild sylvestris
  is dioecious (male M/f, female f/f) and
  cultivated vines are mostly hermaphrodite.
  There is no heterogametic sex whose hybrids
  are the sterile class.
Modern data / statistic: none that tests
  Haldane in grape. Interspecific Vitis hybrid
  sterility, if scored, is not a heterogametic-
  sex contrast.
What would falsify it: not applicable as a
  grape test. The note is filled as "does not
  map onto Vitis SDR" rather than as an
  invented sterility experiment.
What we will not claim: that grape interspecific
  hybrids show Haldane's rule. That the SDR is
  a Y chromosome in the animal sense. That
  VviAGL11 is the sex gene.
```

---

## Stepping-stone model

```
Theory: Stepping-stone model
Original paper (year): Kimura M, Weiss GH. 1964. The stepping stone
  model of population structure and the decrease of genetic
  correlation with distance. Genetics 49(4):561-576.
  DOI 10.1093/genetics/49.4.561 PMID 17248204 PMC1210594.
  (Kimura 1953 Annual Report of the National Institute of Genetics
  Japan 3:62-63 is a one-page note; 1964 is the paper. Weiss and
  Kimura 1965 J Appl Probab 2:129-149 is later math.)
  Distinct from filled IBD: Wright 1943 is continuous isolation by
  distance. Stepping-stone is discrete neighbor-only migration.
One-sentence prediction: In a lattice of demes that exchange
  migrants only with neighbors, genetic correlation declines with
  the number of steps between demes (and with dimension).
Assumptions: a lattice of demes; migration only to neighbors;
  correlation is a function of steps, not Euclidean distance as
  such; samples are demes, not clones or cultivars.
Which fail here: a cultivar PCA is not a lattice. Humans and
  rivers move vines farther than one step. Grafted clones are
  not demes.
Modern data / statistic: genetic correlation versus step-count
  and versus Euclidean distance among wild V. sylvestris patches
  after clone / pedigree filters.
Dataset: Dong Y et al. 2023. Science. DOI 10.1126/science.add8655
  PMID 36862793. 3525-accession WGS; use wild sylvestris only
  after clone / pedigree filter.
What would falsify it: correlation among wild patches is not
  higher along neighbor-connected habitat (river / corridor)
  than at equal Euclidean distance, or the decay is no steeper
  than Wright 1943 continuous IBD.
What we will not claim: that a wine-region PCA is a stepping-
  stone lattice. That this note replaces Wright 1943 IBD
  (different job: discrete neighbor steps vs continuous
  distance).
```

---

## Island model

```
Theory: Island model
Original paper (year): Wright S. 1931. Evolution in Mendelian
  populations. Genetics 16(2):97-159.
  DOI 10.1093/genetics/16.2.97 PMID 17246615 PMC1201091.
  Named: Wright 1943 Genetics 28:114-138 (already filled as IBD)
  writes "we shall refer to it as the island model" and cites
  1931 for the math. Lock 1931 as the source, the same way
  Muller 1964 is the ratchet math and Felsenstein 1974 named it.
  Distinct from filled IBD: island / continent-island has no
  distance. Every deme draws migrants from the same pool.
  FST ~ 1 / (1 + 4Nem). IBD is the distance-dependent
  alternative Wright himself set against this model.
One-sentence prediction: Among equal demes that exchange
  migrants with a common pool (not with neighbors only),
  differentiation is a function of Nem and does not increase
  with geographic distance.
Assumptions: equal demes; a common migrant pool (not neighbor-
  only); no distance dependence of FST; samples are demes,
  not pedigrees or cultivars.
Which fail here: a vineyard is not an island. Nursery stock
  and rivers violate the equal-m pool. Cultivar panels are
  pedigrees, not demes.
Modern data / statistic: FST among wild V. sylvestris patches
  versus geographic distance after river / human transport
  is controlled.
Dataset: Dong et al. 2023 Science (DOI 10.1126/science.add8655).
  Wild sylvestris subset after clone filter.
What would falsify it: FST among wild patches is not
  independent of distance after river / human transport is
  controlled (nonzero IBD slope kills the island null; that
  is Wright's own 1943 contrast).
What we will not claim: that a vineyard block is an island
  deme. That this note replaces Wright 1943 IBD (Wright
  himself set the two models against each other).
```

---

## Clonal interference

```
Theory: Clonal interference
Original paper (year): Gerrish PJ, Lenski RE. 1998. The fate
  of competing beneficial mutations in an asexual population.
  Genetica 102:127-144 (often cited 102/103:127-144; Springer
  landing is vol. 102). DOI 10.1023/A:1017067816551.
  No PMID on the Springer page.
  Not the original: Muller HJ. 1932. Some genetic aspects of
  sex. Am Nat 66:118-138. Precursor for the advantage of
  recombination / ratchet, already dropped as a ratchet
  original. Gerrish and Lenski name "clonal interference"
  and derive the fixation / substitution results.
  Distinct from filled Hill-Robertson: HR is interference
  among linked selected loci with recombination. CI is the
  asexual case: competing beneficials cannot recombine onto
  one haplotype, so the weaker is lost.
One-sentence prediction: In a finite asexual population,
  beneficial mutations that arise on different clones compete;
  the weaker is driven out before fixation, so the substitution
  rate saturates with N and U_b.
Assumptions: finite N; asexual transmission; two (or more)
  competing beneficials on different haplotypes; no
  recombination that joins them.
Which fail here: a grafted cultivar is asexual between
  cuttings, but the "population" is a nursery of cuttings
  from one founder, not an E. coli chemostat. Most scored
  grape sports are single-locus (color, hair) on one clone,
  not two competing beneficials in one finite N.
Modern data / statistic: clone-private putatively beneficial
  (or phenotype-changing) mutations across sister clones;
  test for mutual exclusion of competitor classes.
Datasets: Vondras et al. 2019 BMC Genomics 20:972; Roach
  et al. 2018 PLoS Genet 14(11):e1007807; Carrier et al.
  2012 PLoS ONE 7(3):e32973. Clone panels.
What would falsify it: clone-private putatively beneficial
  (or phenotype-changing) mutations do not show mutual
  exclusion across sister clones (both persist; no lost
  competitor class). A single-sport color loss (not two
  competing sports) is not CI.
What we will not claim: that a color sport is clonal
  interference. That this note replaces Hill-Robertson
  (different job: asexual competing beneficials vs linked
  selected loci with recombination).
```

---

## Allele surfing / range expansion

```
Theory: Allele surfing / range expansion
Original paper (year): Edmonds CA, Lillie AS, Cavalli-Sforza
  LL. 2004. Mutations arising in the wave front of an
  expanding population. Proc Natl Acad Sci USA 101(4):975-979.
  DOI 10.1073/pnas.0308064100 PMID 14732681 PMC327127.
  Named "surfing": Klopfstein S, Currat M, Excoffier L. 2006.
  The fate of mutations surfing on the wave of a range
  expansion. Mol Biol Evol 23(3):482-490.
  DOI 10.1093/molbev/msj057 PMID 16280540. Later name, not
  the source. Lande is not this claim (quantitative genetics
  / founder effect, not wave-front surfing).
One-sentence prediction: A mutation that arises (or is
  sampled) at the front of a range expansion can reach a
  much higher frequency and wider spatial range than the
  same mutation in a stationary population, by repeated
  founder events.
Assumptions: a single expanding front; the mutation is
  sampled at the wave front; geography is the expansion,
  not human transport or dual domestication.
Which fail here: domestication is not a single expanding
  front. Dual domestication (Dong 2023 table vs wine) and
  human transport break the wave. Cultivar relatedness
  fakes a front-to-core cline.
Modern data / statistic: frequency of alleles at a putative
  expansion edge of wild or early-cultivated Vitis versus
  core frequencies, after clone + IBD filters, versus
  matched non-expansion alleles.
Dataset: Dong et al. 2023 Science (DOI 10.1126/science.add8655).
What would falsify it: high-frequency alleles at the
  putative expansion edge of wild or early-cultivated
  Vitis are not in excess of core frequencies after clone
  + IBD filters, or the excess is no larger than matched
  non-expansion alleles (surfing null dies; selection /
  pedigree remains).
What we will not claim: that a cultivar relatedness cline
  is surfing. That Klopfstein 2006 is the source (it named
  the phenomenon).
```

---

## Genome shock

```
Theory: Genome shock
Original paper (year): McClintock B. 1984. The significance
  of responses of the genome to challenge. Science
  226(4676):792-801. DOI 10.1126/science.15739260
  PMID 15739260. Nobel lecture 8 December 1983, Karolinska
  Institutet; the Science paper is the published text. She
  writes "shocks" / "responses of the genome to challenge."
  "Genome shock" is the later name for that claim. Not a
  PNAS paper.
  Distinct from filled McClintock 1950: 1950 is the origin
  and behavior of mutable loci (Ac/Ds). 1984 is the claim
  that unprepared stress restructures the genome (TE
  mobilization, rearrangements) as a response.
One-sentence prediction: A challenge the genome is
  unprepared for (breakage, hybridization, tissue-culture
  shock) mobilizes elements and restructures chromosomes;
  programmed shocks (heat shock, SOS) do not.
Assumptions: an unprepared challenge (not a constitutive
  clock); the response is TE mobilization / rearrangement,
  not a SNP clock; programmed shocks are a different class.
Which fail here: a constitutive somatic TE clock is not a
  shock response. Grafting and nursery propagation are
  chronic, not a single challenge. Scoring only SNPs hides
  the TE / SV class.
Modern data / statistic: clone-private TE insertions and
  SVs clustered on shock-associated nodes (hybridization,
  culture, color-sport events) versus a constitutive
  per-year somatic clock.
Datasets: Carrier et al. 2012 PLoS ONE 7(3):e32973;
  Vondras et al. 2019 BMC Genomics 20:972. SVs: Zhou et al.
  2019 Nat Plants 5:965-979.
What would falsify it: clone-private TE insertions (and
  SVs: Zhou 2019) are not clustered on shock-associated
  nodes versus a constitutive per-year somatic clock. A
  method-fair census that is SNP-dominated would also kill
  the 1984 claim as a grape mechanism (same census as the
  1950 TE note, different job: timing vs presence).
What we will not claim: that McClintock 1950 is the genome-
  shock paper (different job: mutable alleles). That a
  constitutive clone TE clock is a shock response.
```

---

## Allopolyploidy / secondary polyploidy

```
Theory: Allopolyploidy / secondary polyploidy
Original paper (year): Stebbins GL. 1947. Types of
  polyploids: their classification and significance.
  Advances in Genetics 1:403-429.
  DOI 10.1016/S0065-2660(08)60490-3 (also
  10.1016/s0065-2660(08)60490-3). No PMID (book-series
  chapter). ScienceDirect landing 406; title / year /
  venue / pages / DOI locked from citing publisher pages
  and the DOI string itself (same standard as Klekowski
  1988 / Ohno 1970).
  Not used as the source: Stebbins 1940 Am Nat 74:54-66
  DOI 10.1086/280872 (significance of polyploidy; earlier,
  not the auto / allo / segmental classification).
  Stebbins 1950 Variation and Evolution in Plants (book,
  later synthesis).
  Distinct from filled gene balance / Ohno: Ohno 1970 and
  Birchler 2007 are dosage after duplication. Stebbins
  1947 is the classification of polyploid types (auto,
  allo, segmental allo) and the role of secondary /
  palaeo-polyploidy.
One-sentence prediction: Allopolyploids combine
  differentiated genomes; segmental allopolyploids pair
  as if auto at some segments; secondary polyploids
  (palaeo-polyploids) diploidize and hide the event in
  chromosome number.
Assumptions: polyploid type (auto / allo / segmental)
  can be scored from pairing or subgenome differentiation;
  secondary / palaeo-polyploids are distinguished from
  recent allo events; tandem arrays are not homoeologs.
Which fail here: Vitis is palaeo-hexaploid, not a recent
  allopolyploid. Hemizygous SVs in clones change dose
  without a new WGD. Tandem NLR arrays are not homoeologs.
Modern data / statistic: recovery of differentiated
  homoeologous subgenomes versus three palaeo-hexaploid
  ancestral genomes; retention of TF / signaling ohnologs
  versus tandem NLRs.
Dataset: Jaillon O et al. 2007. Nature 449:463-467.
  DOI 10.1038/nature06148 PMID 17721507. Three ancestral
  genomes; no recent WGD. Companion: Zhou et al. 2019
  Nat Plants 5:965-979 (SVs change dose inside a clone
  without WGD).
What would falsify it: the three ancestral genomes are
  not recovered as two (or more) differentiated
  homoeologous subgenomes of a recent allo event, or TF
  / signaling ohnologs are not the retained class versus
  tandem NLRs (gene-balance companion, different job).
  Zhou 2019 SVs change dose inside a clone without WGD.
What we will not claim: that Jaillon 2007 is a recent
  allopolyploid. That this note replaces gene balance /
  Ohno (different job: polyploid type vs dosage after
  duplication). That Stebbins 1940 or 1950 is the source.
```

---

## Drift-barrier hypothesis

```
Theory: Drift-barrier hypothesis
Original paper (year): Lynch M. 2011. The lower bound to
  the evolution of mutation rates. Genome Biol Evol
  3:1107-1118. DOI 10.1093/gbe/evr066 PMID 21821597
  PMC3194889. Original research (theory + comparison to
  published rates). Not a review.
  Not the source: Lynch 2010 Trends Genet 26:345-352 is
  a review (red line). Sung W, Ackerman MS, Miller SF,
  Doak TG, Lynch M. 2012. Drift-barrier hypothesis and
  mutation-rate evolution. PNAS 109(45):18488-18492.
  DOI 10.1073/pnas.1216223109 PMID 23077252 PMC3494944
  is the empirical named-title follow-up; cite as the
  test, not the source.
  Distinct from filled nearly-neutral: Ohta 1973 is
  fixation of slightly deleterious alleles when |Nes| ~ 1.
  Drift-barrier is evolution of the mutation rate itself
  (proofreading / repair) to a floor set by 1/Ne.
One-sentence prediction: Selection pushes the mutation
  rate down until further antimutator advantages fall
  below the power of drift, so per-site mu scales
  negatively with Ne (and with coding target size).
Assumptions: a meaningful Ne; the trait is the mutation
  rate (proofreading / repair), not the load of slightly
  deleterious alleles; mu is germline / sexual, not
  somatic clone mu.
Which fail here: a cultivar collection is not one Ne.
  Somatic clone mu is not the germline / sexual mu the
  theory is about. Dual domestication splits Ne.
Modern data / statistic: per-generation per-site
  mutation rate (not load; load is Ohta) in wild versus
  cultivated lineages after clones are filtered.
Dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Wild vs cultivar Ne
  contrast after clone filter. No locked grape wild-vs-
  cultivar mu paper; Vondras 2019 / Roach 2018 are
  clone-somatic clocks, usable only as a sister somatic-
  mu dataset, not as the species-level test. Do not
  invent a grape mutation-rate paper.
What would falsify it: per-generation per-site mutation
  rate (not load) is not higher in the smaller-Ne
  cultivated lineages after clones are filtered.
What we will not claim: that Lynch 2010 is the source
  (review). That Vondras / Roach measured species-level
  mu. That load (Ohta) is the drift-barrier test.
```

---

## GC-biased gene conversion

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

---

## Soft sweep

```
Theory: Soft sweep
Original paper (year): Hermisson J, Pennings PS. 2005.
  Soft sweeps: molecular population genetics of
  adaptation from standing genetic variation.
  Genetics 169(4):2335-2352.
  DOI 10.1534/genetics.104.036947 PMID 15716498
  PMC1449620.
  Distinct from filled hitchhiking: Maynard Smith and
  Haigh 1974 is the hard-sweep / new-mutation hitchhike.
  Soft sweep is multiple copies (standing variation or
  recurrent mutation) contributing to the substitution,
  so linked diversity is only partly erased.
One-sentence prediction: Adaptation from standing
  variation (or from recurrent new mutation) produces
  a soft sweep: more than one ancestral haplotype of
  the selected allele survives, and the hitchhiking
  dip is shallower than a hard sweep of equal s.
Assumptions: more than one copy of the selected allele
  (standing or recurrent); a sexual sample; linked
  diversity is not clone-IBD or first-degree pedigree.
Which fail here: cultivar relatedness and first-degree
  pedigrees produce long shared haplotypes that look
  like a hard sweep (Dong 2023 caution, same as
  hitchhiking). Ascertainment of "the" domestication
  allele on a 12X / cultivar panel hides extra
  haplotypes. Clones are not a random sexual sample.
Modern data / statistic: haplotype count and residual
  linked diversity at domestication peaks (color /
  sex / flavor) after clone + IBD filters.
Caution dataset: Dong et al. 2023 Science
  (DOI 10.1126/science.add8655). Color / sex / flavor
  peaks. Standing hermaphrodite haplotypes H1/H2
  already in some sylvestris (Dong 2023 SDR) are the
  ascertainment / standing-variation test, not
  VviAGL11.
What would falsify it: if a candidate domestication
  haplotype is a single star phylogeny (hard), the
  soft-sweep claim dies for that locus. If several
  independent haplotypes carry the selected allele
  at residual linked diversity, the hard-sweep
  (Maynard Smith-Haigh) claim dies.
What we will not claim: that Dong 2023 demonstrated
  a soft sweep. That VviAGL11 is the sex-locus test
  (SDR H1/H2 is). That this note replaces hitchhiking
  (hard vs soft are different jobs).
```

---

## Chimera / tunica-corpus meristem layers

```
Theory: Chimera / tunica-corpus meristem layers
Original paper (year): Satina S, Blakeslee AF, Avery
  AG. 1940. Demonstration of the three germ layers
  in the shoot apex of Datura by means of induced
  polyploidy in periclinal chimeras. Am J Bot
  27(10):895-905.
  DOI 10.1002/j.1537-2197.1940.tb13952.x
  JSTOR 2436558. No PMID. Wiley landing Cloudflare-
  blocked; CSHL repository page opened.
  Modern grape lock (allowed by the brief): Franks T,
  Botta R, Thomas MR, Franks J. 2002. Chimerism in
  grapevines: implications for cultivar identity,
  ancestry and genetic improvement. Theor Appl Genet
  104:192-199. DOI 10.1007/s001220100683
  PMID 12582686 (PMID from citing PubMed pages).
  Pinot Meunier: three VVS2 alleles; L1 vs L2 split
  by somatic embryogenesis yield two genotypes /
  phenotypes.
One-sentence prediction: The shoot apex is a layered
  meristem (tunica-corpus). A mutation in one layer
  can stabilize as a periclinal chimera; the layers
  have independent genotypes and can be separated.
Assumptions: a layered meristem whose layers keep
  independent genotypes; a periclinal chimera is
  stable and separable; layer count is scored, not
  assumed from a mixed-leaf SSR.
Which fail here: Datura has three germ layers. Vitis
  SAM is two-layered (L1 / L2). Diplontic selection
  (Klekowski 1988, already filled) can purge a layer.
  Leaf-DNA "triallelic" SSRs are not proof of three
  layers. Recessives in L1 hide from L2 (gametes).
Modern data / statistic: genotypes of layer-split
  regenerants of a chimeric cultivar, and layer-
  restriction of clone-private mutations after a
  method-fair L1 vs L2 census.
Lead test: Franks et al. 2002 Theor Appl Genet
  104:192-199 (Pinot Meunier L1/L2 split). Genome-
  wide companions: Vondras 2019 / Roach 2018 /
  Carrier 2012.
What would falsify it: if layer-split regenerants of
  a chimeric cultivar are genetically identical, or
  if clone-private mutations are not layer-restricted
  after a method-fair L1 vs L2 census, the periclinal-
  chimera claim dies for that cultivar. Do not treat
  a mixed-leaf SSR profile as the theory.
What we will not claim: that Vitis has three Datura
  layers. That a triallelic leaf SSR proves three
  layers. That this note replaces diplontic selection
  (Klekowski is meristem competition; this is layer
  structure).
```

---

## Reinforcement

```
Theory: Reinforcement of reproductive isolation
Original paper (year): Dobzhansky T. 1940. Speciation
  as a stage in evolutionary divergence. The American
  Naturalist 74(753):312-321. DOI 10.1086/280899.
  Isolating mechanisms develop along geographic
  boundaries after adaptive complexes have formed,
  because hybridization is maladaptive.
  (Dobzhansky 1937 book is the BDM source, already
  filled. This 1940 paper is the reinforcement
  argument, not that book. Wave 2 dropped a 1936
  year; the journal page is 1 July 1940, pages
  312-321.)
One-sentence prediction: Where hybrids are unfit,
  selection completes premating isolation in
  sympatry more than in allopatry.
Assumptions: secondary contact with some gene flow;
  hybrids less fit than parentals; the trait under
  test is premating isolation, not a one-locus
  incompatibility.
Which fail here: a nursery hybrid is not secondary
  contact. Cultivar relatedness fakes isolation.
  Humans move both species. BDM (already filled)
  is hybrid inviability genetics, not reinforcement.
Modern data / statistic: premating isolation
  (flowering time, pollen success, mate choice) in
  sympatric versus allopatric vinifera x riparia /
  rupestris / amurensis or sylvestris contacts.
Caution dataset (not a proof of Dobzhansky 1940):
  Dong et al. 2023 Science
  (DOI 10.1126/science.add8655) reports Syl-W gene
  flow into cultivated groups. Gene flow is the
  opposite of completed reinforcement; use as
  CAUTION, not as a reinforcement map. Do not invent
  a grape hybrid / prezygotic-isolation paper.
What would falsify it: premating isolation is not
  stronger in sympatry than in allopatry, OR hybrid
  inviability maps to a single locus with no
  premating increment.
What we will not claim: that Dong 2023 proved
  reinforcement. That this note replaces BDM
  (Dobzhansky 1937 book). That a grape
  powdery-mildew NLR paper exists here.
```

---

## Two-fold cost of sex

```
Theory: Two-fold cost of sex (cost of males)
Original paper (year): Maynard Smith J. 1978. The
  Evolution of Sex. Cambridge University Press.
  242 pp. ISBN 052121887X. Book. Sexual females
  invest about half their offspring in sons; an
  asexual female that makes only daughters doubles
  in frequency when rare if all else is equal.
  (Kondrashov 1988 is a different, already-dropped
  cost-of-males / deterministic-mutation paper.
  Do not substitute it here.)
One-sentence prediction: An asexual mutant that
  produces only daughters replaces a dioecious
  sexual population in a few tens of generations
  unless a short-term benefit of sex counters the
  two-fold cost.
Assumptions: separate sexes and an equal sex
  ratio; the asexual is a female that skips sons;
  all-else-equal fecundity and survival; the
  comparison is sexual versus asexual reproduction,
  not cutting versus seed.
Which fail here: this does not map onto grafted
  clones. A grafted vine is a cutting of an
  existing genotype, not an asexual female
  replacing sexuals via daughters. Cultivated
  grape is mostly hermaphrodite, not dioecious
  with a cost of sons. Nursery propagation is not
  Maynard Smith's experiment.
Modern data / statistic: none that tests the
  two-fold cost in grape. Clone versus seedling
  yield is not a cost-of-males contrast.
What would falsify it: not applicable as a grape
  test. The note is filled as "does not map onto
  grafted clones" rather than as an invented
  asexual-female invasion.
What we will not claim: that grape clones
  demonstrate the two-fold cost. That Kondrashov
  1988 is this paper. That hermaphroditism is a
  test of the cost of males (that is Baker, already
  filled).
```


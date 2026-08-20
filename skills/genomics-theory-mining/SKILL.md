---
name: genomics-theory-mining
description: >
  Dig up a classic genomics or population-genetic theory and test it
  against modern data. Use when the user wants old-theory mining,
  forgotten models, Muller ratchet, background selection, Meselson,
  BDM, DDC, Baker, isolation by distance, gene balance, nearly-neutral,
  hitchhiking, Hill-Robertson, Ohno WGD, Kingman coalescent,
  infinite-alleles, molecular clock, McDonald-Kreitman, Tajima D,
  genetic draft, introgression, Haldane, stepping-stone,
  island model, clonal interference, allele surfing, genome shock,
  allopolyploidy, drift-barrier, gBGC, soft sweep, chimera,
  reinforcement, two-fold cost of sex, Haldane cost, inbreeding depression, infinitesimal, genetic assimilation,
  C-value, concerted evolution, birth-and-death, metapopulation,
  breakage-fusion-bridge, fractionation, Ewens, shifting balance, Fisher geometric, mutation-selection balance,
  molecular drive, Holliday conversion, quasispecies, serial founder,
  Lande response, endosymbiosis, Vavilov, Price equation, Hamilton, Nei distance, Weir-Cockerham FST,
  Orr adaptation, Y degeneration, Mayr BSC, HKA, or a revival paper that
  is not a methods benchmark.
---

# genomics-theory-mining

The paper is the old math plus a new test, not a review with extra adjectives.
Find the original, list the assumptions, then say which modern data can break them.
Filled notes live in `theories.md` (thirty-eight notes: eight first wave, nine second wave, nine third wave, twelve fourth wave). One theory per job.

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
| Coalescent | Kingman 1982 Stoch Proc Appl 13:235-248 | Sample genealogies are binary n-coalescent trees | Clones and pedigrees are not a random haploid sample | Clone / pedigree samples still look Kingman after relatedness is scored |
| Infinite-alleles | Kimura and Crow 1964 Genetics 49:725-738 | Each mutation is a new allele; IBS is IBD | Chips are biallelic and recurrent; clones fake IBS | IBS on Vitis chips / WGS behaves as infinite-alleles after clone filter |
| Molecular clock | Zuckerkandl and Pauling 1962 Horizons ch. p.189; 1965 Evolving Genes and Proteins 97-166 | Divergence accumulates linearly on a germline clock | Somatic clone clock != sexual clock | Clone clock equals wild sylvestris / germline clock on matched sites (Vondras / Roach vs Dong wilds) |
| McDonald-Kreitman | McDonald and Kreitman 1991 Nature 351:652-654 | Dn/Ds equals Pn/Ps under neutrality | Clone-private SNPs are not substitutions | After clone filter, grape MK does not reject neutrality at domestication loci |
| Tajima D | Tajima 1989 Genetics 123:585-595 | pi equals theta_W under neutrality | Cultivar relatedness fakes negative D | Strongly negative D in cultivar panels vanishes after clone + IBD filter |
| Mutation accumulation | Mukai 1964 Genetics 50:1-19; Lovell 2017 plant comparator | Sheltered genomes accumulate deleterious load | Diplontic selection and chimeras are not a Mukai cage | Clone-private load not deleterious-enriched after diplontic / chimera correction |
| Genetic draft | Gillespie 2000 Genetics 155:909-919 | Recurrent sweeps add drift-like noise at linked sites | Chip skeleton is not a map; clone IBD fakes draft | Linked diversity explained by recombination / BGS, not recurrent sweeps |
| Introgression / hybrid swarm | Anderson 1949 Introgressive Hybridization (book) | Backcross tracts are geographically clinal | Cultivar relatedness fakes tracts | Putative tracts vanish after IBD / clone filters or are not clinal (Dong 2023 Syl-W into CG3-CG6 is CAUTION) |
| Haldane's rule | Haldane 1922 J Genet 12:101-109 | The rare / sterile hybrid sex is the heterogametic sex | Grape is not XX/XY; sex is an SDR | Does not map onto Vitis SDR; do not invent a heterogametic sterility test |
| Stepping-stone | Kimura and Weiss 1964 Genetics 49:561-576 | Correlation declines with steps, not Euclidean distance | Cultivar PCA; human / river jumps | Dong 2023 wilds: neighbor-corridor correlation not higher than Euclidean |
| Island model | Wright 1931 Genetics 16:97-159 (1943 named it) | FST = f(Nem); no distance decay | Vineyard is not an island | Dong 2023 wilds: FST not independent of distance |
| Clonal interference | Gerrish and Lenski 1998 Genetica 102:127-144 | Competing asexual beneficials exclude the weaker | Nursery cuttings are not a chemostat | Vondras 2019 / Roach 2018 / Carrier 2012: clone-private sports not mutually exclusive |
| Allele surfing | Edmonds, Lillie and Cavalli-Sforza 2004 PNAS 101:975-979 | Front mutations reach high frequency by founder repeats | Dual domestication; human transport | Dong 2023: edge alleles not in excess of core after clone + IBD filters |
| Genome shock | McClintock 1984 Science 226:792-801 | Unprepared challenge restructures the genome | Constitutive somatic TE clock is not a shock | Carrier 2012 / Vondras 2019: TE / SV not clustered on shock nodes vs per-year clock |
| Allopolyploidy / secondary polyploidy | Stebbins 1947 Adv Genet 1:403-429 | Allo / segmental allo / palaeo-polyploid types leave distinct pairing and retention | Vitis is palaeo-hexaploid, not recent allo | Jaillon 2007: three ancestral genomes, not a recent allo pair; Zhou 2019 SVs change dose without WGD |
| Drift-barrier | Lynch 2011 Genome Biol Evol 3:1107-1118 | Per-site mu falls until antimutators are lost to drift | Cultivar panel is not Ne; somatic != germline mu | Dong 2023: cultivar mu (not load) not higher than wild after clone filter; no locked grape mu paper |
| GC-biased gene conversion | Galtier, Piganeau, Mouchiroud and Duret 2001 Genetics 159:907-911 | GC and W-to-S rise where recombination is high | No meiosis in cuttings; chip is not a map | Dong 2023 on a real Vitis map: GC / W-to-S not higher in high-r bins after CpG control |
| Soft sweep | Hermisson and Pennings 2005 Genetics 169:2335-2352 | Standing / recurrent copies leave multiple haplotypes and a shallow dip | Pedigree IBD fakes a hard sweep | Dong 2023 color / sex / flavor: single star phylogeny kills soft; H1/H2 standing sex haplotypes are the standing-variation test |
| Chimera / tunica-corpus | Satina, Blakeslee and Avery 1940 Am J Bot 27:895-905 | Layered meristem; periclinal chimera is stable and separable | Vitis is L1/L2, not three Datura layers | Franks 2002 Pinot Meunier L1/L2 split; Vondras / Roach / Carrier as genome-wide layer-census companions |
| Reinforcement | Dobzhansky 1940 Am Nat 74:312-321 (paper; 1937 book is BDM) | Premating isolation completes in sympatry where hybrids are unfit | Nursery hybrid is not secondary contact | Premating isolation not stronger in sympatry, or inviability is one-locus (Dong 2023 Syl-W gene flow is CAUTION) |
| Two-fold cost of sex | Maynard Smith 1978 The Evolution of Sex (book) | Asexual females replace sexuals via daughters | Grafted cuttings are not asexual females | Does not map onto grafted clones; do not invent a cost-of-males test |
| Haldane cost of selection | Haldane 1957 J Genet 55:511-524 | Allelic substitution costs ~10-30 generation-equivalents of selective death | Grafted clones are not a substituting sexual population | Does not map onto grafted clones; do not invent a grape cost-of-selection paper |
| Inbreeding depression | Darwin 1876 Cross and Self Fertilisation (book) | Selfed / inbred progeny are less vigorous than crossed progeny | Standing clone heterozygosity is not a self-vs-cross test | Roach 2018 ancestral inbreeding is CAUTION; selfed seedlings not less fit after clone filter |
| Infinitesimal / polygenic | Fisher 1918 Trans R Soc Edinb 52:399-433 (volume imprint 1919) | A metric trait is many Mendelian loci of small effect | Color / sex / flavor are large-effect loci; clones are not a sexual pedigree | Dong 2023 color / sex / flavor peaks are few large-effect loci, not an infinitesimal trait |
| Genetic assimilation | Waddington 1953 Evolution 7:118-126 | An induced phenotype becomes constitutive after selection | Cuttings skip the multi-generation sexual selection | Does not map onto grafted clones; do not invent a grape heat-shock assimilation paper |
| C-value / junk DNA | Ohno 1972 Brookhaven Symp Biol 23:366-370 | Most DNA is failed-duplication debris, not gene number | Scoring only genes hides repeats / TE | Jaillon 2007 genome size explained by gene number, not junk / TE (Carrier 2012 TE class) |
| Concerted evolution | Zimmer et al. 1980 PNAS 77:2158-2162 | Family members are more alike within species than to orthologs | Tandem NLRs are not rDNA; clones fake identity | Tandem copies more like other-Vitis orthologs than paralogs (birth-and-death alternative) |
| Birth-and-death gene family | Nei, Gu and Sitnikova 1997 PNAS 94:7799-7806 | Duplicates persist or die; members need not homogenize | Tandem NLRs are not MHC; palaeo-ohnologs are not tandem | Tandem NLR / disease-gene copies form one homogenized clade, not births plus pseudogenes |
| Metapopulation | Levins 1969 Bull Entomol Soc Am 15:237-240 | Occupancy is a colonization-extinction balance across patches | A vineyard is not a patch; cultivars are not demes | Dong 2023 wild patches: occupancy not a colonization-extinction balance after clone filter |
| Breakage-fusion-bridge | McClintock 1941 Genetics 26:234-282 | Broken ends fuse, bridge, and re-break; rearrangements cycle | SNP-only census hides BFB; distinct from 1950 TE and 1984 shock | Carbonell-Bejerano 2017 rearrangements not BFB-class; clone SVs are SNP-like (Zhou 2019) |
| Fractionation / diploidization | Thomas, Pedersen and Freeling 2006 Genome Res 16:934-946 | After WGD, one homeolog loses genes preferentially; connected genes stay | Vitis is palaeo-hexaploid, not recent tetraploid; SVs change dose without WGD | Jaillon 2007: no biased homeolog loss; TF / signaling not the retained class vs tandem NLRs |
| Ewens sampling formula | Ewens 1972 Theor Popul Biol 3:87-112 | Neutral allele-count configurations follow the sampling formula | Clones fake allele identity; chips are biallelic | Dong 2023 wilds: configuration not Ewens after clone + IBD filters |
| Shifting balance | Wright 1932 Proc 6th Int Congr Genet 1:356-366 | Subdivided races find higher peaks by drift then intergroup export | A vineyard is not a Wright race; cuttings skip the trial | Dong 2023 wild patches: no local nonadaptive peak-shift then export after clone filter |
| Fisher's geometric model | Fisher 1930 Genetical Theory ch. II pp. 38-41 | Large random mutations almost never improve; small ones might | Color / sex / flavor are large-effect; clones are not a walk | Dong 2023 color / sex / flavor peaks are few large-effect loci, not a small-step walk |
| Mutation-selection balance | Haldane 1927 Math Proc Camb Phil Soc 23:838-844 | A deleterious allele sits at a mutation-selection equilibrium | Grafted clones are not a sexual equilibrium; clone-private SNPs are not q | Wild coding load not at mutation-selection equilibrium after clone filter |
| Molecular drive | Dover 1982 Nature 299:111-117 | Genomic turnover cohesively replaces a family in genome and population | Tandem NLRs are not rDNA; clones fake cohesion | Tandem copies not cohesively replacing in the population (Zimmer or birth-and-death instead) |
| Gene conversion | Holliday 1964 Genet Res 5:282-304 | Hybrid-DNA mismatch repair converts one allele to the other | Cuttings skip meiosis; distinct from gBGC | No conversion tracts after clone filter; W-to-S bias is the gBGC job |
| Quasispecies | Eigen 1971 Naturwissenschaften 58:465-523 | A mutant cloud is maintained around a master sequence | RNA virus / prebiotic kinetics, not a grafted clone | Does not map onto grafted clones; do not invent a grape quasispecies paper |
| Serial founder | Ramachandran et al. 2005 PNAS 102:15942-15947 | Heterozygosity falls with distance from a single origin | Dual domestication; human transport | Dong 2023: diversity not a single-origin decline after clone + IBD filters |
| Multivariate response / breeder's equation | Lande 1979 Evolution 33:402-416 | Mean change is G beta (covariance times selection gradient) | Clones are not a sexual pedigree; few large-effect loci | Dong 2023 color / sex / flavor: not a G-matrix response (few large-effect loci) |
| Endosymbiosis / organelle origin | Sagan 1967 J Theor Biol 14:225-274 | Mitochondria and plastids were free-living prokaryotes | Eukaryogenesis is not a grape-clone experiment | Does not map onto grafted clones; do not invent a grape organelle-origin paper |
| Vavilov centers of origin | Vavilov 1932 Proc 6th Int Congr Genet 1:331-342 | Cultivated plants originate in a few geographically small diversity centres | Dual domestication; a vineyard is not a centre | Dong 2023: grape diversity not a single Vavilov-centre decline after clone + IBD filters |
| Price equation | Price 1970 Nature 227:520-521 | Mean change equals covariance of a character with relative fitness (plus transmission) | Cuttings are not a sexual generation; few large-effect loci | Dong 2023 color / sex / flavor: not a Price covariance partition (few large-effect loci) |
| Kin selection / inclusive fitness | Hamilton 1964 J Theor Biol 7:1-16 | Altruism spreads when inclusive fitness rises (relatedness times benefit) | Grafted clones are not social interactors | Does not map onto grafted clones; do not invent a grape kin-selection paper |
| Nei genetic distance | Nei 1972 Am Nat 106:283-292 | Distance from gene identity accumulates with divergence under isolation | Clones fake identity; dual domestication is not one split | Dong 2023 wilds: D not a single-split clock after clone + IBD filters |
| Weir-Cockerham FST | Weir and Cockerham 1984 Evolution 38:1358-1370 | FST is a moment estimator from allele-frequency variance, not Wright's island formula as data | A vineyard is not a deme; clones fake FST | Dong 2023 wilds: WC FST not independent of distance after clone filter (island dies) |
| Orr exponential factors | Orr 1998 Evolution 52:935-949 | Factors fixed on a walk to an optimum are approximately exponential in size | Color / sex / flavor are few large-effect; clones are not a walk | Dong 2023 color / sex / flavor peaks are a few large-effect loci, not an exponential walk |
| Y-chromosome degeneration | Charlesworth 1978 PNAS 75:5618-5622 | A non-recombining Y ratchets load and becomes inert; X dosage rises | Vitis SDR is young, not an XX/XY Y | Dong 2023 chr-2 SDR: little Y-like degeneration / recombination still present after clone filter |
| Biological species concept | Mayr 1942 Systematics and the Origin of Species (book) | Species are interbreeding populations isolated from other such groups | Cultivar x cultivar is not a species test; gene flow is caution | Dong 2023 Syl-W gene flow: sylvestris and vinifera are not isolated biological species |
| HKA test | Hudson, Kreitman and Aguade 1987 Genetics 116:153-159 | High-divergence regions are high-polymorphism regions under neutrality | Clone IBD fakes polymorphism; chips are not loci | After clone + IBD filters, polymorphism does not scale with divergence (MK / Tajima remain other jobs) |

Sixty-seven filled notes (eight first wave, nine second wave, nine third wave, twelve fourth wave, ten fifth wave, ten sixth wave, nine seventh wave). Long form in `theories.md`. One theory per job.

Kondrashov 1988 (cost of males) is on the door list but was not filled: it does not map onto grafted clones.
Muller 1942 was not locked on a publisher page and is not cited for BDM.
Flor 1971 is a review and was not used as a theory source.
Flor 1955 Phytopathology / Flor 1956 Adv Genet were not opened on a publisher page this wave and are not cited.
Haldane 1922 is filled as "does not map onto Vitis SDR"; grape is not XX/XY.

Reinforcement (Dobzhansky 1940 Am Nat 74:312-321) is filled as a
paper, distinct from the 1937 BDM book. Dong 2023 Syl-W gene flow
is CAUTION, not a reinforcement map.
Two-fold cost of sex (Maynard Smith 1978 book) is filled as "does
not map onto grafted clones"; Kondrashov 1988 is not this paper.
Overdominance / heterozygote advantage is on the door list but was
not filled: term vs theory split (Hull 1946 Agron J vs Dobzhansky
1950 Genetics); standing heterozygosity in clones is not a test of
balancing selection; no locked grape inversion / overdominant QTL
paper.
Red Queen (Van Valen 1973 Evol Theory 1:1-30) is on the door list
but was not filled: the original claim is a constant taxonomic
extinction rate; the host-pathogen reading is later; no grape
pathogen-coevolution paper is locked.
Centromere drive (Henikoff 2001 Science review; Henikoff and Malik
2002 Nature N&V) is on the door list but was not filled: named
papers are a review and a one-page N&V; the claim requires female
meiosis; grafted clones have no meiosis between cuttings; no grape
centromere / CenH3 paper is locked.


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
- Kingman coalescent assumes a random sample from a large haploid population. Clones and pedigrees are not that sample.
- Clone-private SNPs are not McDonald-Kreitman substitutions.
- Strongly negative Tajima's D in a cultivar panel is relatedness until clones and IBD are removed.
- The somatic clone clock is not the Zuckerkandl-Pauling germline clock.
- Genetic draft is recurrent linked substitutions, not one hitchhiking event and not background selection.
- Haldane's rule does not map onto the Vitis sex-determination region.

- Stepping-stone is neighbor-only steps; a cultivar PCA is not a lattice.
- The island model has no distance; a nonzero IBD slope in wild sylvestris kills it.
- Clonal interference needs two competing beneficials in one finite N; a single sport is not CI.
- Allele surfing needs a single expanding front; dual domestication and human transport break it.
- Genome shock is an unprepared challenge, not a constitutive somatic TE clock.
- Vitis is palaeo-hexaploid, not a recent allopolyploid; SVs change dose without WGD.
- Drift-barrier is evolution of mu, not Ohta load; no locked grape wild-vs-cultivar mu paper.
- gBGC is meiotic; a chip skeleton is not a recombination map (same map rule as BGS / HR).
- Soft sweep is multiple surviving haplotypes; pedigree IBD fakes a hard sweep.
- Vitis SAM is L1/L2, not three Datura layers; Franks 2002 Pinot Meunier is the grape test.
- Reinforcement is premating isolation after secondary contact, not BDM inviability and not Dong 2023 gene flow.
- The two-fold cost of sex does not map onto grafted clones. Hermaphroditism is the Baker test, not a cost of males.

- Haldane 1957 cost does not map onto grafted clones as a substituting sexual population.
- Darwin 1876 is a self-versus-cross progeny test; standing clone heterozygosity is not that test.
- Fisher 1918 infinitesimal dies where Dong 2023 color / sex / flavor are few large-effect loci.
- Waddington 1953 assimilation needs many sexual generations; cuttings skip them.
- Ohno 1972 junk DNA is C-value versus gene number, not selfish-DNA persistence (1980).
- Zimmer 1980 concerted evolution is within-species homogenization; Nei 1997 is the opposite job.
- Levins 1969 is patch occupancy; a vineyard is not a patch (island / stepping-stone / IBD remain separate).
- McClintock 1941 BFB is broken-end cycling, not 1950 TE and not 1984 shock.
- Thomas, Pedersen and Freeling 2006 fractionation is biased homeolog loss after WGD, not Ohno dosage and not Stebbins polyploid type.

- Ewens 1972 is the sampling configuration under infinite-alleles; Kimura and Crow 1964 is the allele model (already filled). Clone IBS is not the sample.
- Wright 1932 shifting balance is peak-shift by subdivided trial-and-error; Wright 1931 island and Wright 1943 IBD remain separate jobs. A vineyard is not a Wright race.
- Fisher 1930 geometric is random mutations in n-space (pages 38-41); Fisher 1918 infinitesimal is already filled.
- Haldane 1927 mutation-selection balance is equilibrium load; Haldane 1957 cost and Mukai 1964 MA are different jobs. Clone-private SNPs are not q = mu/s.
- Dover 1982 molecular drive is cohesive replacement through genome and population; Zimmer 1980 concerted is the within-species pattern (already filled).
- Holliday 1964 gene conversion is hybrid-DNA mismatch repair; Galtier 2001 gBGC is the GC-biased population force (already filled). Cuttings skip meiosis.
- Eigen 1971 quasispecies does not map onto grafted clones. A chimera is not a mutant cloud.
- Ramachandran 2005 serial founder is heterozygosity declining from one origin; dual domestication, IBD, and allele surfing are different jobs.
- Lande 1979 is G beta; Dong 2023 color / sex / flavor are few large-effect loci, not a G-matrix response. Not Fisher 1918 and not Fisher 1930 geometric.
- Sagan 1967 organelle origin does not map onto grafted clones. Lynch 1996 remains the organelle-ratchet note. Timmis 2004 is a review.

- Vavilov 1932 is seven geographically small crop centres (ESP facsimile pp. 331-342). Homologous series is named there as Vavilov 1922 J Genet; that paper was not opened. Dual domestication is not one centre. Serial founder remains Ramachandran 2005.
- Price 1970 is selection as covariance; Lande 1979 remains G beta. Cuttings are not a generation. Dong 2023 color / sex / flavor are few large-effect loci.
- Hamilton 1964 inclusive fitness does not map onto grafted clones. A chimera is not kin selection. Trivers 1974 was not filled.
- Nei 1972 is between-population distance from gene identity; Wright 1931 island, Wright 1943 IBD, and Nei 1997 birth-and-death remain other jobs. Clone IBS is not identity.
- Weir and Cockerham 1984 is the FST estimator; Wright 1931 remains the island parameter. A vineyard is not a deme.
- Orr 1998 is the exponential distribution of factors fixed on a walk; Fisher 1930 geometric is the chance a random mutation improves (already filled). Orr 2005 is a review.
- Charlesworth 1978 is Y degeneration by ratchet plus dosage compensation. Haldane 1922 remains does-not-map for heterogametic sterility. Charlesworth 1991 Science is a review. Dong 2023 chr-2 SDR is the young-SDR contrast.
- Mayr 1942 is the biological species book; Dobzhansky 1937 remains BDM and 1940 remains reinforcement. Founder effect (often 1954) was not opened.
- HKA 1987 is polymorphism-divergence scaling; MK 1991 and Tajima 1989 remain other jobs. Hudson 1990 survey and Hudson 2002 ms were not used as sources.

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
- Kingman 1982: https://doi.org/10.1016/0304-4149(82)90011-4
- Kimura and Crow 1964: https://doi.org/10.1093/genetics/49.4.725 (PMID 14156929 PMC1210609)
- Zuckerkandl and Pauling 1965 chapter: https://doi.org/10.1016/B978-1-4832-2734-4.50017-6
- McDonald and Kreitman 1991: https://doi.org/10.1038/351652a0 (PMID 1904993)
- Tajima 1989: https://doi.org/10.1093/genetics/123.3.585 (PMID 2513255 PMC1203831)
- Mukai 1964: https://doi.org/10.1093/genetics/50.1.1 (PMID 14191352 PMC1210633)
- Gillespie 2000: https://doi.org/10.1093/genetics/155.2.909 (PMID 10835409 PMC1461093)
- Haldane 1922: https://doi.org/10.1007/BF02983075 (IAS: https://www.ias.ac.in/article/fulltext/jgen/012/02/0101-0109)

- Kimura and Weiss 1964: https://doi.org/10.1093/genetics/49.4.561
- Wright 1931: https://doi.org/10.1093/genetics/16.2.97
- Gerrish and Lenski 1998: https://doi.org/10.1023/A:1017067816551
- Edmonds et al. 2004: https://doi.org/10.1073/pnas.0308064100
- Klopfstein et al. 2006 (name only): https://doi.org/10.1093/molbev/msj057
- McClintock 1984: https://doi.org/10.1126/science.15739260
- Stebbins 1947: https://doi.org/10.1016/S0065-2660(08)60490-3
- Lynch 2011: https://doi.org/10.1093/gbe/evr066
- Sung et al. 2012 (test, not source): https://doi.org/10.1073/pnas.1216223109
- Galtier et al. 2001: https://doi.org/10.1093/genetics/159.2.907
- Hermisson and Pennings 2005: https://doi.org/10.1534/genetics.104.036947
- Satina, Blakeslee and Avery 1940: https://doi.org/10.1002/j.1537-2197.1940.tb13952.x
- Franks et al. 2002: https://doi.org/10.1007/s001220100683
- Dobzhansky 1940: https://doi.org/10.1086/280899
- Maynard Smith 1978 book: ISBN 052121887X (Cambridge University Press)

- Haldane 1957: https://doi.org/10.1007/BF02984069 (IAS: https://www.ias.ac.in/article/fulltext/jgen/055/03/0511-0524)
- Darwin 1876 book: https://darwin-online.org.uk/content/record?itemID=F1249
- Fisher 1918: https://doi.org/10.1017/S0080456800012163
- Waddington 1953: JSTOR 2405747 (Evolution 7:118-126)
- Ohno 1972: PMID 5065367 (EuropePMC MED 5065367)
- Zimmer et al. 1980: https://doi.org/10.1073/pnas.77.4.2158 (PMC348671)
- Nei, Gu and Sitnikova 1997: https://doi.org/10.1073/pnas.94.15.7799 (PMC33709)
- Levins 1969: https://doi.org/10.1093/besa/15.3.237
- McClintock 1941: https://doi.org/10.1093/genetics/26.2.234 (PMC1209127)
- Thomas, Pedersen and Freeling 2006: https://doi.org/10.1101/gr.4708406 (PMC1484460)

- Ewens 1972: https://doi.org/10.1016/0040-5809(72)90035-4 (EuropePMC MED 4667078)
- Wright 1932: http://www.esp.org/books/6th-congress/facsimile/contents/6th-cong-p356-wright.pdf (TOC: http://www.esp.org/books/6th-congress/facsimile/index.html)
- Fisher 1930 book, geometric pages 38-41: https://archive.org/details/geneticaltheoryo00fishuoft
- Haldane 1927: https://doi.org/10.1017/S0305004100015644
- Dover 1982: https://doi.org/10.1038/299111a0 (EuropePMC MED 7110332)
- Holliday 1964: https://doi.org/10.1017/S0016672300001233
- Eigen 1971: https://doi.org/10.1007/BF00623322
- Ramachandran et al. 2005: https://doi.org/10.1073/pnas.0507611102 (PMC1276087; EuropePMC MED 16243969)
- Lande 1979: https://doi.org/10.1111/j.1558-5646.1979.tb04694.x (EuropePMC MED 28568194)
- Sagan 1967: https://doi.org/10.1016/0022-5193(67)90079-3 (EuropePMC MED 11541392)

- Vavilov 1932: http://www.esp.org/books/6th-congress/facsimile/contents/6th-cong-p331-vavilov.pdf (TOC: http://www.esp.org/books/6th-congress/facsimile/index.html)
- Price 1970: https://doi.org/10.1038/227520a0 (EuropePMC MED 5428476)
- Hamilton 1964: https://doi.org/10.1016/0022-5193(64)90038-4 (EuropePMC MED 5875341)
- Nei 1972: https://doi.org/10.1086/282771 (Crossref work JSON; CiNii crid 1364233269783061504)
- Weir and Cockerham 1984: https://doi.org/10.1111/j.1558-5646.1984.tb05657.x (EuropePMC MED 28563791)
- Orr 1998: https://doi.org/10.1111/j.1558-5646.1998.tb01823.x (EuropePMC MED 28565213)
- Charlesworth 1978: https://doi.org/10.1073/pnas.75.11.5618 (PMC393018; EuropePMC MED 281711)
- Mayr 1942 book: https://books.google.com/books/about/Systematics_and_the_Origin_of_Species_fr.html?id=XxMgAQAAMAAJ
- Hudson, Kreitman and Aguade 1987: https://doi.org/10.1093/genetics/116.1.153 (PMC1203113; EuropePMC MED 3110004)

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
- Do not treat clone-private SNPs as McDonald-Kreitman substitutions.
- Do not write a clone tree in years-since-planting as the molecular clock.
- Do not invent a heterogametic sterility pattern for Vitis. Haldane does not map onto the SDR.
- Do not cite Flor 1971. Flor 1955 / 1956 originals were not locked this wave.
- Do not invent a grape powdery-mildew NLR paper.

- Do not cite Lynch 2010 Trends Genet as the drift-barrier source (review).
- Do not invent a grape mutation-rate paper or a grape recombination-map paper.
- Do not write VviAGL11 as the soft-sweep sex-locus test (SDR H1/H2 is).
- Do not treat a mixed-leaf SSR profile as tunica-corpus proof.
- Do not fill overdominance, Red Queen, or centromere drive.
- Do not invent a grape hybrid / prezygotic-isolation paper for reinforcement.
- Do not invent a cost-of-males test in grafted clones. Two-fold cost does not map.
- Do not cite McClintock 1984 as the 1950 TE note (different job).
- Do not cite Stebbins 1940 or 1950 as the 1947 polyploid-type source.

- Do not cite Wang and Bradburd 2014 as an IBE original (review).
- Do not fill adaptive introgression as distinct from Anderson 1949.
- Do not cite Nei and Rooney 2005 or Freeling 2009 as theory sources (reviews).
- Do not cite Dover 1982 as the concerted-evolution original (Zimmer 1980 is).
- Do not cite McClintock 1941 as the 1950 TE note or the 1984 shock note.
- Do not invent a grape cost-of-selection, assimilation, rDNA, NLR-phylogeny, or patch-turnover paper.
- Do not treat standing clone heterozygosity as Darwin 1876 inbreeding depression.
- Do not write Fisher 1918 as the 1930 geometric model.

Heterosis / hybrid vigor is on the candidate list but was not filled: no single named original distinct from filled Darwin 1876 inbreeding depression and the already-dropped overdominance split (Hull 1946 vs Dobzhansky 1950); Shull 1908 / 1914 pages were not opened; standing clone heterozygosity is not hybrid vigor.
Endosymbiotic gene transfer is on the candidate list but was not filled as a separate note: Timmis, Ayliffe, Huang and Martin 2004 Nat Rev Genet is a review; a Martin original was not opened; Sagan 1967 is organelle origin, not gene transfer.
Isolation by colonization is on the candidate list but was not filled as a second named original: Ramachandran et al. 2005 is the one serial-founder lock.
Soft vs hard selection (Wallace 1968 chapter / Wallace 1975 Evolution 29:465-473 / Christiansen 1975 Am Nat 109:11-16) is on the candidate list but was not filled: Wallace 1975 Evolution HTML was Cloudflare / timeout; Christiansen 1975 Am Nat HTML was not opened; the 1968 Lewontin-volume chapter was not opened.
Outcrossing depression / Bateson is on the candidate list but was not filled: Bateson 1909 was already dropped for the two-locus incompatibility claim; no distinct outbreeding-depression original was opened.
Phylogeography Avise is on the candidate list but was not filled: Avise et al. 1987 Annu Rev Ecol Syst is a review.
Vavilov centers / domestication syndrome is on the candidate list but was not filled: ESP TOC lists N. I. Vavilov 1932 "The Process of Evolution on Cultivated Plants" at p. 331; that PDF was not opened; Hammer 1984 was not used.

- Do not cite Dover 1982 as the concerted-evolution original (Zimmer 1980 is). This note is drive, a different job.
- Do not cite Timmis et al. 2004 or Nei and Rooney 2005 or Freeling 2009 as theory sources (reviews).
- Do not cite Eigen and Schuster 1977 as the quasispecies source (1971 is).
- Do not cite Lush 1937 as opened (it was not); Lande 1979 is the locked multivariate paper.
- Do not write Fisher 1930 geometric as Fisher 1918 infinitesimal.
- Do not write Wright 1932 as Wright 1931 island or Wright 1943 IBD.
- Do not write Holliday 1964 as Galtier 2001 gBGC.
- Do not write Sagan 1967 as Lynch 1996 organelle ratchet, or as EGT.
- Do not invent a grape Ewens, peak-shift, FGM, mutation-load-equilibrium, rDNA-drive, conversion-tract, quasispecies, serial-founder, G-matrix, or organelle-origin paper.
- Do not fill heterosis, EGT, isolation-by-colonization as a second original, soft vs hard selection, outcrossing depression, Avise phylogeography, or Vavilov / domestication syndrome this wave.

Heterosis / hybrid vigor is on the candidate list but was not filled: no single named original distinct from filled Darwin 1876 and dropped overdominance (Hull 1946 vs Dobzhansky 1950); Shull 1908 / 1914 pages were not opened; standing clone heterozygosity is not hybrid vigor.
Soft vs hard selection (Wallace 1968 chapter / Wallace 1975 Evolution 29:465-473 DOI 10.1111/j.1558-5646.1975.tb00836.x PMID 28563194 / Christiansen 1975 Am Nat 109:11-16 DOI 10.1086/282970) is on the candidate list but was not filled: Wallace 1975 EuropePMC HTML opened for author+year+venue this wave but carried no abstract or claim text; the 1968 Lewontin-volume chapter was not opened; Christiansen 1975 Chicago HTML was Cloudflare. Do not fill without quoting the hard/soft claim from an opened page.
Phylogeography Avise is on the candidate list but was not filled: Avise et al. 1987 Annu Rev Ecol Syst is a review.
Trivers 1974 parent-offspring conflict is on the candidate list but was not filled: not a genomics job for this skill.
Pritchard JK, Stephens M, Donnelly P. 2000. Inference of population structure using multilocus genotype data. Genetics 155(2):945-959. DOI 10.1093/genetics/155.2.945 PMID 10835412 PMC1461096. EuropePMC HTML opened (abstract names a model-based clustering method and software). DROP: method, not a named theory; this skill is not a methods bake-off.
Li and Durbin 2011 PSMC is on the candidate list but was not filled: too new, and a method, not a named original theory.
Lewontin 1974 The Genetic Basis of Evolutionary Change (Columbia) is on the candidate list but was not filled: book pages were not opened; the paradox-of-variation job would overlap filled Kimura 1968 / Lewontin-Hubby territory without a locked 1966 page.
Kimura 1983 The Neutral Theory of Molecular Evolution (book) was skipped: Kimura 1968 is already filled.
Crow and Kimura 1970 An Introduction to Population Genetics Theory was skipped: intro book, not a named original.
Gillespie 1991 The Causes of Molecular Evolution was skipped: Gillespie 2000 draft is already filled.
Charlesworth 1994 evolution of sex chromosomes was skipped: no 1994 paper of that title was found; 1991 Science 251:1030-1033 is a review. 1978 PNAS is the filled original.
Hudson 1990 Oxford Surveys coalescent chapter was skipped: survey; not opened. Hudson 2002 Bioinformatics ms was skipped: software method.
Mayr founder effect as a second named original was skipped: 1942 is the BSC lock; the founder-principle paper (often 1954) was not opened. Serial founder remains Ramachandran 2005.

- Do not cite Vavilov 1922 as this paper (homologous series; named in the 1932 facsimile but not opened).
- Do not cite Hammer 1984 as the centres source.
- Do not cite Price 1972 as the Price-equation source (1970 is).
- Do not cite Hamilton 1964 part II as the source (part I is the math).
- Do not cite Orr 2005 Nat Rev Genet as the adaptation source (review; 1998 is).
- Do not cite Charlesworth 1991 Science as the Y-degeneration source (review). Do not invent a 1994 Charlesworth sex-chromosome original.
- Do not write Mayr 1942 as Dobzhansky 1937 BDM or as Ramachandran 2005 serial founder. Do not write it as Mayr 1954 founder (not opened).
- Do not cite Hudson 1990 or Hudson 2002 as the HKA source.
- Do not cite Pritchard 2000 as a theory original (clustering method).
- Do not write Nei 1972 as Nei 1997 birth-and-death, or as Wright 1931 / Weir-Cockerham 1984.
- Do not write Weir-Cockerham 1984 as Wright 1931 island math.
- Do not write Orr 1998 as Fisher 1930 geometric or Fisher 1918 infinitesimal.
- Do not invent a grape Vavilov-centre, Price-equation, kin-selection, Nei-distance, FST-estimator, adaptive-walk, Y-degeneration, biological-species, or HKA paper.

Related: `plant-lit-review`, `vitis-popgen`, `grapevine-adna`, `vitis-pangenome`.

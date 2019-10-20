# Summary of Kaneka

The Kaneka system requires the following two modifications of the standard methods.

First, the PCR must be done with specially designed Forward and Reverse primers that contain an additional sequence and modified bases. The additional sequence of Forward enables binding to a gold nanocolloid, and the additional sequence of the Reverse enables binding to a solid-phased DNA probe, as follows. (Figure 1, Nagai et al. 2015)

![Figure 1 from Nagai et al. 2015](https://ars.els-cdn.com/content/image/1-s2.0-S1568988315300597-gr1.jpg)

Second, the chromatography paper is prepared by printing conjugated DNA oligomers onto it. The bottom part of the chromatography paper holds a DNA oligomer conjugated to a gold nanocolloid. This DNA oligomer can bind to the DNA PCR amplicon, and is picked up by the DNA PCR amplicon as it moves upward. Then, the DNA PCR amplicon, which is now attached to a gold nanocolloid, is captured by the solid-phased DNA probe on a specific region on the chromatography paper. Development buffer allows visualization of the position of gold nanocolloid. (Figure 2, Nagai et al. 2015)

![Figure 2 from Nagai et al. 2015](https://ars.els-cdn.com/content/image/1-s2.0-S1568988315300597-gr2.jpg)

# Feasability

# Cheaper alternatives

# Finding unique sequences in the target gene (in case of undocumented target)

To design a chromatography chip that is specific to the target gene, it is necessary to select a nucleic acid sequence within the target that is unique, meaning that it does not overlap with irrelevant sequences that may be found in the same environment (for example, human DNA). This is very important, because different living organisms may share very similar genes. To achieve this, a bioinformatics pipeline is needed to analyze known DNA sequences from online databases and pick up unique regions in the target. The pipeline may involve the following steps (this may be subject to change after testing), and the order and parameters will require optimization during development. The parameters may differ slightly depending on the nature of the target.

* Divide the target sequence into many 20 nucleotide-long segments (sliding window: length 20, step 1)
* Align the target sequences to the NCBI nucleotide collection using [BLASTn](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastn&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome)
* Eliminate sequences with matches that are incompatible with PCR (perfect match in 3'-end)
* Map unique regions
* Design PCR primers that bind to unique regions

# 

# References

- Paper-based reactions
  - Green et al. 2014 [Toehold switches: de-novo-designed regulators of gene expression](https://www.sciencedirect.com/science/article/pii/S0092867414012896?via%3Dihub)
  - Pardee et al. 2014 [Paper-based synthetic gene networks](https://www.sciencedirect.com/science/article/pii/S0092867414012914?via%3Dihub)
  - Pardee et al. 2016 [Rapid, Low-Cost Detection of Zika Virus Using
Programmable Biomolecular Components](https://collinslab.mit.edu/files/cell_pardee2.pdf?fbclid=IwAR1eQfex-SAMQJzeTwXLqg701tIcZWE7uV1c8ARLCnmjll4kmgp-6MkMa6I)
- [Kaneka](https://www.kaneka-labtest.com/en/chromato/index.html)
  - Leave a Nest is connected with them.
  - Nagai et al. 2015 [Easy detection of multiple Alexandrium species using DNA chromatography chip](https://sci-hub.tw/10.1016/j.hal.2015.10.014)
  - Sano et al. 2018 [Rapid multiplex nucleic acid amplification test developed using paperchromatography chip and azobenzene-modified oligonucleotides](https://sci-hub.tw/10.1016/j.jbiosc.2018.03.017)
- [Kurabou GeneFields](https://www.kurabo.co.jp/bio/English/product/products.php?M=L&A=P&CID=9)
  - "GeneFields Meat 48" costs JPY73,872 (1 week)

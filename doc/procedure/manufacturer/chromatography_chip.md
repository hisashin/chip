# Summary of Kaneka

The Kaneka system requires the following two modifications of the standard methods.

First, the PCR must be done with specially designed Forward and Reverse primers that contain an additional sequence and modified bases. The additional sequence on the Forward primer enables binding to a gold nanocolloid for color detection, and the additional sequence on the Reverse primer enables binding to a solid-phased DNA probe on a specific location of the chromatography paper, as follows. (**Figure 1**, Nagai et al. 2015)

![Figure 1 from Nagai et al. 2015](https://ars.els-cdn.com/content/image/1-s2.0-S1568988315300597-gr1.jpg)

**Figure 1** from Nagai et al. 2015

Second, the chromatography paper is prepared by printing conjugated DNA oligomers onto it. The bottom part of the chromatography paper holds a DNA oligomer conjugated to a gold nanocolloid. This DNA oligomer can bind to the DNA PCR amplicon, and is picked up by the DNA PCR amplicon as it moves upward. Then, the DNA PCR amplicon, which is now attached to a gold nanocolloid, is captured by the solid-phased DNA probe on a specific region on the chromatography paper. Development buffer allows visualization of the position of gold nanocolloid. (**Figure 2**, Nagai et al. 2015)

![Figure 2 from Nagai et al. 2015](https://ars.els-cdn.com/content/image/1-s2.0-S1568988315300597-gr2.jpg)

**Figure 2** from Nagai et al. 2015

## Advantage(s) of Kaneka

It's possible to test several PCR reactions (currently up to five) per paper strip.

## Disadvantage(s) of Kaneka

High cost of modified DNA oligomers.
Requires spatially controlled printing of DNA onto chromatography paper.

# Summary of paper-based sensor (Pardee et al. 2016)

The efficiency of this entirely paper-based system was demonstrated in the context of Zika virus detection. The presence of the target sequence in the sample triggers the production of an enzyme, the beta-galactosidase LacZ. This enzyme converts a yellow substrate (chlorophenol red-beta-D-galactopyranoside) into a purple product (chlorophenol red), resulting in a visible color change from yellow to purple. The workflow is illustrated in the **Graphical Abstract** of Pardee et al. 2016. They also developed a system to distinguish more precisely between single-nucleotide variants of the target, which is important if there is a need to monitor several versions of the target that are highly similar in terms of sequence.

![Graphical Abstract from Pardee et al. 2016](https://marlin-prod.literatumonline.com/cms/attachment/f796e0ea-f0e1-490f-9746-6ac2898d63d0/fx1.jpg)

**Graphical Abstract** from Pardee et al. 2016

# Advantage(s) of paper-based sensor

No special or expensive chemicals are necessary. Furthermore, LacZ technology has been around for more than 40 years, so there should be no problems in terms of patents. Another advantage is that this technology can be easily applied to both DNA and RNA targets, meaning that the potential future applications are much broader.

# Disadvantage(s) of paper-based sensor

After PCR, the DNA target has to be transcribed to RNA for the color test to work. This adds one additional step.
However, the reaction to produce RNA simply occurs at 37 degrees and does not require thermocycling, so it's very easy to overcome. 

# Feasability and cost

The paper-based sensor is much more promising in terms of feasibility and cost.
In its present form, it does not implement a chromatography step, basically because they are testing one target gene per paper strip, so spatial resolution is not necessary.

Chromatography would enable the detection of multiple targets per paper strip. However, similar to Kaneka, we would probably be limited to about 4-5 targets per strip. I'm not sure what the advantage is, and it probably depends on the application. Unless there is a specific reason or advantage to justify multiplexing, one target per reaction per paper strip is always better in terms of reliability and design cost.

One paper strip containing one dried cell-free based LacZ system can be dipped into the PCR reaction. The PCR product will migrate on the paper strip and cause a change to purple color if the target is present. This is very simple and easy to implement.

# How to produce the paper strip

## Finding unique sequences in the target gene (in case of undocumented target)

To design a chromatography chip that is specific to the target gene, it is necessary to select a nucleic acid sequence within the target that is unique, meaning that it does not overlap with irrelevant sequences that may be found in the same environment (for example, human DNA). This is very important, because different living organisms may share very similar genes. To achieve this, a bioinformatics pipeline is needed to analyze known DNA sequences from online databases and pick up unique regions in the target. The pipeline may involve the following steps (this may be subject to change after testing), and the order and parameters will require optimization during development. The parameters may differ slightly depending on the nature of the target.

* Divide the target sequence into many 20 nucleotide-long segments (sliding window: length 20, step 1)
* Align the target sequences to the NCBI nucleotide collection using [BLASTn](https://blast.ncbi.nlm.nih.gov/Blast.cgi?PROGRAM=blastn&PAGE_TYPE=BlastSearch&LINK_LOC=blasthome)
* Eliminate sequences with matches that are incompatible with PCR (perfect match in 3'-end)
* Map unique regions
* Design PCR primers that bind to unique regions

## Design of the dried cell-free based LacZ system

### Ingredients

Name | Order | Homemade
---- | ----- | --------
Artificial DNA containing target complementary sequence fused to LacZ | yes | yes
T7 RNA polymerase *in vitro* transcription mix | yes | yes
cell-free *in vitro* translation mix based on bacterial ribosomes | yes | yes

## Testing the reaction

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

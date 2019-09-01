# Summary

This project aims to make DNA test easy. As easy as pregnancy test with cheap disposable kits at room temperature.
No fridge, pipette, centrifuge, electrophoresis nor UV illuminator. DNA extractor([ex1](https://www.kaneka-labtest.com/en/pre/dna_version2.html), [ex2](https://www.funakoshi.co.jp/contents/64147)) and DNA chromatography chip([ex1](https://www.kaneka-labtest.com/en/chromato/index.html), [ex2](https://www.kurabo.co.jp/bio/English/product/products.php?M=D&PID=99), [ex3](https://techcrunch.com/2016/05/06/zika-test/)) should be used instead. Thermal cycler is needed at first but we have [NinjaPCR](https://github.com/hisashin/NinjaPCR) and might be removed in future with [such tech](https://www.twistdx.co.uk/en/products/product/twistamp-basic).

Use case examples :
- Food allergy patients (even kids) can test their food by themselves.
- In pandemic, people can pick a blood from finger and test infectious diseases like Zika, by themselves.
- Halal test

Whole Procedure :

1. Manufacturer (we)
 1. Make preservable primer and reverse primer placed in A2, one of two connected PCR tubes (A1+A2)
 1. Make preservable DNA extraction solution and tissue prep solution (B)
 1. Make preservable neutralization solution and reaction mix (C)
 1. Make preservable DNA chromatography chip (D)
  1. Design
  1. Manufacture
 1. Packaging, Inventory management, Sales and Shipping
1. End User
 1. Pick up ~10uL sample without specific tool
 1. Put it into A1
 1. Put B into A1
 1. Place A1+A2 into tube holder of thermal cycler (for example NinjaPCR)
 1. Prepare
  1. Hold 10 min to extract DNA
  1. Keep 95 degree celcius for 3 minutes
 1. Put C into A2
 1. Move ~4uL from A1 to A2
 1. Amplification
 1. Detection

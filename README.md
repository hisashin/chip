# Summary

This project aims to make DNA test easy. As easy as pregnancy test with cheap disposable kits at room temperature.
No fridge, pipette, centrifuge, electrophoresis nor UV illuminator. DNA extractor([ex1](https://www.kaneka-labtest.com/en/pre/dna_version2.html), [ex2](https://www.funakoshi.co.jp/contents/64147)) and DNA chromatography chip([ex1](https://www.kaneka-labtest.com/en/chromato/index.html), [ex2](https://www.kurabo.co.jp/bio/English/product/products.php?M=D&PID=99), [ex3](https://techcrunch.com/2016/05/06/zika-test/)) should be used instead. Thermal cycler is needed at first but we have [NinjaPCR](https://github.com/hisashin/NinjaPCR) and might be removed in future with [such tech](https://www.twistdx.co.uk/en/products/product/twistamp-basic).

Use case examples :
- Food allergy patients (even kids) can test their food by themselves.
- In pandemic, people can pick a blood from finger and test infectious diseases like Zika, by themselves.
- Halal test

Whole Procedure :

- Manufacturer (we)
   - Make preservable primer (P) and reverse primer (^P) placed in A2, one of two connected PCR tubes (T1+T2)
   - Make preservable DNA extraction solution and tissue prep solution (E)
   - Make preservable neutralization solution and reaction mix (N)
   - Make preservable DNA chromatography chip (C)
      - Design
      - Manufacture
   - Packaging, Inventory management, Sales and Shipping
- End User
   - Pick up ~10uL sample without specific tool (S)
   - Put S into T1
   - Put E into T1
   - Place T1+T2 into tube holder of thermal cycler
   - Prepare
      - Hold 10 min to extract DNA
      - Keep 95 degree celcius for 3 minutes
   - Put N into T2
   - Move ~4uL from T1 to T2
   - Amplification
   - Detection

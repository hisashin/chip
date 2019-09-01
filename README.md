# Summary

This project aims to make DNA test easy. Hopefully as easy as pregnancy test with cheap disposable kits at room temperature.
No fridge, pipette, vortex mixier, centrifuge, electrophoresis nor UV illuminator. DNA extractor([ref](https://www.kaneka-labtest.com/en/pre/dna_version2.html), [ref](https://www.funakoshi.co.jp/contents/64147)) and DNA chromatography chip([ref](https://www.kaneka-labtest.com/en/chromato/index.html), [ref](https://www.kurabo.co.jp/bio/English/product/products.php?M=D&PID=99), [ref](https://techcrunch.com/2016/05/06/zika-test/)) should be used instead. Thermal cycler is needed at first but we have [NinjaPCR](https://github.com/hisashin/NinjaPCR) and might be removed in future with [such tech](https://www.twistdx.co.uk/en/products/product/twistamp-basic).

Use case examples :
- Food allergy patients (even kids) can test their food by themselves. (500 million people)
- In pandemic, people can pick a blood from finger and test infectious diseases like Zika, by themselves. (200 million people/year only for Mararia)
- Halal test (1.6 billion muslim)

Whole Procedure :

![Whole procedure](https://github.com/hisashin/chip/blob/master/doc/images/procedure.png)

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
   - Extraction
      - Hold 10 min
      - Keep 95 degree celcius for 3 minutes
   - Put N into T2
   - Move ~4uL from T1 to T2
   - Amplification
   - Detection

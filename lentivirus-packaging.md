---
layout: protocols
title: Lentivirus packaging
author: Shaohe Wang
author_url: https://scholar.google.com/citations?user=R_-kJV4AAAAJ&hl=en
date: 2021-10-12
---

If you are new to lentivirus, please read this very helpful [guide article on lentivirus](https://www.addgene.org/guides/lentivirus/). For safety reasons, lentiviral vectors used for research purpose has been engineered to replication incompetent and often also self-inactivating after integration. Please use biosafety procedures BSL2 or higher for lentivirus work.

## Reagents

For tissue culture:

- 293 cells (e.g., Takara, Cat# 632273)
- DMEM (e.g., Thermo Fisher, 11965118)
- Fetal bovine serum (FBS; e.g., GE Healthcare/Cytiva, SH30070.03)
- 200 mM L-glutamine (e.g., Thermo Fisher, 25030081)
- 100x PenStrep (10,000 units/mL penicillin, 10,000 µg/mL streptomycin; e.g., Thermo Fisher, 15140163)
- DMEM/F-12 (e.g., Thermo Fisher, 11039047)
- Chloroquine

1. To make _DMEM Complete_ medium for 293 cells, add 50 mL FBS, 5 mL L-Glutamine and 5 mL 100x PenStrep to 500 mL DMEM. Filter sterilize and store at 4°C.

Plasmids for transfection:

- Packaging plasmid [psPAX2](https://www.addgene.org/12260/)
- VSV-G envelope plasmid [pMD2.G](https://www.addgene.org/12259/)
- Your lentiviral transfer plasmids (e.g., sgRNA-expressing plasmids made from [pW212](https://www.addgene.org/170810/))

Reagents for transfection:

- 1 M HEPES-NaOH, pH 7.50
- 5 M NaCl
- 150 mM Na<sub>2</sub>HPO<sub>4</sub>
- 2 M CaCl<sub>2</sub>

1. To make 0.3 M CaCl<sub>2</sub>, mix 30 mL 2 M CaCl<sub>2</sub> with 170 mL H<sub>2</sub>O (Millipore purified water or Ultrapure water). Filter sterilize and keep at 4°C.

1. To make 2x HBS pH 7.10:

| Working concentration | Stock concentration | Volume for 200 mL |
|:---|:---|:---|
| H<sub>2</sub>O | - | 176.8 mL (use 150 mL first; adjust pH to 7.10 with NaOH; then adjust volume to 200 mL) |
| 50 mM HEPES | 1 M | 10 mL |
| 280 mM NaCl | 5 M | 11.2 mL |
| *1.5 mM Na<sub>2</sub>HPO<sub>4</sub> | 150 mM | 2 mL |

*Na<sub>2</sub>HPO<sub>4</sub>-7H<sub>2</sub>O, MW = 268.07 g/mol

After adjusting pH and volume, filter sterilize and keep at 4°C. Periodically check the pH of 2X HBS using pH paper, since correct pH is the key for efficient transfections.


## Procedure for lentivirus packaging

### 1. Day 1: Seed 293 cells for transfection.

- For each virus to make, seed 4 million 293 cells per 10-cm dish, or 10 million 293 cells per 15-cm dish.

	- Packaging with a 10-cm dish is often sufficient, but a 15-cm dish may be preferred for lentiviral vectors expected to be more difficult. For example, if the lentiviral vector is large so that the between LTR length is approaching the packaging limit.
	- 293 cells are used for lentivirus packaging because they are very easy to transfect. We routinely get >80% transfection efficiency with classical calcium co-precipitation method using 293TN from System Biosciences or AAV-293 from Takara Clontech (Takara, Cat# 632273).

### 2. Day 2: Transfection

- Check seeded cells: they should be ~80% confluent.
	- If cells are slightly low confluency, wait for half a day before transfecting. Cells can be transfected within 50-80% confluence, but the more cells you have the higher titer you will get.
	- If the cells are apparently slow growing, consider thawing early passage stocks.

- If cells are ready:
	- Warm up 2x HBS (pH = 7.10) and 0.3 M CaCl2 solution to room temperature.
	- Thaw the stock plasmid DNAs: your lentiviral vector, the packaging plasmid psPAX2 and the envelope plasmid pMD2.G.
	- Warm up enough DMEM complete.
	- Thaw an aliquot of 25 mM chloroquine.

- Replace medium in each dish with 8 mL fresh media + 25 uM chloroquine.
(3) In one set of 15 mL tubes, add 1 mL 2× HBS.  In another set of tubes, add 10 ug your lentiviral plasmid, 10 ug pR16 and 10 ug pR17.  Then proceed one by one for transfection.  For each plasmid to transfect, add 1 mL 0.3 M CaCl2, pipet to mix well.  Add this mixture into the tube containing 2× HBS dropwise.  Pipet to mix well.
(5) Immediately add this mixture dropwise into a 10-cm dish for transfection.  Replace medium with 8 mL fresh medium + 25 uM chloroquine after 6-12 hours of transfections (can be overnight).

Day 3-4: Collect virus-containing supernatant
(1) At ~24 hour post the first medium change, collect the supernatant into a 50 mL tube, and add back 8 mL fresh medium + 25 uM chloroquine.  Store at 4°C.
(2) After another 24 hours, collect the supernatant into the same 50 mL tube stored at 4°C.
For new constructs, the lenti-Go-Stix can be used as a handy tool to estimate the viral titer at this point.
(3) Filter the pooled supernatant through a 0.45 um filter (use SteriFlip for convenience).  If not concentrating, the filtered solution can be directly used, or stored at -80°C after freezing in liquid N2 or dry ice.
(4) Add ~4 mL 5× PEG-it reagent (System Biosciences, LV825A-1), mix well by pipetting.  Refrigerate for at least 12 hours at 4°C.  Virus solution with PEG is stable for up to 5 days at 4°C.
Day 5: Collect concentrated virus
(1) Pre-cool the swinging-bucket centrifuge in the equipment room to 4°C.  Spin at 1500× g for 30 min at 4°C to collect the virus.  *Keep the tube on ice during transfer.
(2) Remove the supernatant as much as possible by aspirating.
(3) Resuspend the pellet with 1/10 to 1/100 of the original viral solution volume of medium (DMEM/F12 + PenStrep).  Store at -80°C.  I typically use 500 uL.
The lenti-Go-Stix can be used to estimate the viral titer at this point after 1:100 dilution of the viral stock.
Aliquoting can be done but is not necessary, as PEG provides cryoprotection for the solution, and data has shown freeze-thaw for up to 5 times do not seem to affect the virus titer.

---
layout: protocols
title: PCR Amplification
author: Shaohe Wang
author_url: https://scholar.google.com/citations?user=R_-kJV4AAAAJ&hl=en
date: 2020-10-25
---

### 1. Reagents

We always use a high-fidelity DNA polymerase (such as Q5, Phusion, or Pfu) to amplify a DNA fragment for molecular cloning to minimize the chance of introducing mutations. However, for genotyping or other applications that do not require high-fidelity, Taq and its enhanced derivatives are perfectly fine. Our current favorite is the [Q5 Hot Start High-Fidelity 2X Master Mix](https://www.neb.com/products/m0494-q5-hot-start-high-fidelity-2x-master-mix#Product%20Information).

### 2. Procedure

1. Prepare PCR reactions. We usually use the [8-tube PCR strips](https://www.usascientific.com/0.2ml-pcr-8-tube-strip-8-capstrips/p/PCR-Tu-Pull-Dome).

    | Stock | µL for 50 µL | ×5 | ×10 | ×15 |
    |:---|:---|:---|:---|:---|
    | [2× Q5 master mix](https://www.neb.com/products/m0492-q5-high-fidelity-2x-master-mix#Product%20Information)	| 25 | 125 | 250 | 375 |
    | Water |  18 | 90 | 180 | 270 |
    | Primer 1 | 2.5 | 12.5 | 25 | 37.5 |
    | Primer 2 | 2.5 | 12.5 | 25 | 37.5 |
    | Template (10-20 ng/µL) | 2 | 10 | 20 | 30 |

1. Typical cycling conditions:

    - 98°C, 2 min

    - 30× cycles of:
      - 98°C, 10 sec
      - 55-60°C, 15 sec
      - 72°C, 10 sec/kb for short fragments, ~30 sec/kb for long fragments]

    - 72°C, 2 min

    - 12°C, hold

# Genome Exploration II — Callithrix jacchus

Individual assignment analyzing the genome assembly of the common marmoset 
(*Callithrix jacchus*, isolate 240, calJac240_pri) using Galaxy 
(usegalaxy.org).

## Overview
This project explores basic genome assembly statistics, sequence-length 
structure, and small-scale ORF (open reading frame) prediction using 
publicly available whole-genome shotgun sequence data.

## Workflow
1. **Assembly statistics** — Ran Fasta Statistics on the genome FASTA to 
   generate summary stats (total length, N50/L50, GC content, etc.)
2. **Sequence-length structure** — Sorted sequences by length to identify 
   the five longest scaffolds/chromosomes
3. **Filtering** — Applied a ≥10 kb length filter and compared before/after 
   statistics
4. **Small ORF exploration** — Extracted a ~19.6 kb region from chromosome 1 
   and ran EMBOSS getorf (min. ORF size ~300 bp) to identify candidate 
   open reading frames

## Key Results
- Total assembly length: ~2.93 Gb across 25 scaffolds
- N50: 141,933,726 bp / L50: 9
- GC content: 40.83%
- 402 ORFs identified in the test region; longest ORF = 1,191 bp

## Tools Used
- Galaxy (usegalaxy.org)
- Fasta Statistics
- Sort
- Filter sequences by length
- EMBOSS getorf

## Notes
ORFs identified here are computational predictions only — an ORF is a 
stretch of sequence lacking an internal stop codon under the chosen 
criteria, not a confirmed gene. Validating a true gene requires further 
evidence (annotation, transcript data, protein similarity, or dedicated 
gene-prediction methods).

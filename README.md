# TP53 Mutation Hotspot Scanner

This is a lightweight Python script I built to automate the search for clinical mutation hotspots in the human *TP53* tumor suppressor gene. 

Normally, finding a specific target sequence means manually searching NCBI, downloading massive FASTA files, and trying to parse them by hand. I wanted to speed this up, so I wrote this script to handle the pipeline computationally.

### What it does:
1. **Connects to NCBI:** Uses Biopython's `Entrez` module to securely and programmatically fetch the raw *TP53* mRNA transcript (`NM_000546`).
2. **Parses the Data:** Uses `SeqIO` to clean up the raw FASTA file and isolate the pure nucleotide sequence.
3. **Scans for Targets:** Scans the entire 2,500+ base pair sequence for a predefined target probe (representing a mutation hotspot) and outputs the exact coordinate if it finds a match. 

### Built With
* Python 3
* Biopython (`Entrez`, `SeqIO`)

### Quick Setup
To run this yourself, just make sure you have Biopython installed:
`pip install biopython`

*Note: NCBI requires an email address to use their programmatic databases. If you clone this script, just swap in your own email at the top of the file so they don't block your connection!*

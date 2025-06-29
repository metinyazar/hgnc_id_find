# hgnc_id_find
Maps gene symbols (official, previous, and aliases) to HGNC, Ensembl, and Entrez IDs using the HGNC complete dataset for standardized gene identifier lookup.
Gene Symbol Mapping from HGNC Complete Dataset
This script builds a comprehensive lookup dictionary to map gene symbols—including official symbols, previous names, and aliases—to standardized identifiers from the HGNC complete set. The identifiers include:

HGNC ID
Ensembl Gene ID
Entrez Gene ID

Features
Parses the HGNC complete dataset (hgnc_complete_set.txt) and extracts relevant columns.

Constructs a symbol-to-identifier dictionary that includes:

Official gene symbols

Previous gene symbols

Alias symbols

Normalizes input gene names (e.g., trimming whitespace, converting to uppercase).

Provides a lookup_gene_info() function to retrieve (HGNC ID, Ensembl ID, Entrez ID) tuples.

Applies the lookup function to two input columns (lead_gene, partner_gene) in a user-defined DataFrame to enrich gene data with identifiers.

Usage
Ensure the following:

Your input file is in a pandas DataFrame named file with columns lead_gene and partner_gene.

The HGNC file path (hgnc_complete_set.txt) is correctly set to your local directory.

Example output columns added to file:

hgnc_id_1, ensembl_gene_id_1, entrez_id_1 (from lead_gene)

hgnc_id_2, ensembl_gene_id_2, entrez_id_2 (from partner_gene)

Dependencies
Python 3.x

pandas

numpy


🧬 Step-by-Step Guide to Perform the Experiment
🔹 Objective:

Predict the 3D structure of a given protein sequence using Homology Modeling or Threading.

🧩 Step 1: Choose Your Protein Sequence

Go to UniProt: https://www.uniprot.org

Search for any protein (e.g., “Hemoglobin subunit alpha (HBA1)” or “Lysozyme”).

Copy its FASTA sequence (a text format that looks like this):

>sp|P69905|HBA_HUMAN Hemoglobin subunit alpha OS=Homo sapiens OX=9606 GN=HBA1 PE=1 SV=2
VLSPADKTNVKAAWGKVGAHAGEYGAEALERMFLSFPTTKTYFPHF...


Save it in a text file named target.fasta.

🧪 Step 2: Identify a Template Using BLAST

We’ll find a known protein structure (template) similar to your protein.

Visit NCBI BLAST → https://blast.ncbi.nlm.nih.gov/

Select Protein BLAST.

Paste your sequence in the search box.

Choose Database: PDB (Protein Data Bank).

Click BLAST.

✅ Output:

You’ll get a list of templates with:

PDB IDs (e.g., 1A3N)

Sequence identity %

E-value (lower = better match)

Pick the template with highest identity (>30%) and lowest E-value.

🧱 Step 3: Perform Homology Modeling

You can do this using SWISS-MODEL (easiest, online) or MODELLER (Python-based).

🧭 Option 1: Using SWISS-MODEL (recommended)

Go to https://swissmodel.expasy.org/

Click on “Start Modelling”

Paste your target sequence.

It will automatically find the template and build your 3D model.

Download the resulting PDB file (predicted structure).

🧩 Step 4: Model Evaluation

After model generation, check its quality.

Use any of these:

SWISS-MODEL built-in QMEAN score

ProSA-web (https://prosa.services.came.sbg.ac.at/prosa.php
)

Ramachandran Plot (SAVES server) (https://saves.mbi.ucla.edu/
)

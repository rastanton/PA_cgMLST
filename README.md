# PA_cgMLST
Pseudomonas aeruginosa cgMLST
Requires Python, python modules biopython and dendropy, and blat (https://genome.ucsc.edu/goldenPath/help/blatSpec.html), the last of which has to be in your $PATH

Before the cgMLST script (PA_cgMLST_Exe.py) can be run, a directory for the individual alleles needs to be made. Once made, the individual allele fasta files can be constructed using the PA_cgMLST_Fasta_Alleles.py script and the full allele fasta using this command:

> python PA_cgMLST_Fasta_Alleles.py PA_cgMLST_Alleles.fasta Folder/For/Alleles

Once that script is run, the PA_cgMLST_Exe.py can be run in a folder with annotated P. aeruginosa annotated gene multifastas with a ".ffn" file extension, like those made using Prokka (https://github.com/tseemann/prokka, using the PAO1_Allele_Matches.fasta and the folder that was created for the alleles:

> python PA_cgMLST_Exe.py PA_cgMLST_Alleles.fasta Folder/For/Alleles

This will make three folders in your directory (cgMLST_PSL, cgMLST_Allele_Matches, and cgMLST_Trees). The cgMLST_PSL folder will contain the .psl files generated by blat, the cgMLST_Allele_Matches will contain the cgMLST allele match files (matches for each allele will be on each line), and the resultant distance matrix and tree files (using the Neighbor Joining and UPGMA methods).

Org: NCEZID\
Version: 1.0\
Status: Maintained\
Keywords: outbreak, pseudomonas aeruginosa, cgMLST\
Labor Hours: 500\
Contact Email: ncezid_shareit@cdc.gov

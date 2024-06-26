# Spectral entropy
Spectral entropy is an application of Shannon entropy from information theory (1, 2). <br>
Please [view for more documentation](https://docs.google.com/document/d/1tOoKTudIaQwRFRsWvQ1QJ-Z4d3uWjV11klk7XFXWLuQ/edit). <br>
Brief steps:<br>
1. Create reference file with `./makeCustomGenomeSizes.sh` ; change `species`, `blacklist_path`, and `telomere_path` ; if using hg38, you can use `/new-stg/home/eunice_2/Entropy/00_LocalKL/18_new/hg38_res.3000.bed_res.3000.bed.size.200.bed` and skip this step. 
2. Create pseudobulks using `./PrepareCells.R` ; change the `seurat_path`, `conditions`, and `cell_` parameters with the path to your seurat object, meta column with conditions i.e. AD vs Control, and meta column with celltype labels, respectively.
3. `sbatch head.sh` ; change the `inputdir` with the output directory from `PrepareCells.R` ; set the `outputdir` with the output directory path ; set the `codedir` with the directory with all the copied script ; all outputs are saved in the `outputdir` variable.
<br>

References
1. Shannon, C. E. A mathematical theory of communication. Bell Syst. Tech. J. 27, 379–423 (1948).
2. Li, Y., Kind, T., Folz, J. et al. Spectral entropy outperforms MS/MS dot product similarity for small-molecule compound identification. Nat Methods 18, 1524–1531 (2021). 

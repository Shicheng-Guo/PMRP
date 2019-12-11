#### Genetics and Epigenetics data analysis to Personalized Medicine Research Dataset in MCRI


Timeline:
* 2019/12/10: Phase2-8500/8648, re-imputation and phasing again: `/gpfs/home/guosa/hpc/project/pmrp/phase1/round2`
* 2019/12/10: Phase1-10124, re-imputation and phasing again: `/gpfs/home/guosa/hpc/project/pmrp/phase1/round2`
* remove deletion/duplication: `plink --bfile $plink --list-duplicate-vars ids-only suppress-first`
* plink --bfile S_Hebbring_Unr --update-alleles top_to_forward.txt --make-bed --out S_Hebbring
* phase2 raw data were saved in `/mnt/bigdata/Genetic/Projects/S_Hebbring_2128_Released_Data`
* phase1 raw data were saved in `/mnt/bigdata/Genetic/Projects/EXOMECHIP_MARSHFIELD`




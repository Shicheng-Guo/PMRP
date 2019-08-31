
```
cd /gpfs/home/guosa/hpc/project/pmrp/merge
mkdir temp
for i in {1..24}
do
echo \#PBS -N $i  > $i.job
echo \#PBS -l nodes=1:ppn=1 >> $i.job
echo \#PBS -M Guo.shicheng\@marshfieldresearch.org >> $i.job
echo \#PBS -m abe  >> $i.job
echo \#PBS -o $(pwd)/temp/ >>$i.job
echo \#PBS -e $(pwd)/temp/ >>$i.job
echo cd $(pwd) >> $i.job
echo plink --bfile PMRP-Phase1-phase2-Full --chr $i --recode vcf --out PMRP2019.chr$i >>$i.job
echo bcftools view PMRP2019.chr$i.vcf -Oz -o PMRP2019.chr$i.vcf.gz >>$i.job
qsub $i.job
done
```

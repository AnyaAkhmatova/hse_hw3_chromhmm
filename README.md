# hse_hw3_chromhmm

# Майнор "Биоинформатика". 2 год, 2 семестр.
## Домашнее задание 3.

Google colab ноутбук: https://colab.research.google.com/drive/1HWfpqiuzVt3d0BNGu_SOobRb6wFzW_Sb#scrollTo=x70xq0JkveJD.

Была выбрана клеточная линия DND-41. 

Список 10-ти гистоновых меток (и соответствующих имен файлов), для которых был сделан анализ:

| Гистоновая метка  | Файл |
| ------------- | ------------- |
| H2az | wgEncodeBroadHistoneDnd41H2azAlnRep1.bam |
| H3k27ac | wgEncodeBroadHistoneDnd41H3k27acAlnRep1.bam |
| H3k27me3 | wgEncodeBroadHistoneDnd41H3k27me3AlnRep1.bam | 
| H3k36me3 | wgEncodeBroadHistoneDnd41H3k36me3AlnRep1.bam |
| H3k04me1 | wgEncodeBroadHistoneDnd41H3k04me1AlnRep1.bam |
| H3k04me2 | wgEncodeBroadHistoneDnd41H3k04me2AlnRep1.bam |
| H3k04me3 | wgEncodeBroadHistoneDnd41H3k04me3AlnRep1.bam |
| H3k79me2 | wgEncodeBroadHistoneDnd41H3k79me2AlnRep1.bam |
| H3k09ac | wgEncodeBroadHistoneDnd41H3k09acAlnRep1.bam | 
| H3k09me3 | wgEncodeBroadHistoneDnd41H3k09me3AlnRep1.bam |
| control | wgEncodeBroadHistoneDnd41ControlStdAlnRep1.bam |

[Файл cellmarkfiletable.txt](https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/cellmarkfiletable.txt)

[Папка с выдачей ChromHMM](https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/tree/main/ChromHMM_output/modelData), [та же папка на google disk](https://drive.google.com/drive/folders/1-CrUVKGdrw9XMUEF_eB8LMj9R4glhJFx?usp=share_link)

____

### Картинки из выдачи ChromHMM

<img src="https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/ChromHMM_output/modelData/transitions_10.png" width="300" height="350"> <img src="https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/ChromHMM_output/modelData/emissions_10.png" width="300" height="350"> <img src="https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/ChromHMM_output/modelData/Dnd41_10_overlap.png" width="300" height="350">

<img src="https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/ChromHMM_output/modelData/Dnd41_10_RefSeqTSS_neighborhood.png" width="450" height="350"> <img src="https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/ChromHMM_output/modelData/Dnd41_10_RefSeqTES_neighborhood.png" width="450" height="350">

____

### Табличка с номерами эпигенетических типов, их характерные эпигенетические метки и другие свойства, а также присвоенные им названия

| Номер состояния  | Название | Метки и расположение | Screenshot |
| ------------- | ------------- | ------------- | ------------- |
| 1 | Active promoter | <ul><li>для состояния характерны метки H3k04me1, H3k27ac, H3k09ac, H3k04me2, H3k04me3, H2az, H3k79me2</li><li>проявляется преимущественно в CpGIsland, RefSeqExon, RefSeqTSS, RefSeqTSS2kb, реже в RefSeqGene, RefSeqTES</li><li>сконцентрировано около TSS</li></ul>| ![](https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/images/1.png)|
| 2 | Weak enhancer | <ul><li>для состояния характерны метки H3k04me1, H3k27ac, H3k09ac, H3k04me2, H2az</li><li>проявляется преимущественно в RefSeqTES, laminB1lads, реже в RefSeqExon, RefSeqGene</li></ul> | ![](https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/images/2.png) |
| 3 | Weak enhancer | <ul><li>для состояния характерны метки H3k04me1, H3k27ac, H3k04me2, H2az</li><li>проявляется преимущественно в RefSeqTES, laminB1lads, реже в RefSeqExon, RefSeqGene, RefSeqTSS2kb</li></ul> | ![](https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/images/3.png) |
| 4 | Strong enhancer | <ul><li>для состояния характерны метки H3k04me1, H3k27ac, H3k09ac, H3k04me2, H3k04me3, H3k79me2, H3k36me3</li><li>проявляется преимущественно в RefSeqGene, RefSeqTES, реже в RefSeqExon, RefSeqTSS2kb</li></ul> | ![](https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/images/4.png) |
| 5 | Transcribed | <ul><li>для состояния характерна метка H3k79me2</li><li>проявляется преимущественно в RefSeqGene</li></ul> | ![](https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/images/5.png) |
| 6 | Transcribed | <ul><li>для состояния характерны метки H3k79me2, H3k36me3</li><li>проявляется преимущественно в RefSeqExon, RefSeqGene, RefSeqTES</li></ul> | ![](https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/images/6.png) |
| 7 | Transcribed | <ul><li>для состояния характерна метка H3k36me3</li><li>проявляется преимущественно в RefSeqExon, RefSeqGene, RefSeqTES</li></ul> | ![](https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/images/7.png) |
| 8 | Heterochromatin | <ul><li>для состояния характерна метка H3k09me3</li><li>проявляется преимущественно в laminB1lads (ядерная ламина), реже в RefSeqExon, RefSeqTES</li></ul> | ![](https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/images/8.png) |
| 9 | Repressed | <ul><li>для состояния ни одна из меток нехарактерна</li><li>проявляется преимущественно в laminB1lads (ядерная ламина)</li></ul> | ![](https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/images/9.png) |
| 10 | Heterochromatin | <ul><li>для состояния характерна метка H3k27me3</li><li>проявляется преимущественно в laminB1lads (ядерная ламина), реже в RefSeqExon, RefSeqGene, RefSeqTES</li></ul> | ![](https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/images/10.png) |

____
### Список всех запущенных команд:

Установка java и ChromHmm
```
!curl -O https://raw.githubusercontent.com/deepjavalibrary/d2l-java/master/tools/fix-colab-gpu.sh && bash fix-colab-gpu.sh
!curl -O https://raw.githubusercontent.com/deepjavalibrary/d2l-java/master/tools/colab_build.sh && bash colab_build.sh
!java --list-modules | grep "jdk.jshell"
!wget http://compbio.mit.edu/ChromHMM/ChromHMM.zip
!unzip /content/ChromHMM.zip
```

Скачивание файлов
```
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneDnd41H2azAlnRep1.bam -o H2azAlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneDnd41H3k27acAlnRep1.bam -o H3k27acAlnRep1.bam 
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneDnd41H3k27me3AlnRep1.bam -o H3k27me3AlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneDnd41H3k36me3AlnRep1.bam -o H3k36me3AlnRep1.bam 
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneDnd41H3k04me1AlnRep1.bam -o H3k04me1AlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneDnd41H3k04me2AlnRep1.bam -o H3k04me2AlnRep1.bam 
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneDnd41H3k04me3AlnRep1.bam -o H3k04me3AlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneDnd41H3k79me2AlnRep1.bam -o H3k79me2AlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneDnd41H3k09acAlnRep1.bam -o H3k09acAlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneDnd41H3k09me3AlnRep1.bam -o H3k09me3AlnRep1.bam
! wget http://hgdownload.cse.ucsc.edu/goldenPath/hg19/encodeDCC/wgEncodeBroadHistone/wgEncodeBroadHistoneDnd41ControlStdAlnRep1.bam -o ControlStdAlnRep1.bam
```

BinarizeBam
```
!java -mx5000M -jar /content/ChromHMM/ChromHMM.jar BinarizeBam -b 200  /content/ChromHMM/CHROMSIZES/hg19.txt /content/ cellmarkfiletable.txt   binarizedData
```

LearnModel
```
!java -mx5000M -jar /content/ChromHMM/ChromHMM.jar LearnModel -b 200  /content/binarizedData/ /content/modelData/ 10 hg19
```

____

### Бонус

```
names = ['1_active_promoter',
         '2_weak_enhancer',
         '3_weak_enhancer',
         '4_strong_enhancer',
         '5_transcribed',
         '6_transcribed',
         '7_transcribed',
         '8_heterochromatin',
         '9_repressed',
         '10_heterochromatin']

lines = []
with open('Dnd41_10_dense.bed', 'r') as f:
    lines = f.readlines()

for i in range(1, len(lines)):
    line = lines[i].split(sep='\t')
    line[3] = names[int(line[3]) - 1]
    lines[i] = '\t'.join(line)

with open('Dnd41_10_dense.bed', 'w') as f:
    for line in lines:
        f.write(line)
```

![](https://github.com/AnyaAkhmatova/hse_hw3_chromhmm/blob/main/images/new.png)

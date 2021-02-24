#提高安装R包的速度

options(BioC_mirror="https://mirrors.tuna.tsinghua.edu.cn/bioconductor/")

options("repos" = c(CRAN="http://mirrors.cloud.tencent.com/CRAN/")) 

options(download.file.method = 'libcurl')

options(url.method='libcurl')


singleR

("https://ltla.github.io/SingleRBook/using-the-classic-mode.html")
samtools 
samtools view -h -q 1 -F 4 -F 256 big.sort.dedup.bam |grep -v XA:Z |grep -v SA:Z |samtools view -b - > big.sort.dedup.unique.bam

其中参数：

-q 1：过滤掉比对质量小于1的reads；

-F 4：过滤掉没有比对上的reads；

-F 256：过滤掉比对上的多次的reads。


library(data.table)

geoData <- fread(txtFile, sep="\t")

geneNames <- unname(unlist(geoData[,1, with=FALSE]))

exprMatrix <- as.matrix(geoData[,-1, with=FALSE])

#提高安装R包的速度

options(BioC_mirror="https://mirrors.tuna.tsinghua.edu.cn/bioconductor/")

options("repos" = c(CRAN="http://mirrors.cloud.tencent.com/CRAN/")) 

options(download.file.method = 'libcurl')

options(url.method='libcurl')

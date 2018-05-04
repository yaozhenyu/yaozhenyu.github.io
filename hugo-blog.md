# Hugo生成静态网站
## 安装hugo
1. go语言安装  
`go get -d github.com/gohugoio/hugo`  
由于github访问很慢，故建议直接下载二进制文件。
2. 二进制文件安装  
下载地址: https://github.com/gohugoio/hugo/releases  
[点击下载windows64位hugo-v0.40.2](https://github.com/gohugoio/hugo/releases/download/v0.40.2/hugo_0.40.2_Windows-64bit.zip)  
解压后，把`hugo.exe`文件所在目录添加到`PATH`环境变量中去。这种方式不需要安装go语言。
3. linux安装（ubuntu)  
`sudo apt-get install hugo`

查看是否安装成功，打开命令行工具输入命令`hugo version` 如果有`Hugo Static Site Generator v0.40.2 windows/amd64 BuildDate: 2018-04-30T06:48:14Z`这样的信息输出则说明安装成功。

## 基本使用
1. 新建一个项目myblog  
`hugo new site myblog`生成一个目录myblog，或者`hugo new site .`直接在当前目录生成一个项目。
2. `hugo server` 用浏览器打开 http://localhost:1313 查看效果。

## 皮肤

![GoIndex](https://raw.githubusercontent.com/donwa/goindex/master/themes/logo.png)  

GoIndex  
====  
基于 [Cloudflare Workers](https://workers.cloudflare.com/) 和 [Google Drive](https://www.google.com/drive/) 的功能，你可以部署你的代码在Cloudflare Workers，实现以目录形式展示google drive中的文件。

`index.js` 包含 Workers 所需的代码.  

## Demo  
material:  
[https://index.gd.workers.dev/](https://index.gd.workers.dev/)  
classic:  
[https://indexc.gd.workers.dev/](https://indexc.gd.workers.dev/)  

## 安装部署方案1  
1、在本地安装 rclone   
2、按照 https://rclone.org/drive/ 流程进行授权。  
3、执行 rclone config file 查看 rclone.conf 路径。找到root_folder_id和refresh_token记录下来。  
4、下载 https://github.com/donwa/goindex 中的 index.js  并填入 root 和 refresh_token  
5、复制代码 到 CloudFlare 部署。  

## 安装部署方案2  
作者不会记录refresh_token，但为避免纠纷，建议有条件的同学使用方案1进行部署  
1、访问[https://install.gd.workers.dev/](https://install.gd.workers.dev/)  
2、授权认证后，生成部署代码。  
3、复制代码 到 CloudFlare 部署。  

## 文件夹密码：
在google drive 文件中放置 `.password` 文件来设置密码。  
密码文件只能保护该文件不被列举，不能保护该文件夹的子文件夹不被列举。  
也不保护文件夹下文件不被下载。  
  
程序文件中 `root_pass` 只为根目录密码，优先于 `.password` 文件  


## 更新日志  

1.0.6  
添加 classic 模板  

1.0.5  
添加文件展示页  

1.0.4  
修复 注入问题。  

1.0.3  
修复 `.password` 绕过下载问题。  

1.0.2  
优化前端逻辑  
添加文件预览功能(临时)  
添加前端文件缓存功能  
  
1.0.1  
添加 README.md 、 HEAD.md 支持  
  
1.0.0  
前后端分离，确定基本架构  
添加.password 支持  

--------------
Google Drive Directory Index  
Combining the power of [Cloudflare Workers](https://workers.cloudflare.com/) and [Google Drive](https://www.google.com/drive/) will allow you to index you files on the browser on Cloudflare Workers.    

`index.js` is the content of the Workers script.  


## Deployment  
1.Install `rclone` software locally  
2.Follow [https://rclone.org/drive/]( https://rclone.org/drive/) bind a drive  
3.Execute the command`rclone config file` to find the file `rclone.conf` path  
4.Open `rclone.conf`,find the configuration `root_folder_id` and `refresh_token`  
5.Download index.js in https://github.com/donwa/goindex and fill in root and refresh_token  
6.Deploy the code to [Cloudflare Workers](https://www.cloudflare.com/)

## Quick Deployment  
1.Open https://installen.gd.workers.dev/  
2.Auth and get the code  
3.Deploy the code to [Cloudflare Workers](https://www.cloudflare.com/)  



## About  
Cloudflare Workers allow you to write JavaScript which runs on all of Cloudflare's 150+ global data centers.  

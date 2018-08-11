# node-opencv
用node搭建人脸识别环境

### 一、准备工作
* Windows 7 旗舰版 64位操作系统
* node 环境 v8.11.3-x64
* python 2.7
* OpenCV 2.4.9

### 二、安装部署
* 安装 OpenCV
  * 将下载好的 OpenCV 安装到 C 盘，然后添加环境变量 OPENCV_DIR 值为 C:\opencv\build\x64\vc12
* 安装 Python
* 安装 node
  * 建议使用 cnpm 安装
  * 运行命令 cnpm install opencv

### 三、错误处理
* 未能加载 Visual C++ 组件“VCBuild.exe”
  * cnpm install -g node-gyp
  * cnpm install --global --production windows-build-tools
  * 尝试运行以上两条命令，然后再次安装，如果还不行，建议自行下载 Microsoft Visual C++ 2013
  
* 缺少各种 dll 文件
  * 首先将 C:\opencv\build\x64\vc12\bin 下面的 dll 文件全部复制到 C:\Windows\System32 下面
  * 使用一个小工具 depends 打开 \node_modules\_opencv@6.0.0@opencv\build\opencv\v6.0.0\Release\node-v57-win32-x64\opencv.node 二进制文件，它会显示该文件缺少哪些 dll 文件，请自行下载，放入 C:\Windows\System32 下面
  
如何使用请参阅 https://github.com/peterbraden/node-opencv <br/>
示例请参阅 http://www.liuhongyi.net/content/1.html

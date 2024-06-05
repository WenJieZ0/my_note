# docker
## 安装
* 环境：windows(win10_19044以下版本)
  1. 进入bios，开启cpu虚拟化技术（通过任务管理器-性能-CPU-虚拟化参数检验是否开启）
  2. 打开控制面板-程序-程序和功能-启用或关闭windows功能-找到Hyper-V-如果勾选了则取消勾选-重启
  3. 安装Docker Toolbox，[参考文档](https://blog.csdn.net/yangxiao_hui/article/details/107504733)
    * 除文档中描写的安装问题外如果出现问题如`This computer doesn’t have VT-X/AMD-v enabled. Enabling it in the BIOS is mandatory!`，[解决方案，文本编辑sh脚本修改命令](https://blog.csdn.net/yunhuaikong/article/details/133956112)
    * 下载boot2docker.iso可能一直下不下来，访问dos提示中的版本地址浏览器直接下载，根据文档指示操作。
* 环境：windows(win10_19044以上)
  1. [安装参考](https://blog.csdn.net/GoodburghCottage/article/details/131413312)
    * 如果出现`Docker Engine stopped`问题，[参考文档](https://blog.csdn.net/cplvfx/article/details/138033592)
## 卸载
* 卸载Docker Toolbox，[参考文档](https://blog.csdn.net/wang465745776/article/details/80143054)
## 后端生产环境构建
* dockerfile 
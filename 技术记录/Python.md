# Python
- [Python](#python)
- [Python虚拟环境的使用](#python虚拟环境的使用)
  - [创建虚拟环境](#创建虚拟环境)
  - [激活虚拟环境](#激活虚拟环境)
    - [更改PowerShell执行策略](#更改powershell执行策略)
    - [安装依赖](#安装依赖)
  - [退出虚拟环境](#退出虚拟环境)

# Python虚拟环境的使用
## 创建虚拟环境
>在非C盘创建虚拟环境时要更改PowerShell执行策略才可激活虚拟环境

当python版本高于3.3 的时候可以直接使用venv模块来创建虚拟环境
```shell
python -m venv myenv
```
使用该命令会在终端当前的路径下创建一个`myenv`文件夹作为虚拟环境

## 激活虚拟环境

在刚才myenv的上一级目录的终端中激活虚拟环境
```shell
myenv\Scripts\activate
```
使用该命令后会激活虚拟环境
### 更改PowerShell执行策略
-  PowerShell 自由运行本地创建的脚本：
    ```shell
    Set-ExecutionPolicy RemoteSigned
    ```
- 禁止 PowerShell 运行脚本：
    ```shell
    Set-ExecutionPolicy Restricted
    ```

### 安装依赖
因为虚拟环境的目的就是为了隔离环境，所以不同的环境中要安装不同的依赖

和平时一样使用 `pip install` 来安装

```shell
pip install xxx
```


## 退出虚拟环境
使用`deactivate`命令退出虚拟环境
```shell
deactivate
```


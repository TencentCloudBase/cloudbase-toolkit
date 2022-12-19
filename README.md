# Tencent CloudBase Toolkit

> 注意：该 vscode 插件已停止维护！！！

Tencent CloudBase Toolkit 是腾讯云 - 云开发发布的 VS Code（Visual Studio Code）插件。该插件可以让您更好地在本地进行云开发项目开发和代码调试，并且轻松将项目部署到云端。

通过 Tencent CloudBase Toolkit 插件，您可以：

-   在本地快速创建云开发项目
-   在本地创建简单的 Node 云函数
-   同步云端的云函数列表，并下载函数代码到本地
-   部署云函数到云端，支持云端安装依赖
-   对云函数进行简单的操作，如删除云函数、查看云函数详细信息
-   增量更新云函数文件
-   删除云端的云函数文件
-   部署静态托管文件到云端
-   创建云开发 cloudbaserc 配置文件

## 安装 CloudBase Toolkit 插件

### 1. 运行 VS Code IDE。

### 2. 打开 VS Code 插件市场。

### 3. 在搜索框中输入 `Tencent CloudBase Toolkit`，单击搜索框下方列表中的 `Tencent CloudBase Toolkit` 插件查看详情并选择【install】

## 创建环境

如果你已经开通了云开发服务，并创建了相关环境，可以跳过此步骤。

### 1. 登录腾讯云官方账号  

打开[腾讯云官网](https://cloud.tencent.com/)，注册腾讯云账号，然后登录账号。如有账号，可以直接登录。

### 2. 开通云开发

进入[云开发主页](https://cloud.tencent.com/product/tcb)，授予相关权限开通使用。

### 3. 创建环境

点击 **新建环境**，输入环境名称，选择按量计费模式，点击立即开通，等待服务开通完成后继续进行下面的操作。

## 配置

### 1. 单击左侧导航栏的图标，打开已安装好的 Tencent CloudBase Toolkit 插件。

![](https://main.qcloudimg.com/raw/e3eaa985a98675d071f4f367782b3444.png)

### 2. 点击登录

![](https://main.qcloudimg.com/raw/e7ff42a700bba0452bc1410469cba821.png)

### 3. 选择登录方式

CloudBase Toolkit 提供了两种登录方式，你可以通过腾讯云 - 云开发控制台登录，也可以使用腾讯云访问秘钥登录。

![](https://main.qcloudimg.com/raw/3e2fcab89d52ec399a108f9e19306a7b.png)

### 4. 创建配置文件

登录成功后，在 VSCode 窗口的右下方会有”登录成功“的提示。同时，如果当前项目下没有检测到 cloudbaserc 配置文件，CloudBase Toolkit 会提示你创建云开发项目，或创建配置文件。

创建云开发项目会拉取云端模块创建全新的项目，而创建配置文件只会在当前目录下生成 cloudbaserc 配置文件。

![](https://main.qcloudimg.com/raw/8c48de011ab9239080af8cf0b4ba5ca4.png)

## 使用

注意：CloudBase Toolkit 插件依赖于 `cloudbaserc` 配置文件，只有当前项目的根目录下存在 `cloudbaserc` 配置文件时，才能使用 CloudBase Toolkit 插件进行相关操作。

### 初始化云开发项目

如果你还没有云开发项目，可以使用初始化操作创建一个全新的云开发项目，CloudBase Toolkit 提供了部分模板项目供选择。

打开一个空的文件夹，点击侧边栏的云开发图标，点击下图示例中的条目

![](https://main.qcloudimg.com/raw/d74a2dca88a1e21736dc0bfbe2a00b66.png)

选择使用的云开发环境

![](https://main.qcloudimg.com/raw/74a8c3e8c187c9b04e8428af0ee3b50f.png)

选择项目使用的开发语言

![](https://main.qcloudimg.com/raw/bb6d56b43417235d9c82156b5e641983.png)

选择使用的模板，这里可以选择 Hello World 快速开始

![](https://main.qcloudimg.com/raw/bd12505aab00e241ff0c67c66301a07c.png)

等待模板下载完成，右下角会有提示。欢迎贡献你的模板~~

![](https://main.qcloudimg.com/raw/30a4cddd78e2bd15a182bcd7aa33a803.png)

项目目录结构

![](https://main.qcloudimg.com/raw/fae94ab052f64876225e0f2090bb263d.png)

### 部署云函数

**对云函数进行部署/删除/下载代码等操作时，必须选中云函数文件夹，否则会因为无法解析到准确的函数名称，而导致操作失败。**

右键选中函数文件夹，点击部署云函数即可。CloudBase Toolkit 支持同时选择多个云函数进行部署。

CloudBase Toolkit 支持两种部署云函数的方式：

1. 部署云函数（上传全部文件）：即将函数目录下的所有文件上传，也包含 node_modules 目录
2. 部署云函数（云端安装依赖）：只部署代码文件，会忽略 node_modules 目录，云函数会自动在线安装依赖

![](https://main.qcloudimg.com/raw/5450089421dba1b37009810413765536.png)

### 同步云函数列表

同步云函数列表功能可以把云端函数同步到本地，并创建对应的函数同名文件夹，但不会下载函数代码。此操作可以直接右键进行，无需选择函数。

![](https://main.qcloudimg.com/raw/155b13a33afa4a15447ce78dbd830561.png)

### 下载函数代码

使用下载函数代码功能，可以将云端函数代码下载到本地，进行操作时，需要选择云函数名称对应的目录。CloudBase Toolkit 支持同时选择多个云函数，下载云函数代码。

![](https://main.qcloudimg.com/raw/ca98ff95f3d279298b2b337ec2a8d8e8.png)

### 云函数增量更新

CloudBase Toolkit 支持上传单个文件或文件夹到云函数中，而无需重新上传整个云函数。

![](https://main.qcloudimg.com/raw/45fe187665da78a67800dd96de7cfdd2.png)

### 云函数删除云端文件

CloudBase Toolkit 支持删除云函数中的单个文件或文件夹，当删除文件夹时，文件夹下的文件也会被删除。

![](https://main.qcloudimg.com/raw/65d6adeae576b1880a179c47ab0376be.png)

### 云端云函数操作

点击侧边栏的云开发图标，可以查看云端部署的云函数。选择对应的云函数，右键可以对云函数进行删除、查看、下载等操作。

![](https://main.qcloudimg.com/raw/6043a30ed58a0f23419267f756fcbad1.png)

![](https://main.qcloudimg.com/raw/2f68db368b88656094557c56335a329c.png)

### 上传文件/文件夹到静态网站

CloudBase Toolkit 支持上传文件/文件夹到静态网站存储中，同时支持文件多选，既可以同时选择多个文件上传。

CloudBase Toolkit 提供了两种上传方法：

-   上传到静态托管：需要输入云端存放文件（夹）的**文件夹路径**，选中的文件（夹）将被上传到此路径下。
-   上传到静态托管（根目录）：选中的文件（夹）将被直接上传到根目录下

![](https://main.qcloudimg.com/raw/b9c306cb17c71834d89281448a8a92d7.png)

### 注销登录

使用 Ctrl+Shift+P 唤起命令面板，输入 `cloudbase` 进行搜索，选择注销登录命令即可。

![](https://main.qcloudimg.com/raw/dcaba91db66dc50ec1ec9d213283968a.png)

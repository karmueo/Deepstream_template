# Vscode调试

## 目录

- [教程](#教程)
- [使用方法](#使用方法)

## 教程 <a name = "教程"></a>

### 1. 需要 VSCode 的 .devcontainer 文件来了解如何将 docker 容器挂载为工作区。参考`.devcontainer/devcontainer.json`

- devcontainer.json 文件是一个配置文件，主要用于 Visual Studio Code 的 Remote - Containers 扩展功能。这个文件定义了如何在容器中设置和管理开发环境，使得开发者能够使用完全定义和容器化的开发环境进行工作。它允许团队成员在统一且配置一致的开发环境中工作，减少了“在我这里可以运行”的问题。

### 2. 配置 task

- 设置task，以便可以构建和测试代码。参考`.vscode/tasks.json`

### 3. 配置调试

- 一旦可以构建代码，可能想要运行和调试它。可以通过向 `.vscode/launch.json` 文件添加不同的配置来完成此操作

## 使用方法 <a name = "使用方法"></a>

### 1. 先决条件

#### 1. docker-ce安装

参考[docker安装](https://docs.docker.com/engine/install/)

#### 2. nvidia-container-toolkit安装

参考[nvidia-container-toolkit安装教程](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html)

### 3. 获取 NGC 帐户和 API 密钥
```sh
sudo apt-key del 7fa2af80
wget https://developer.download.nvidia.com/compute/cuda/repos/ubuntu2004/x86_64/cuda-keyring_1.0-1_all.deb
```

### 2. 用法

- 在Vscode中打开项目，按`ctrl+shift+p`，输入`Dev Containers: Reopen in Container`

## 构建与 CI 集成指南

本指南旨在为用户提供详细的构建和 CI 集成步骤，并引导用户参考小米官方 Vela/QuickApp 构建文档。

### 1. 本地构建

首先，确保安装了所需的构建工具和依赖项。然后使用以下命令进行本地构建：

```bash
# 官方构建命令示例
<PLACEHOLDER_FOR_BUILD_COMMAND>
```

### 2. CI 构建

在 GitHub Actions 中设置 CI 构建流程。以下是一个 GitHub Actions 示例：

```yaml
name: CI Build

on:
  push:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout code
      uses: actions/checkout@v2

    - name: Set up JDK
      uses: actions/setup-java@v2
      with:
        java-version: '11'

    - name: Build Project
      run: |
        # 官方构建命令示例
        <PLACEHOLDER_FOR_BUILD_COMMAND>
```

### 3. 处理签名密钥

为了确保构建的应用程序可以签名并上传，您需要通过 GitHub Secrets 来存储和管理您的签名密钥。请遵循以下步骤：

1. 在您的 GitHub 仓库中，前往 Settings > Secrets > Actions。
2. 创建新的 Secret，命名为 `SIGNING_KEY`，并粘贴您的签名密钥。

### 4. 在 MiWatchEmulator 和真实设备上测试

使用 MiWatchEmulator 进行测试，确保您的应用程序在模拟器上运行良好。对于真实设备，您需要将构建的 APK 文件安装并测试功能。 

### 5. 视频编码与文件大小注意事项

在编码视频时，请确保使用适当的比特率和分辨率，以避免文件过大。建议在满足质量要求的前提下，尽量压缩文件大小。 

如需进一步的指导和信息，请参考小米官方文档。
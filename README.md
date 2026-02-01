# VelaVideoPlayer (QuickApp for Mi Watch)

最小示例：在手表上播放内置视频或下载后播放临时文件。

运行/测试
1. 在仓库中打包的 Zip 中会包含一个示例视频 `Common/demo.mp4`（由 Actions 在构建时下载）。
2. 在 MiWatchEmulator / AstroBox / 真机上传并运行此 QuickApp。
3. 若要本地构建或打包，请使用你熟悉的 Vela/QuickApp 打包工具（示例项目不包含特定打包脚本）。

说明
- 内置视频路径：`/Common/demo.mp4`
- 下载示例使用：fetch.fetch({ responseType: 'file' })，返回的 res.data 可直接赋给 video 的 src。
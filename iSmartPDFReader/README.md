# iSmartPDFReader 1.2.0 — preview build 11 / 预览修复版

下载最新完整源码：[iSmartPDFReader-1.2.0-build11-source.zip](iSmartPDFReader-1.2.0-build11-source.zip)。解压后进入 `iSmartPDFReader` 文件夹查看 Swift 源码、Xcode 工程、测试、脚本与资源。许可：[MIT](LICENSE)。

Build 11 fixes normal streamed answers being rejected when network gateways omit or rewrite response format headers. Framing is validated from the actual response, HTML is rejected, and incomplete or quota-limited answers are not reported as complete. The native account connection has been verified online using a fixed synthetic question, without sending personal PDFs.

构建 11 修复了正常流式回答因缺少格式标记而提示“未收到流式回答”的问题。已使用账号和固定合成问题验证完成回答，未发送个人 PDF；同时补充了缺失标记、格式改写、网页、额度错误和中断内容的测试。

Full source: download and extract [iSmartPDFReader-1.2.0-build11-source.zip](iSmartPDFReader-1.2.0-build11-source.zip), then open the included `iSmartPDFReader` directory. The archive includes 88 reviewed source/resource files and no personal PDFs, credentials, caches or compiled apps. See [SOURCE_MANIFEST.json](SOURCE_MANIFEST.json) for file hashes and [PRIVACY.md](PRIVACY.md) for privacy details.

SHA-256: `f329fcad16dc934edb35850498f7f41a4622b692fd3d49a7208c4439753ca9ee`

This is a free, open-source app with native ChatGPT-account Q&A and the 页灵 (Page Sprite) companion. Account access and limits are controlled by OpenAI. The source license does not grant rights to third-party services. This source update does not announce App Store publication or approval.

这是免费开源的 PDF 阅读器，支持原生 ChatGPT 账号问答和页灵宠物。账号权限及额度由 OpenAI 决定。源码发布不代表 App Store 已上传、审核或发布。

After extraction, read `README.md`. Run offline checks with:

```sh
bash scripts/test-store.sh
bash scripts/test-local.sh
bash scripts/test-annotations.sh
```

The optional `scripts/check-live-connection.sh` sends only its fixed synthetic question through this app's own account. It does not read PDFs or chat history and does not refresh or replace credentials. Never share the account directory or its contents.

支持 / Contact: whkygl@163.com

# Chromium 和 Firefox 内核怎么选？

如果同一张商品图在两台电脑上的预览结果不同，可以先用 **「指纹浏览器」** 的 Windows 版留一组对照：固定页面地址和窗口宽度，记下浏览器版本。它的 Windows 客户端使用基于 Chromium 的 CEF；要判断问题是否也出现在 Firefox 上，还需用 Firefox 内核再做一次相同操作。

![指纹浏览器设备身份配置页](https://zwbrowser.com/images/desktop-guide-identity-light.webp)

## 产品名称、浏览器内核和设备标识分开记

AdsPower 的配置文档说明，SunBrowser 基于 Chrome，FlowerBrowser 基于 Firefox。新建环境时写下所选类型和具体版本。只改网页看到的浏览器标识，不能据此断定底层渲染引擎已经改变。[AdsPower 配置文档](https://help.adspower.com/docs/creating_browser_profiles)

![AdsPower产品展示](https://github.com/user-attachments/assets/d9cf60b3-2ea6-42e9-8a46-77ee610ea27f)

## 用一份网页验收单比较两个内核

| 页面任务 | 两边保持相同 | 分别记录 |
| --- | --- | --- |
| 网页排版 | 地址、窗口宽度和页面缩放 | 换行、滚动条、弹窗的位置 |
| 富文本编辑 | 相同文本和同一张示例图片 | 粘贴是否保留段落、图片能否预览 |
| 文件下载 | 同一份测试报表 | 下载是否开始、文件名是否正确 |
| 业务表单 | 普通成员角色、同一组测试数据 | 必填提示、日期选择、提交回执 |

每轮只调整一项。若只有一个内核出现差异，先用其当前受支持版本复核，再把版本号、操作步骤和页面截图一起交给网站维护者。若两边都失败，先查网站角色、输入数据或服务状态。

团队选默认内核时，可以用最高频的三项业务任务做决定；保留另一种内核作为兼容性验收样本。

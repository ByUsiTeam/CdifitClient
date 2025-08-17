# CdifitClient

这是一个基于移动端应用 `iApp` 开发的开源客户端软件，旨在为用户提供便捷的云端文件管理和视频播放功能。项目采用 MIT 开源协议，欢迎广大开发者参与贡献。

## [UML.md](UML.md)

## 项目特性
- **视频播放模块**：基于 WebView 实现视频播放器，支持 URL 输入、播放控制和全屏处理。
- **文件管理模块**：提供云端文件浏览功能，支持多种文件类型识别和操作（预览/下载）。
- **用户认证模块**：支持 Cookie 管理和验证码登录系统，确保用户账号安全。
- **动画工具类**：封装 Lottie 动画库，提供简洁的动画加载与控制接口。
- **系统工具类**：适配不同 Android 版本，优化状态栏和系统 UI。
- **网络工具类**：封装 HTTP 请求、JSON 解析和文件下载功能。
- **通知工具类**：提供统一的 Toast 和错误提示，支持定制化界面通知。

## 模块结构
- **主界面**：包含文件浏览器、侧边栏、刷新控件和广告区域。
- **视频播放界面**：提供视频播放器、URL 输入框、解析按钮和进度控制。
- **登录界面**：包含 Cookie 输入框、验证码区域和登录按钮。
- **侧边栏界面**：展示用户信息、存储策略、广告位和设置入口。

## 开发与运行环境
- 基于 iApp 开发框架
- Android 系统适配支持

## 贡献指南
欢迎提交 Issues 和 Pull Requests，帮助我们改进功能和性能。

## 许可协议
本项目采用 MIT 协议，分发时请注明原始项目地址。

## 基础特性
1. 基于移动端应用 `iApp` 开发的 **CdifitClient** 客户端软件
2. 采用 MIT 开源协议，分发时需注明原项目地址

## TERR
```tree
src//
├── Lottie.myu
├── StoragePolicySettings.iyu
├── View.myu
├── a.mjava
├── bfq2.iyu
├── byusi.myu
├── core.myu
├── dir.iyu
├── hlist.iyu
├── home.iyu
├── janz1.iyu
├── list.iyu
├── login.iyu
├── mian.iyu
├── music.iyu
├── picturePreview.iyu
├── sidebar.iyu
├── tw.myu
├── web.iyu
├── webView.mjava
└── window.iyu
res//
├── VideoPlayer2.zip
├── byusi/
│ ├── html/
│ │ ├── captcha.html
│ │ └── graphPreview.html
│ ├── logo/
│ │ ├── byusi.png
│ │ ├── cdifit.png
│ │ └── properos.png
│ └── resources/
│     ├── ApplicationUseIcon/
│     │ ├── ic_settings_application_and_service.png
│     │ └── ic_settings_privacy.png
│     ├── Lottie/
│     │ ├── 0.005020299610974055.json
│     │ ├── 0.json
│     │ ├── 1.json
│     │ ├── 2.json
│     │ ├── 3.json
│     │ ├── 4.json
│     │ ├── 404.json
│     │ ├── 5.json
│     │ ├── 6.json
│     │ ├── ByUsi/
│     │ │ ├── 404.json
│     │ │ ├── accomplish.json
│     │ │ ├── ai.json
│     │ │ ├── loading.json
│     │ │ └── loading2.json
│     │ ├── app.json
│     │ ├── complete.json
│     │ ├── error.json
│     │ ├── file.json
│     │ ├── gome.json
│     │ ├── home.json
│     │ ├── list.json
│     │ ├── loading.json
│     │ ├── message.json
│     │ ├── message1.json
│     │ ├── my.json
│     │ ├── ok.json
│     │ ├── rocket.json
│     │ ├── thecharts.json
│     │ ├── true.json
│     │ ├── yes.json
│     │ ├── 中国国旗.json
│     │ ├── 人物.json
│     │ ├── 图标运动图形2.json
│     │ ├── 屏幕02洛蒂导出.json
│     │ ├── 提醒铃铛.json
│     │ ├── 文件夹下载.json
│     │ ├── 星球.json
│     │ ├── 现金流的骨架.json
│     │ ├── 菜单开关.json
│     │ ├── 跑2圈.json
│     │ ├── 骨架骨骼动画.json
│     │ └── 骷髅卡•愿望列表网格.json
│     ├── icon/
│     │ ├── file-earmark.png
│     │ ├── file-pdf.png
│     │ ├── filetype-aac.svg
│     │ ├── filetype-ai.svg
│     │ ├── filetype-bmp.svg
│     │ ├── filetype-cs.svg
│     │ ├── filetype-css.png
│     │ ├── filetype-csv.svg
│     │ ├── filetype-doc.png
│     │ ├── filetype-docx.png
│     │ ├── filetype-exe.png
│     │ ├── filetype-gif.png
│     │ ├── filetype-heic.svg
│     │ ├── filetype-html.png
│     │ ├── filetype-jpg.png
│     │ ├── filetype-js.svg
│     │ ├── filetype-json.svg
│     │ ├── filetype-jsx.svg
│     │ ├── filetype-key.svg
│     │ ├── filetype-m4p.svg
│     │ ├── filetype-md.png
│     │ ├── filetype-mdx.svg
│     │ ├── filetype-mov.svg
│     │ ├── filetype-mp3.png
│     │ ├── filetype-mp4.png
│     │ ├── filetype-otf.svg
│     │ ├── filetype-php.svg
│     │ ├── filetype-ppt.svg
│     │ ├── filetype-pptx.svg
│     │ ├── filetype-psd.svg
│     │ ├── filetype-py.png
│     │ ├── filetype-raw.svg
│     │ ├── filetype-rb.svg
│     │ ├── filetype-sass.svg
│     │ ├── filetype-scss.svg
│     │ ├── filetype-sh.svg
│     │ ├── filetype-sql.svg
│     │ ├── filetype-svg.svg
│     │ ├── filetype-tiff.svg
│     │ ├── filetype-tsx.svg
│     │ ├── filetype-ttf.svg
│     │ ├── filetype-txt.svg
│     │ ├── filetype-wav.svg
│     │ ├── filetype-woff.svg
│     │ ├── filetype-xls.svg
│     │ ├── filetype-xlsx.svg
│     │ ├── filetype-xml.png
│     │ ├── filetype-yml.png
│     │ ├── folder.png
│     │ └── music-note-beamed.png
│     ├── template/
│     │ └── json/
│     │     ├── StoragePolicySwitching.json
│     │     ├── login_information.json
│     │     ├── picturePreview.json
│     │     └── share.json
│     └── ttf/
│         ├── 001hh1.ttf
│         ├── acbt80.ttf
│         ├── bb2325.ttf
│         ├── z_c.TTF
│         ├── z_x.TTF
│         └── zt.TTF
├── sdk/
│ └── player.bysi.sdk
├── ts0.png
├── ts1.png
├── ts2.png
├── tw/
│ └── twtb.png
└── wallpaper/
    └── DefaultWallpaper_1.png

16 directories, 137 files
```


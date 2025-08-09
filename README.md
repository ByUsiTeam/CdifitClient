# CdifitClient

## [UML.md](UML.md)
```mermaid
classDiagram
    direction LR
    
    %% 核心功能模块
    class 视频播放模块 {
        +WebView 播放器
        +EditText URL输入框
        +解析视频功能
        +播放控制逻辑
        +全屏处理
    }
    
    class 文件管理模块 {
        +RecyclerView 文件列表
        +目录浏览功能
        +文件类型识别
        +文件操作(预览/下载)
        +存储策略管理
    }
    
    class 用户认证模块 {
        +Cookie 管理
        +登录表单
        +验证码系统
        +Cookie 写入/读取
    }
    
    %% 工具类
    class 动画工具类 {
        +Lottie 动画加载
        +设置动画属性
        +控制动画播放
    }
    
    class 系统工具类 {
        +状态栏控制
        +Android 版本适配
        +系统UI优化
    }
    
    class 网络工具类 {
        +HTTP请求封装
        +JSON解析
        +文件下载
    }
    
    class 通知工具类 {
        +Toast通知
        +定制化提示
        +错误提示
    }
    
    %% 业务逻辑
    class 核心业务逻辑 {
        +目录加载
        +文件操作处理
        +页面导航
        +广告处理
        +分享功能
    }
    
    %% 界面组件
    class 主界面 {
        +文件浏览器
        +侧边栏
        +刷新控件
        +广告区域
    }
    
    class 视频播放界面 {
        +视频播放器
        +URL输入
        +解析按钮
        +进度控制
    }
    
    class 登录界面 {
        +Cookie输入框
        +验证码区域
        +登录按钮
    }
    
    class 侧边栏界面 {
        +用户信息
        +存储策略
        +广告位
        +设置入口
    }
    
    %% 关系定义
    主界面 --> 核心业务逻辑 : 调用
    视频播放界面 --> 动画工具类 : 使用
    登录界面 --> 网络工具类 : 使用
    核心业务逻辑 --> 文件管理模块 : 包含
    核心业务逻辑 --> 系统工具类 : 依赖
    核心业务逻辑 --> 网络工具类 : 使用
    文件管理模块 --> 视频播放模块 : 打开
    侧边栏界面 --> 用户认证模块 : 管理
    
    %% 注释说明
    note for 视频播放模块 "基于WebView的视频播放器\n支持URL输入和解析功能"
    note for 文件管理模块 "实现云端文件浏览\n支持多种文件类型操作"
    note for 用户认证模块 "基于Cookie的认证系统\n支持验证码功能"
    note for 动画工具类 "封装Lottie动画库\n提供简化调用接口"
    note for 系统工具类 "处理Android系统适配\n包括状态栏和UI优化"
```

## 基础特性
1. 基于移动端应用 `iApp` 开发的 **CdifitClient** 客户端软件
2. 采用 MIT 开源协议，分发时需注明原项目地址

## TERR
```tree
./
├── AndroidManifest.xml
├── JiYU.mtsx
├── LICENSE
├── README.md
├── UML.md
├── apk/
│ ├── assets/
│ │ └── extra_conf1g.xml
│ └── lib/
│     ├── Lottiesx
│     ├── ts.dex.i
│     └── tw
├── app_webview/
│ ├── BrowserMetrics-spare.pma
│ ├── Default/
│ │ ├── Cookies
│ │ ├── Cookies-journal
│ │ ├── Local Storage/
│ │ │ └── leveldb/
│ │ │     ├── 000004.log
│ │ │     ├── 000005.ldb
│ │ │     ├── CURRENT
│ │ │     ├── LOCK
│ │ │     ├── LOG
│ │ │     └── MANIFEST-000001
│ │ ├── PersistentOriginTrials/
│ │ │ ├── LOCK
│ │ │ └── LOG
│ │ ├── Service Worker/
│ │ │ ├── Database/
│ │ │ │ ├── 000003.log
│ │ │ │ ├── CURRENT
│ │ │ │ ├── LOCK
│ │ │ │ ├── LOG
│ │ │ │ └── MANIFEST-000001
│ │ │ └── ScriptCache/
│ │ │     ├── index
│ │ │     └── index-dir/
│ │ │         └── the-real-index
│ │ ├── Session Storage/
│ │ │ ├── 000003.log
│ │ │ ├── CURRENT
│ │ │ ├── LOCK
│ │ │ ├── LOG
│ │ │ └── MANIFEST-000001
│ │ ├── Shared Dictionary/
│ │ │ ├── cache/
│ │ │ │ ├── index
│ │ │ │ └── index-dir/
│ │ │ │     └── the-real-index
│ │ │ ├── db
│ │ │ └── db-journal
│ │ ├── Web Data-journal
│ │ ├── Web-Data
│ │ ├── WebStorage/
│ │ │ ├── QuotaManager
│ │ │ └── QuotaManager-journal
│ │ ├── blob_storage/
│ │ │ └── 714156d8-99a3-48b3-986d-d904a9c2a971/
│ │ └── shared_proto_db/
│ │     ├── 000003.log
│ │     ├── CURRENT
│ │     ├── LOCK
│ │     ├── LOG
│ │     ├── MANIFEST-000001
│ │     └── metadata/
│ │         ├── 000003.log
│ │         ├── CURRENT
│ │         ├── LOCK
│ │         ├── LOG
│ │         └── MANIFEST-000001
│ ├── last-exit-info
│ ├── pref_store
│ ├── variations_seed_new
│ ├── variations_stamp
│ └── webview_data.lock
├── bin/
│ └── CdifitClient_0.1.16_dp.Apk
├── docs/
├── files/
│ ├── ByUsi/
│ │ ├── Cdifit/
│ │ │ └── ggao.html
│ │ └── Config.json
│ ├── System/
│ │ ├── Config/
│ │ │ └── sidebar
│ │ ├── Cookie
│ │ ├── ResourceLinkCache/
│ │ │ └── DWkqil
│ │ └── homeList.json
│ └── temp/
│     ├── VideoPlayer2/
│     │ ├── artplayer.css
│     │ ├── artplayer.js
│     │ ├── flv.js
│     │ ├── hls.js
│     │ ├── index.htm
│     │ └── res/
│     │     ├── background.jpg
│     │     ├── indicator.svg
│     │     ├── load.gif
│     │     ├── ploading.gif
│     │     └── state.svg
│     ├── ad.html
│     ├── cca.html
│     └── clickAdvertisement
├── icon.png
├── res/
│ ├── VideoPlayer2.zip
│ ├── byusi/
│ │ ├── html/
│ │ │ ├── captcha.html
│ │ │ └── graphPreview.html
│ │ ├── logo/
│ │ │ ├── byusi.png
│ │ │ ├── cdifit.png
│ │ │ └── properos.png
│ │ └── resources/
│ │     ├── ApplicationUseIcon/
│ │     │ ├── ic_settings_application_and_service.png
│ │     │ └── ic_settings_privacy.png
│ │     ├── Lottie/
│ │     │ ├── 0.005020299610974055.json
│ │     │ ├── 0.json
│ │     │ ├── 1.json
│ │     │ ├── 2.json
│ │     │ ├── 3.json
│ │     │ ├── 4.json
│ │     │ ├── 404.json
│ │     │ ├── 5.json
│ │     │ ├── 6.json
│ │     │ ├── ByUsi/
│ │     │ │ ├── 404.json
│ │     │ │ ├── accomplish.json
│ │     │ │ ├── ai.json
│ │     │ │ ├── loading.json
│ │     │ │ └── loading2.json
│ │     │ ├── app.json
│ │     │ ├── complete.json
│ │     │ ├── error.json
│ │     │ ├── file.json
│ │     │ ├── gome.json
│ │     │ ├── home.json
│ │     │ ├── list.json
│ │     │ ├── loading.json
│ │     │ ├── message.json
│ │     │ ├── message1.json
│ │     │ ├── my.json
│ │     │ ├── ok.json
│ │     │ ├── rocket.json
│ │     │ ├── thecharts.json
│ │     │ ├── true.json
│ │     │ ├── yes.json
│ │     │ ├── 中国国旗.json
│ │     │ ├── 人物.json
│ │     │ ├── 图标运动图形2.json
│ │     │ ├── 屏幕02洛蒂导出.json
│ │     │ ├── 提醒铃铛.json
│ │     │ ├── 文件夹下载.json
│ │     │ ├── 星球.json
│ │     │ ├── 现金流的骨架.json
│ │     │ ├── 菜单开关.json
│ │     │ ├── 跑2圈.json
│ │     │ ├── 骨架骨骼动画.json
│ │     │ └── 骷髅卡•愿望列表网格.json
│ │     ├── icon/
│ │     │ ├── file-earmark.png
│ │     │ ├── file-pdf.png
│ │     │ ├── filetype-aac.svg
│ │     │ ├── filetype-ai.svg
│ │     │ ├── filetype-bmp.svg
│ │     │ ├── filetype-cs.svg
│ │     │ ├── filetype-css.png
│ │     │ ├── filetype-csv.svg
│ │     │ ├── filetype-doc.png
│ │     │ ├── filetype-docx.png
│ │     │ ├── filetype-exe.png
│ │     │ ├── filetype-gif.png
│ │     │ ├── filetype-heic.svg
│ │     │ ├── filetype-html.png
│ │     │ ├── filetype-jpg.png
│ │     │ ├── filetype-js.svg
│ │     │ ├── filetype-json.svg
│ │     │ ├── filetype-jsx.svg
│ │     │ ├── filetype-key.svg
│ │     │ ├── filetype-m4p.svg
│ │     │ ├── filetype-md.png
│ │     │ ├── filetype-mdx.svg
│ │     │ ├── filetype-mov.svg
│ │     │ ├── filetype-mp3.png
│ │     │ ├── filetype-mp4.png
│ │     │ ├── filetype-otf.svg
│ │     │ ├── filetype-php.svg
│ │     │ ├── filetype-ppt.svg
│ │     │ ├── filetype-pptx.svg
│ │     │ ├── filetype-psd.svg
│ │     │ ├── filetype-py.png
│ │     │ ├── filetype-raw.svg
│ │     │ ├── filetype-rb.svg
│ │     │ ├── filetype-sass.svg
│ │     │ ├── filetype-scss.svg
│ │     │ ├── filetype-sh.svg
│ │     │ ├── filetype-sql.svg
│ │     │ ├── filetype-svg.svg
│ │     │ ├── filetype-tiff.svg
│ │     │ ├── filetype-tsx.svg
│ │     │ ├── filetype-ttf.svg
│ │     │ ├── filetype-txt.svg
│ │     │ ├── filetype-wav.svg
│ │     │ ├── filetype-woff.svg
│ │     │ ├── filetype-xls.svg
│ │     │ ├── filetype-xlsx.svg
│ │     │ ├── filetype-xml.png
│ │     │ ├── filetype-yml.png
│ │     │ ├── folder.png
│ │     │ └── music-note-beamed.png
│ │     ├── template/
│ │     │ └── json/
│ │     │     ├── StoragePolicySwitching.json
│ │     │     ├── login_information.json
│ │     │     ├── picturePreview.json
│ │     │     └── share.json
│ │     └── ttf/
│ │         ├── 001hh1.ttf
│ │         ├── acbt80.ttf
│ │         ├── bb2325.ttf
│ │         ├── z_c.TTF
│ │         ├── z_x.TTF
│ │         └── zt.TTF
│ ├── sdk/
│ │ └── player.bysi.sdk
│ ├── ts0.png
│ ├── ts1.png
│ ├── ts2.png
│ ├── tw/
│ │ └── twtb.png
│ └── wallpaper/
│     └── DefaultWallpaper_1.png
└── src/
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

49 directories, 213 files
```
# iOS 参考

## 常见入口

- `*.xcodeproj` / `*.xcworkspace`
- `Package.swift`
- `Info.plist`
- `Assets.xcassets`
- `AppDelegate`
- `SceneDelegate`
- `UIViewController`
- `SwiftUI View`
- `Tests/`

## 推荐工具

- Xcode
- iOS Simulator
- `xcodebuild`
- `swift package`
- XCTest
- Instruments
- OSLog / Console
- `simctl`
- `xcrun`

## 常用检查

- 编译是否通过
- 测试是否通过
- UI 是否遵守安全区域
- 是否有主线程 UI 更新问题
- 是否存在 retain cycle / 资源未释放
- 是否处理了权限、签名、Capabilities、深链、通知等平台问题

## 调试优先级

1. 先看报错和堆栈
2. 再看当前页面/状态流
3. 再看工程配置、签名和依赖
4. 最后才考虑重构

## 常见命令

```bash
xcodebuild -showBuildSettings -scheme <Scheme>
xcodebuild -list
xcodebuild build -scheme <Scheme> -destination 'platform=iOS Simulator,name=iPhone 15'
xcodebuild test -scheme <Scheme> -destination 'platform=iOS Simulator,name=iPhone 15'
swift package resolve
swift test
xcrun simctl list devices
xcrun simctl boot "iPhone 15"
```

## iOS 细节提醒

- SwiftUI 优先保持状态单向流动
- UIKit 注意生命周期、代理、通知和释放
- 网络请求要处理 loading、error、retry
- 图片、字体、颜色优先走项目资源和常量
- UI 适配优先用系统布局能力，不要硬编码固定尺寸

## 验证重点

- 首屏渲染
- 页面切换
- 键盘与输入框
- 深色模式与无障碍
- 横竖屏与不同尺寸设备
- 崩溃、卡顿、内存泄漏
- 构建配置、签名、依赖解析
- 模拟器和真机结果是否一致
- 关键页面是否可重复进入和退出

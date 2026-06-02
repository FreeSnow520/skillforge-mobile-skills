---
name: "ios-development"
description: "面向 iOS 开发的技能：当用户提到 Swift、SwiftUI、UIKit、Xcode、模拟器、XCTest、Instruments、SPM、App Store、Widget、推送、性能、崩溃或 iPhone/iPad 原生开发时使用。默认只依赖免费、本地或官方工具。"
metadata:
  last_modified: "2026-05-28"
---

# iOS 开发

## 什么时候使用

当任务与 iPhone / iPad 原生开发有关时使用，尤其是：

- Swift / SwiftUI / UIKit
- Xcode 工程、依赖、签名、构建、测试
- 模拟器、真机调试、Instruments、崩溃、内存、卡顿
- 页面实现、交互、适配、安全区域、无障碍
- App 发布前检查、功能回归、性能排查

### 典型任务

- 写一个 SwiftUI 页面或 UIKit 页面
- 修复编译报错、签名报错、依赖冲突
- 排查卡顿、内存泄漏、启动慢、崩溃
- 调整安全区域、键盘、旋转、深色模式
- 补单测、补埋点、补无障碍支持

### 常见触发词

- `SwiftUI`
- `UIKit`
- `Xcode`
- `xcodebuild`
- `Simulator`
- `Instruments`
- `XCTest`
- `SPM`
- `App Store`
- `崩溃`
- `卡顿`
- `内存泄漏`

## 默认原则

- 先看当前工程结构，再决定改动方案
- 优先最小改动，避免重构式修复
- 默认只用免费、官方、本地或开源工具
- 不保留不可调用或需要付费的外部能力
- 发现需求模糊时，先把可验证的范围锁定

## 推荐工作流

1. 确认任务类型：新功能、bug 修复、性能优化、发布问题、兼容性问题
2. 识别项目技术栈：SwiftUI、UIKit、混合、SPM、CocoaPods、XCFramework
3. 找到入口文件、相关视图、状态源、服务层和测试
4. 先检查项目现有约束，再开始改动
5. 实现后用项目已有方式验证：编译、单测、模拟器、真机或 Instruments
6. 输出变更文件和回归点

## 工具优先级

- 构建与测试：`xcodebuild`、`swift test`
- 依赖管理：`swift package`
- 运行与调试：Xcode、iOS Simulator、Instruments、Console
- 问题排查：日志、断点、主线程检查、资源释放检查

## 参考资料

- [通用移动开发工作流](../_shared/common-mobile-workflow.md)
- [iOS 参考](../_shared/ios-reference.md)

## 快速判断

如果任务同时涉及“界面 + 状态 + 工程构建”，优先按这条线处理：

1. 先定位工程入口和相关 View
2. 再看状态与数据流
3. 再看构建、签名、测试与设备差异
4. 最后再考虑做不做抽象优化

## 输出要求

- 说明改了哪些文件
- 说明为什么这么改
- 说明验证方法和回归点
- 如果涉及 UI，说明关键适配点和设备差异

## 常见关注点

- 主线程与异步回调
- retain cycle、资源释放、观察者注销
- 安全区域、键盘、布局压缩与拉伸
- 权限、签名、Capabilities、推送、深链
- 本地化、颜色、字体、资源目录
- 预览和真机结果不一致
- `SPM` / `Pods` / `XCFramework` 版本兼容

## 不要做的事

- 不要依赖付费或不可调用的云服务
- 不要为了排错而引入新的通用路由器
- 不要跳过构建或测试验证
- 不要把问题只修在表层，而不看根因

## 示例提示词

- `修复这个 SwiftUI 页面在 iPhone SE 上按钮被遮住的问题`
- `帮我排查这个 Xcode 编译报错，顺便给出最小修复方案`
- `这个列表滚动很卡，帮我按 Instruments 的思路排查`
- `帮我看一下这个 UIKit 页面有没有 retain cycle 风险`
- `补一个 XCTest 覆盖登录成功和失败两种路径`

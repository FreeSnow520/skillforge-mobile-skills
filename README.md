# SkillForge

> iOS 开发 + 微信小程序开发的双技能包，外加一层很薄的共享工作流模板。

SkillForge 现在不是通用模板集，也不是技能生成器，而是一个面向移动开发的成品 Skills 仓库：

- `ios-development`
- `wechat-mini-program-development`

两者共享一组轻量参考资料，强调本地可执行、免费可用、可验证的开发流程。
共享层只负责模板化工作流，不负责自动分流或泛化路由。

## 你会得到什么

- 一个面向 iOS 的完整开发技能
- 一个面向微信小程序的完整开发技能
- 一组共用的移动开发工作流参考
- 一套可直接复制到技能目录中的目录结构

## 目录结构

```text
skills/
├── _shared/
│   ├── common-mobile-workflow.md
│   ├── ios-reference.md
│   └── wechat-mini-program-reference.md
├── ios-development/
│   └── SKILL.md
└── wechat-mini-program-development/
    └── SKILL.md
```

## 快速上手

### 1. 复制到你的技能目录

```bash
cp -r skills ~/.codex/skills/skillforge
```

如果你的环境使用的是别的技能目录，把 `skills/` 复制到对应位置即可。

### 2. 直接引用技能名

```text
请使用 ios-development 处理这个 SwiftUI 页面
请使用 wechat-mini-program-development 修复这个小程序表单
```

### 3. 按领域执行

#### `ios-development`

适合这些任务：

- Swift / SwiftUI / UIKit 开发
- Xcode 工程、`xcodebuild`、`swift package`
- iPhone / iPad 兼容性、调试、性能、崩溃、内存问题
- XCTest、Instruments、模拟器、自测与发布前检查

#### `wechat-mini-program-development`

适合这些任务：

- 微信小程序页面、组件、生命周期、状态与数据流
- `WXML` / `WXSS` / `JS` / `TS` / `JSON`
- 微信开发者工具、预览、真机调试、打包、上传
- 接口联调、性能优化、兼容性与发布前检查

## 触发词示例

### iOS

- `SwiftUI 页面`
- `UIKit 改造`
- `Xcode 编译失败`
- `模拟器崩溃`
- `Instruments 卡顿`
- `SPM 依赖`

### 微信小程序

- `微信小程序页面`
- `setData 过大`
- `预览失败`
- `真机白屏`
- `上传报错`
- `基础库兼容`

## 示例提示词

### iOS

- `请使用 ios-development 修复这个 SwiftUI 页面在小屏机型上的布局问题`
- `请使用 ios-development 排查这个 Xcode 编译失败`
- `请使用 ios-development 看一下这个页面为什么在 Instruments 里卡顿`
- `请使用 ios-development 帮我看一下这个 UIKit 页面有没有 retain cycle 风险`
- `请使用 ios-development 补一个 XCTest 覆盖登录成功和失败两种路径`

### 微信小程序

- `请使用 wechat-mini-program-development 修复这个小程序表单提交失败`
- `请使用 wechat-mini-program-development 排查真机白屏问题`
- `请使用 wechat-mini-program-development 优化这个列表的 setData 频率`
- `请使用 wechat-mini-program-development 帮我补一个登录授权和用户信息获取流程`
- `请使用 wechat-mini-program-development 把这个组件拆一下，避免页面里堆太多状态`

## 能力边界

### 适合做

- 领域化开发流程
- 代码实现与 bug 修复
- 构建、调试、性能、发布前检查
- 可验证的最小改动
- 本地 / 官方 / 免费 / 开源工具优先

### 不适合做

- 通用路由器
- 泛化技能生成器
- 依赖付费或不可调用服务的流程
- 需要复杂平台编排但仓库里没有对应工具链的场景

## 发布前检查

1. `skills/` 下只保留目标技能和 `_shared/`
2. 每个 `SKILL.md` 的 frontmatter 都能准确触发
3. 技能描述里没有残留付费服务、不可调用链接或通用路由语义
4. 示例提示词覆盖你最常见的真实任务
5. README 能让别人三分钟内看懂怎么用

## 设计原则

1. **只保留能直接执行的技能**
2. **默认使用免费、本地、开源或官方工具**
3. **不保留不可调用或依赖付费服务的流程**
4. **每个技能都保持短、准、可触发**
5. **共享层只做模板化流程，不做泛化路由**

## 备注

如果你还想继续扩展，可以在 `_shared/` 里继续补充面向移动开发的共用参考，但不要把仓库重新做回通用路由器。
这套结构的目标是：**技能负责领域，_shared 负责模板化流程**。

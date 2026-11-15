# 光逝 / Fading Light

一个用 Unreal Engine 5.8 制作的短篇恐怖游戏，通关约 10-15 分钟。

> 推开门的那一刻，灯灭了。

<img width="580" height="380" alt="screenshot-03" src="https://github.com/user-attachments/assets/940dbfe5-598f-4199-a8c6-27f0a2375116" />
<img width="580" height="380" alt="screenshot-02" src="https://github.com/user-attachments/assets/28c8f2bf-c4b2-4ba5-a870-7b88771a5842" />
<img width="580" height="380" alt="screenshot-01" src="https://github.com/user-attachments/assets/2b8bb246-a7c1-487b-b05e-45c798b06cbf" />

---

## 关于

玩家在一条陌生的走廊里醒来，尽头有一盏灯，墙边贴着规则。

推开门之后，光消失了，你只能靠手电看清脚下一小块地方。

墙上的规则说：**不要回头**。

这个游戏的核心不是操作，是判断——**哪一条规则是真的**。

## 下载

**百度网盘**：https://pan.baidu.com/s/1MuvXbSG_lEjdEygzCVzGGQ?pwd=89XK
**提取码**：`89XK`

下载后解压，双击 `HorrorTest.exe`。首次启动较慢，请等待。

## 操作

| 按键 | 功能 |
|---|---|
| W A S D | 移动 |
| 鼠标 | 视角 |
| E | 交互 / 开门 / 拾取 |
| G | 开关手电 |
| Space | 跳跃 |
| Esc | 暂停 |

## 技术信息

| 项 | 值 |
|---|---|
| 引擎 | Unreal Engine 5.8.3 |
| 实现方式 | 纯蓝图（无 C++ 代码） |
| 关卡 | World Partition，单关卡多区域换景 |
| 输入 | Enhanced Input |
| 打包体积 | 316 MB |
| 目标平台 | Windows x64 / DirectX 12 |
| 渲染 | 未使用 Nanite / Lumen，静态光照 |

## 工程结构

```
Content/
├─ BP/            交互物、触发器、门、角色相关蓝图
├─ BPI/           蓝图接口（Interactable）
├─ Input/         Enhanced Input 资产（IA / IMC）
├─ UI/            控件蓝图（主菜单、暂停、纸条、提示、结局）
├─ Audio/         环境音与音效
├─ Fonts/         规则牌材质与纹理
└─ FirstPerson/   主关卡 Lvl_FirstPerson
```

## 本地构建

1. 安装 Unreal Engine 5.8
2. 双击 `HorrorTest.uproject`
3. 首次打开会编译着色器，需要几分钟
4. 打包：平台 → Windows → 打包项目

需要 Visual Studio 2022/2026 的「使用 C++ 的桌面开发」工作负载与 Windows SDK（即使项目是纯蓝图，打包流程也会校验工具链）。

## 已知限制

- 无存档系统，单次通关
- 仅支持 Windows / DX12，无 DX11 回退
- 无手柄支持
- exe 无数字签名，首次运行可能被 Windows「智能应用控制」拦截，属正常现象

## 许可

游戏本体遵循 [Unreal Engine EULA](https://www.unrealengine.com/eula)。

自制内容（蓝图、关卡、UI、音效编排）可自由参考学习，转载请注明出处。

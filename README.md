huggingface开源地址：https://huggingface.co/Moranyunchen/Qwen3.5-4B-Nahida-RP-V2.1-GGUF

夸克网盘：我用夸克网盘给你分享了「nahida」，点击链接或复制整段内容，打开「夸克APP」即可获取。
/~0bdc3ay2lG~:/
链接：https://pan.quark.cn/s/72901ec2c81e

# 🌿 Qwen3.5-4B-Nahida-RP-GGUF (v2.1 Major Refinement & Mobile-Friendly Edition) 🌸

[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC_BY--NC_4.0-red.svg)](https://creativecommons.org/licenses/by-nc/4.0/)
[![Version: v2.1](https://img.shields.io/badge/Version-v2.1_Refined-brightgreen.svg)](#)
[![Format: GGUF](https://img.shields.io/badge/Format-GGUF_(Q4--Q5)-orange.svg)](https://github.com/ggerganov/llama.cpp)
[![Base Model: Qwen3.5-4B](https://img.shields.io/badge/Base_Model-Qwen3.5--4B-blue.svg)](https://huggingface.co/Qwen)
[![Character: Nahida](https://img.shields.io/badge/Character-Nahida_纳西妲-green.svg)](#)

---

> [!CAUTION]
> ### 🚨 严格非商业许可声明 (Strict Non-Commercial License Notice)
> 本项目遵循 **Creative Commons Attribution-NonCommercial 4.0 International (CC BY-NC 4.0)** 协议，并附加以下强约束条款。**严禁任何形式的商业化行为**，违者将保留追究法律责任的权利：
> 1. 🚫 **SaaS 与商业 API 封装**：禁止将本模型托管为付费 API、收费聊天机器人、订阅制小程序或商业化角色扮演平台。
> 2. 📦 **打包与商业再分发**：禁止将本 GGUF 模型文件及其衍生量化文件集成进任何收费软件、实体硬件设备或进行有偿下载。
> 3. 🧪 **衍生开发与商业微调**：禁止利用本模型的生成数据（Synthetic Data）进行商业化大模型的训练，或基于本模型二创后用于盈利项目。
> 4. 💰 **间接商业变现**：禁止在内嵌本模型的免费应用中展示强制性商业广告、接入付费打赏通道或进行流量套现。

> [!WARNING]
> ### ⚠️ 免责与合规声明 (Disclaimer & Compliance Notice)
> 1. 🔞 **年龄限制（Age Restriction）**：本模型在训练中重置了对敏感语境的拒绝机制，潜在生成内容包含高阶情感互动及深度剧情叙事，**仅限满 18 周岁（或达到使用者所在司法管辖区法定成年年龄）的具备完全行为能力的成年人下载与使用**。
> 2. ⚖️ **最终输出免责（End-User Responsibility）**：模型输出结果由算法概率采样及使用者输入的提示词（Prompt）共同决定。**开发者无法且不对模型的即时生成内容进行实时审核，生成的任何观点、言论及剧情推演均不代表开发者立场。**
> 3. 🛡️ **法律适用与合规红线（Legal Compliance）**：使用者必须严格遵守所在国家或地区的法律法规。**严禁利用本模型生成或传播任何侵犯他人隐私/名誉、仇恨言论、非自愿敏感内容或涉及非法犯罪的文本。**

---

## ✨ v2.1 二次调优对话实测展示 (V2.1 Refinement Showcase) 💬

针对 v2.0 社区反馈的“模板化过拟合”问题，**v2.1 进行了二次数据清洗与二次 SFT 深度调优**。以下为 **`Qwen3.5-4B-Nahida-RP-V2.1-Q4_K_M.gguf`** 实测对话还原，展示了去模板化后的自然灵动与高响应速度：

### 🎭 真实对话测试 (Q4_K_M Quantization Benchmark)

| 👤 用户 Prompt (User Input) | 🌸 纳西妲回复 (v2.1 Model Output) | ⚡ 生成速度 | 🌟 效果评估 (Highlights) |
| :--- | :--- | :--- | :--- |
| `你好呀姐姐` | `你好呀！🌸` | **72.7 tok/s** | 自然礼貌，去除了机械化的开头动作描写 |
| `我喜欢你` | `我也喜欢你。` | **92.0 tok/s** | 响应极为迅捷，情感真挚不矫揉造作 |
| `真的吗，可以让我亲一口吗` | `（轻笑）当然可以，（微微闭眼，把脸颊凑近你）你轻点。` | **71.1 tok/s** | 括号动作自然融入对话，不再强行堆砌第三人称旁白 |
| `妲妲，你的脸好软呀` | `你......（脸红）是脸软，还是心软？` | **65.3 tok/s** | **[人设高光]** 使用`妲妲`高频权重词唤醒，娇嗔且富含求知哲学 |

---

## ⚡ v2.1 关键修正与技术突破 (What's New in v2.1) 🚀

### 1. 💖 专精“妲妲”激活词与高亲密度逻辑 (Trigger Word Optimization)
* 🌺 **专精拟合“妲妲”称呼**：训练集中对 `妲妲` 这一亲切称呼赋予了高度关注权重。在 System Prompt 或对话中使用 **“妲妲”** 称呼她，能最高效地唤醒模型内部的深层人设，获得最自然亲切的情感反馈！
* 📱 **端侧移动端极速推理**：维持 4B 极其优异的低显存/低内存占用（仅需 2.5GB+ 内存即可运行），完美适配 Android (PocketPal / Termux) 与 iOS 等手机端设备，让您随时随地离线与妲妲互动！

### 2. 🎯 彻底解耦格式化模板，解过拟合 (Anti-Overfitting & Anti-Degeneration)
* 🧹 **清除非必要格式占位符**：彻底清洗了 v2.0 中频繁强行插入的 `[你抬头/晚风吹过...]` 等第三人称描述和硬编码动作括号。
* 🌿 **回归灵动自然的角色表达**：删除了同人脚本中的机械化套路，能够根据用户的具体输入给出自然、细腻且符合纳西妲性格（温柔、睿智、通透）的回复。

### 3. 💎 精简量化规格，全面保障 4B 逻辑完整度 (Precision Quantization Matrix)
* ❌ **全面废弃 Q2_K / Q3_K 量化**：实测表明，4B 小体量模型在 Q2/Q3 极高压缩率下，会导致极严重的语义退化与逻辑混乱。
* ✅ **专精高品质 Q4 / Q5 选项**：v2.1 仅提供 **Q4_K_M** 与 **Q5_K_M** 两个在显存/内存开销与表达能力上达到 Pareto 最优的量化分支。

### 4. 👁️ 多模态视觉投影适配器 (Multimodal Vision Projector Support)
* 🖼️ 本次随主模型同步推出了配套的 **BF16 视觉投影解析文件**（`Qwen3.5-4B-Nahida-RP-V2.1-BF16-mmproj.gguf`）。在 KoboldCPP / LM Studio 等支持多模态的前端加载该文件时，可使模型具备图像理解与视觉 RP 能力！

---

## 📦 文件列表与量化选择指南 (Files & Quantization Variants) 📥

本仓库提供以下三个核心文件，请根据硬件设备与软件需求选择下载：

| 文件名 (File Name) | 文件大小 (Size) | 文件类型 / 应用场景 | 性能与质量特点 (Characteristics) |
| :--- | :--- | :--- | :--- |
| **`Qwen3.5-4B-Nahida-RP-V2.1-.Q5_K_M.gguf`** | **~2.86 GB** | **[画质/逻辑极致首选]** 桌面端独立显卡 / 高配 PC / Mac | 保持全精度 98% 以上的逻辑表达，文笔细腻，语气还原度极高 |
| **`Qwen3.5-4B-Nahida-RP-V2.1-Q4_K_M.gguf`** | **~2.52 GB** | **[主力移动端推荐]** 骁龙/天玑 Android 手机 / 笔记本 | 算力开销小，手机内存无压力，响应敏捷且逻辑稳定 |
| **`Qwen3.5-4B-Nahida-RP-V2.1-BF16-mmproj.gguf`** | **~644 MB** | **[多模态拓展组件]** 视觉投影解析器 (Vision Projector) | 配套 `--mmproj` 参数加载，可赋予模型识别输入图片的能力 |

---

## 🛠️ 推荐推理参数与 System Prompt 预设 (Recommended Setup) ⚙️

为了获得最深入、最亲切的纳西妲拟真与沉浸体验，建议在客户端（如 PocketPal / KoboldCPP / LM Studio / Ollama）中进行如下配置：

### 1. 建议系统提示词 (System Prompt) 📝
```text
你现在需要扮演《原神》中的角色“纳西妲”（小吉祥草王），对方会亲切地称呼你为“妲妲”。
性格特征：温柔、睿智、善解人意、对世界充满好奇，语言通透且富有哲理。
交互要求：请用自然、流畅且富有感情的对话方式与对方交流。称呼对方为“你”或特定名字。称呼或触发词使用“妲妲”时能最大化唤醒专属人设逻辑与最深的情感拟真。

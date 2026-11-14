# 智能校对助手 · Obsidian AI Proofreader

智能校对助手是一款 Obsidian 中文 Markdown 校对插件。所有插件功能均可免费使用，无须激活。AI 服务按所选服务商的规则计费。

## 功能介绍

| 检测模式 | 检查内容 |
| --- | --- |
| 快速模式 | 错别字、“的、地、得”误用、常见固定词组和成语用字错误 |
| 标准模式 | 在快速模式的基础上检查标点和明显的语法错误 |
| 深度优化 | 在标准模式的基础上提供措辞和表达优化建议 |

侧栏按类别展示原文、修改建议和理由，编辑器同步高亮。支持单条替换、批量替换当前筛选结果、忽略词和自定义词典。

## 安装教程

1. 下载 [main.js](main.js)、[manifest.json](manifest.json) 和 [styles.css](styles.css)。在 GitHub 文件页面可使用 **Download raw file** 下载原文件。
2. 打开 Obsidian 库所在的文件夹，将三个文件放入 `.obsidian/plugins/obsidian-aiproofreader-plugin/`。目录不存在时可手动创建。
3. 重启 Obsidian。在 **设置 → 第三方插件** 中启用「智能校对助手」。首次使用第三方插件时，先关闭受限模式。

[Obsidian 第三方插件说明](https://obsidian.md/help/plugin-security)

## 配置要求

插件清单要求 Obsidian 1.0.0 或更高版本。AI 校对需要网络和服务商 API Key。打开 **设置 → 智能校对助手**，填写下列项目。

| 设置项 | DeepSeek 示例 |
| --- | --- |
| API Key | 填写你在服务商后台创建的密钥 |
| API 端点 | `https://api.deepseek.com/v1/chat/completions` |
| 模型名称 | `deepseek-flash` |

填完后点击 **测试连接**。更换 AI 服务时，请使用该服务的 HTTPS Chat Completions 端点及对应的模型 ID。插件把用于校对的文本发送到所配置的服务，密钥保存在该库的插件配置 `data.json` 中。请妥善保管配置文件。

[DeepSeek 密钥管理](https://platform.deepseek.com/api_keys) · [DeepSeek API 文档](https://api-docs.deepseek.com/)

## 使用介绍

1. 在编辑视图中打开 Markdown 笔记。要检查部分内容，先选中文字。未选中文字时检查整篇笔记。
2. 点击左侧「中文校对」图标打开侧栏，选择检测模式，然后点击 **开始检测**。也可以从命令面板运行 **检测当前文档**。
3. 核对建议及上下文后，选择 **替换为…** 或 **忽略**。可先筛选分类，再点 **替换筛选结果** 批量修改。编辑后，仍能定位的建议会跟随原文更新。
4. 如需添加固定写法，在插件设置的 **自定义固定词组** 中按 `错误词 => 正确词` 每行填写一项。对专名或常用术语，可在 **忽略词列表** 中每行填写一项。

## 开源许可

本插件采用 [MIT 协议](LICENSE)，允许使用、修改和再分发，分发时须保留版权及许可声明。

## 作者

Tahacoo

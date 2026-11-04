# sd-webui-prompt-all-in-one

> **本分支说明**：本仓库为个人修改分支 `neo-patch`，基于上游 `266fdaf`（2026-11-04），仅包含以下修复，其余功能与上游一致。全部改动由 **DEEPSEEK** 完成。
>
> | 修复 | 内容 |
> | --- | --- |
> | 权重还原 | 权重调回 1 时不再残留 `(tag:1)`，自动还原为 `tag` |
> | 权重配色 | 括号、冒号、权重数字由红/绿改为跟随文字颜色（深色主题下为白色，不再刺眼） |
> | 背景保留 | 加权后关键词的分组背景色（如 `1girl` 的橙色）不再丢失 |
>
> 涉及文件：`javascript/main.entry.js`、`styles/main.min.css`

[![GitHub stars](https://img.shields.io/github/stars/Physton/sd-webui-prompt-all-in-one?style=flat-square)](https://github.com/Physton/sd-webui-prompt-all-in-one/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/Physton/sd-webui-prompt-all-in-one?style=flat-square)](https://github.com/Physton/sd-webui-prompt-all-in-one/network/members)
[![GitHub issues](https://img.shields.io/github/issues/Physton/sd-webui-prompt-all-in-one?style=flat-square)](https://github.com/Physton/sd-webui-prompt-all-in-one/issues)
[![GitHub issues closed](https://img.shields.io/github/issues-closed/Physton/sd-webui-prompt-all-in-one?style=flat-square)](https://github.com/Physton/sd-webui-prompt-all-in-one/issues?q=is%3Aissue+is%3Aclosed)
[![GitHub license](https://img.shields.io/github/license/Physton/sd-webui-prompt-all-in-one?style=flat-square)](https://github.com/Physton/sd-webui-prompt-all-in-one/blob/master/LICENSE.md)
[![GitHub commits](https://img.shields.io/github/last-commit/Physton/sd-webui-prompt-all-in-one?style=flat-square)](https://github.com/Physton/sd-webui-prompt-all-in-one/commits/main)
[![Netlify Status](https://api.netlify.com/api/v1/badges/1441a696-a1a4-4ad7-b520-4abfd96acc76/deploy-status)](https://app.netlify.com/sites/aiodoc/deploys)

<div align="center">

### [🇺🇸 English](README.MD) | [🇷🇺 Русский](README_RU.MD) | [🇨🇳 简体中文](README_CN.MD) | [🇯🇵 日本語](README_JP.MD) | [🇰🇷 한국어](README_KR.MD) | [🇨🇳 繁體中文](README_TW.MD)

</div>

sd-webui-prompt-all-in-one 是一个基于 [stable-diffusion-webui](https://github.com/AUTOMATIC1111/stable-diffusion-webui) 的扩展，旨在提高提示词/反向提示词输入框的使用体验。它拥有更直观、强大的输入界面功能，它提供了自动翻译、历史记录和收藏等功能，它支持多种语言，满足不同用户的需求。

---

**📮📮📮 非常抱歉，由于个人精力有限，本项目不再维护。但是如果有朋友改进了代码，欢迎提交Pull Request，我会抽空合并到主分支。**

---

<div align="center">

### 安装教程、功能详解、使用方法、常见问题等等，详见：[文档](https://aiodoc.physton.com/zh-CN/)。

</div>

----

**📢📢📢 本项目已开发独立运行版本，不依赖 stable-diffusion-webui 既可运行。轻便小巧，专注于提示词的编辑和整理。前往 [Physton/sd-webui-prompt-all-in-one-app](https://github.com/Physton/sd-webui-prompt-all-in-one-app) 查看使用教程。**

----

> 如果你觉得这个扩展有帮助，请在Github上给我一颗星！
> 你也可以请我喝杯咖啡: [donate](#捐赠)

----

> 中国用户镜像地址：[https://gitee.com/physton/sd-webui-prompt-all-in-one.git](https://gitee.com/physton/sd-webui-prompt-all-in-one.git)

----

## 翻译API说明

1. `不需要API KEY`：它们非常不稳定，并不是每个API都能在你的电脑中使用。如果翻译失败，请尝试切换其他API，⚠️⚠️⚠️**不要提交issue！**
2. `需要API KEY`：需要自行申请API KEY。不同接口的申请方法，在切换到对应接口后，会出现对应的申请教程。⚠️⚠️⚠️**它们大部分都是 `免费` 的！**
3. `离线翻译`：在初始化时需要自动下载语言模型。如果你的网络环境不好，可能无法完成自动下载并初始化。

## [文档](https://aiodoc.physton.com/zh-CN/)

- [安装](https://aiodoc.physton.com/zh-CN/Installation.html)
- [扩展更新说明](https://aiodoc.physton.com/zh-CN/ExtensionUpdateDescription.html)
- [翻译接口说明](https://aiodoc.physton.com/zh-CN/TranslationApiConfiguration.html#翻译接口说明)
- [帮助开发](https://aiodoc.physton.com/zh-CN/Contributing.html)
- [自定义主题](https://aiodoc.physton.com/zh-CN/Contributing.html#自定义主题)
- [常见问题](https://aiodoc.physton.com/zh-CN/FAQ.html)
- [请我喝杯咖啡](#请我喝杯咖啡)

## 语言支持

支持几乎所有国家语言的翻译，但大部分国家的UI界面会显示为英文，如果需要本地化语言显，你可以翻译后提交PR。

<details>
<summary>UI支持的语言</summary>

`简体中文` `繁體中文` `English` ` Русский` `日本語` `한국어` ` Français` `Deutsch` ` Español` `Português` `Italiano` `العربية`
</details>

<details>
<summary>翻译支持的语言</summary>

`简体中文 (中国)` `繁體中文 (中國香港)` `繁体中文 (中國台灣)` `English (US)` `Afrikaans (South Africa)` `Shqip (Shqipëria)` `አማርኛ (ኢትዮጵያ)` `العربية (السعودية)` `Հայերեն (Հայաստան)` `অসমীয়া (ভাৰত)` `Azərbaycan dili (Latın, Azərbaycan)` `বাংলা (বাংলাদেশ)` `Башҡорт (Россия)` `Euskara (Espainia)` `Bosanski (Latinski, Bosna i Hercegovina)` `Български (България)` `Català (Espanya)` `Hrvatski (Hrvatska)` `Čeština (Česká republika)` `Dansk (Danmark)` `درى (افغانستان)` `ދިވެހިބަސް (ދިވެހިރާއްޖެ)` `Nederlands (Nederland)` `Eesti (Eesti)` `Føroyskt (Føroyar)` `vosa Vakaviti (Viti)` `Filipino (Pilipinas)` `Suomi (Suomi)` `Français (France)` `Français (Canada)` `Galego (España)` `ქართული (საქართველო)` `Deutsch (Deutschland)` `Ελληνικά (Ελλάδα)` `ગુજરાતી (ભારત)` `Kreyòl ayisyen (Ayiti)` `עברית (ישראל)` `हिन्दी (भारत)` `Hmong Daw (Latn, United States)` `Magyar (Magyarország)` `Íslenska (Ísland)` `Bahasa Indonesia (Indonesia)` `Inuktitut (Kanatami)` `Inuktitut (Latin, Canada)` `ᐃᓄᒃᑎᑐᑦ (ᑲᓇᑕᒥ)` `Gaeilge (Éire)` `Italiano (Italia)` `日本語 (日本)` `ಕನ್ನಡ (ಭಾರತ)` `Қазақ (Қазақстан)` `ភាសាខ្មែរ (កម្ពុជា)` `Klingon (Latn)` `Klingon (plqaD)` `한국어 (대한민국)` `کوردی (عێراق)` `Kurmancî (Latînî, Tirkiye)` `Кыргызча (Кыргызстан)` `ລາວ (ລາວ)` `Latviešu (Latvija)` `Lietuvių (Lietuva)` `Македонски (Северна Македонија)` `Malagasy (Madagasikara)` `Bahasa Melayu (Latin, Malaysia)` `മലയാളം (ഇന്ത്യ)` `Malti (Malta)` `Māori (Aotearoa)` `मराठी (भारत)` `Монгол (Кирилл, Монгол улс)` `ᠮᠣᠩᠭᠣᠯ ᠤᠯᠤᠰ (ᠨᠢᠭᠡᠳᠦᠯ ᠤᠨᠤᠭ᠎ᠠ)` `မြန်မာ (မြန်မာ)` `नेपाली (नेपाल)` `Norsk bokmål (Norge)` `ଓଡ଼ିଆ (ଭାରତ)` `پښتو (افغانستان)` `فارسی (ایران)` `Polski (Polska)` `Português (Brasil)` `Português (Portugal)` `ਪੰਜਾਬੀ (ਗੁਰਮੁਖੀ, ਭਾਰਤ)` `Querétaro Otomi (Latn, México)` `Română (România)` `Русский (Россия)` `Samoan (Latn, Samoa)` `Српски (ћирилица, Србија)` `Srpski (latinica, Srbija)` `Slovenčina (Slovensko)` `Slovenščina (Slovenija)` `Soomaali (Soomaaliya)` `Español (España)` `Kiswahili (Kenya)` `Svenska (Sverige)` `Reo Tahiti (Polynésie française)` `தமிழ் (இந்தியா)` `Татарча (латин, Россия)` `తెలుగు (భారత)` `ไทย (ไทย)` `བོད་ཡིག (རྒྱ་གར།)` `ትግርኛ (ኢትዮጵያ)` `lea fakatonga (Tonga)` `Türkçe (Türkiye)` `Українська (Україна)` `اردو (پاکستان)` `ئۇيغۇرچە (ئۇيغۇرچە، جۇڭگو)` `O'zbekcha (Lotin, O'zbekiston)` `Tiếng Việt (Việt Nam)` `Cymraeg (Y Deyrnas Unedig)` `Yucatec Maya (México)` `isiZulu (iNingizimu Afrika)`
</details>

## 特性

- `直观的输入界面` 提供更直观、强大的输入界面功能，提示词双语对照显示，一目了然。
- `自动翻译` 自动翻译提示词/反向提示词，支持多种语言。
- `几十种翻译服务` 几十个在线翻译，还有离线翻译模型。
- `多国语言` 支持世界上大部分国家语言的翻译，你可以使用任何语言输入提示词。
- `历史记录` 当提示词/反向提示词发生变化时，自动记录。
- `收藏夹` 一键收藏、批量收藏你喜欢的提示词/反向提示词。
- `快速调整` 拖拽调整提示词位置，一键增减提示词权重，一键删除、一键禁用、一键翻译、一键收藏等等。
- `批量操作` 框选多个提示词/反向提示词，一键删除、一键翻译、一键收藏等等。
- `ChatGPT` 通过ChatGPT智能生成提示词。
- `提示词黑名单` 设置黑名单，自动过滤提示词。
- `一键添加提示词` 几千个提示词，点击即可使用。
- `关键词高亮` Lora、LyCORIS、Textual Inversion 高亮和检测。
- `关键词自定义颜色` 不同种类的关键词，可以自定义显示不同的颜色。
- `自定义主题` 自定义主题，自定义扩展风格。
- `......` 更多功能等你发现。

## 演示

- [切换语言](https://aiodoc.physton.com/zh-CN/LanguageSelection.html)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.switch_language.gif)

- [翻译API设置](https://aiodoc.physton.com/zh-CN/TranslationApiConfiguration.html)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.translate_setting.gif)

- [显示/折叠内容](https://aiodoc.physton.com/zh-CN/OtherFeatures.html#显示-折叠扩展面板)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.fold.gif)

- [显示/隐藏WebUI输入框](https://aiodoc.physton.com/zh-CN/OtherFeatures.html#显示-隐藏webui输入框)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.show_input.gif)

- [自动翻译](https://aiodoc.physton.com/zh-CN/AutomaticTranslation.html)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.auto_translate.gif)

- [一键翻译](https://aiodoc.physton.com/zh-CN/BatchTranslation.html)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.translate.gif)

- [优雅的输入](https://aiodoc.physton.com/zh-CN/KeywordInputBox.html)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.elegant_input.gif)

- [快速调整](https://aiodoc.physton.com/zh-CN/ListOfKeywords.html)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.quick_adjust.gif)

- [收藏和历史记录](https://aiodoc.physton.com/zh-CN/History.html)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.history_favorite.gif)

- [使用ChatGPT生成Prompt](https://aiodoc.physton.com/zh-CN/UsingChatgptToGeneratePrompts.html)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.chatgpt.gif)

- [在WebUI的输入框中编写](https://aiodoc.physton.com/zh-CN/WritingInWebUIInputBox.html)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.writing_webui.gif)

- 支持[a1111-sd-webui-tagcomplete](https://github.com/DominikDoom/a1111-sd-webui-tagcomplete)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.tagcomplete.gif)

- [Lora、LyCORIS、Textual Inversion 高亮和检测](https://aiodoc.physton.com/zh-CN/ListOfKeywords.html#高亮关键词)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.keyword_detection.gif)

- [Prompt提示词格式](https://aiodoc.physton.com/zh-CN/FormatOfPrompts.html)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.prompt_format.gif)

- [批量操作](https://aiodoc.physton.com/zh-CN/BatchOperation.html)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.batch_operation.gif)

- [自定义主题/扩展风格](https://aiodoc.physton.com/zh-CN/ThemeStyle.html)

  ![](https://s1.imagehub.cc/images/2023/06/06/demo.custom_theme.gif)

- [一键添加关键词](https://aiodoc.physton.com/zh-CN/GroupTags.html)

  ![](https://s1.imagehub.cc/images/2023/08/15/demo.group_tags.gif)

## 捐赠

[捐赠列表](https://aiodoc.physton.com/zh-CN/Donate.html)

### 请我喝杯咖啡

> 留言可能无法回复，如有问题请联系QQ：94126162或邮箱：pyhston@163.com。
>
| ko-fi (EN) | [![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/physton) |
|:-----------:| :----: |
| Paypal (EN) | [https://paypal.me/physton](https://paypal.me/physton) |
| 爱发电 (CN) | [https://afdian.net/a/physton/thank](https://afdian.net/a/physton/thank) |
| 支付宝 (CN) | ![](https://s1.imagehub.cc/images/2023/07/05/alipay.jpeg) |
| 微信赞赏 (CN) | ![](https://s1.imagehub.cc/images/2023/07/05/wechat.jpeg) |
# Codex / Claude Code + CC Switch 接入教程

本文档用于帮助您通过 `CC Switch` 连接 API 服务。`Codex` 和 `Claude Code` 在 `CC Switch` 中的设置步骤相同，推荐使用 API 页面提供的“导入到 CCS”按钮自动完成配置。

## 一、下载工具

Codex 下载地址：

```text
https://chatgpt.com/download/
```

Codex 官方介绍：

```text
https://openai.com/codex/
```

CC Switch 下载地址：

```text
https://github.com/farion1231/cc-switch/releases/latest
```

CC Switch 官网：

```text
https://ccswitch.ai/
```

macOS 用户也可以使用 Homebrew 安装：

```bash
brew tap farion1231/ccswitch
brew install --cask cc-switch
```

## 二、推荐方式：导入到 CCS

请优先使用 API 页面的一键导入功能。

操作步骤：

1. 打开 API Keys 页面
2. 找到要使用的 API Key
3. 点击“导入到 CCS”
4. 浏览器会唤起 CC Switch
5. 选择 `Codex` 或 `Claude Code`
6. 确认导入
7. 打开对应客户端测试

`Codex` 和 `Claude Code` 的导入步骤是一样的，只是选择的客户端类型不同。

## 三、手动配置方式

如果点击“导入到 CCS”后没有唤起 CC Switch，可以手动新建配置。

请在 `CC Switch` 中填写：

```text
供应商名称：Mecho
官网链接：https://api.mecho.top
App: Codex 或 Claude Code
请求地址：https://api.mecho.top
API Key: 当前 API Key
Model: 默认模型名
```

注意：

- `官网链接` 请填写 `https://api.mecho.top`
- `请求地址` 请填写 `https://api.mecho.top`
- 请求地址末尾不要加斜杠
- 不要填写本文档页面地址
- 不要填写官网地址、后台地址或登录页面地址
- `API Key` 请完整复制，不要多复制空格或换行

## 四、测试连接

打开 `Codex` 或 `Claude Code` 后，发送一个简单请求：

```text
请帮我读取当前文件夹结构，并简单说明这个项目是做什么的。
```

如果可以正常返回内容，说明已经连接成功。

## 常见问题

### 1. 点击导入到 CCS 没有反应

请检查：

- 是否已经安装 CC Switch
- 浏览器是否拦截了外部应用唤起
- CC Switch 是否可以正常打开

### 2. 提示 401 或 403

这通常是认证失败或权限不足。

请检查：

- API Key 是否复制完整
- API Key 是否过期
- 当前账号是否有对应模型权限

### 3. 提示 404

这通常是 API 地址填写错误。

请检查：

- 手动配置时请求地址是否填写为 `https://api.mecho.top`
- 请求地址末尾是否多加了斜杠
- 是否误填了本文档地址、官网地址、后台地址或登录页面地址

### 4. 配置后仍失败

请检查：

- CC Switch 当前启用的是否是正确配置
- 选择的客户端类型是否正确
- 模型名是否填写正确
- 修改配置后是否已经重启 Codex 或 Claude Code

如果仍无法连接，请提供报错截图、系统类型、API 页面截图和 CC Switch 配置页面截图，方便进一步排查。

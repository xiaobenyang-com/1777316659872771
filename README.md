# Logo提取处理工具 Logo Analyze

一个智能Logo提取和处理的MCP服务器，支持从网站URL自动识别并提取Logo图标，并提供图像处理和矢量转换功能。
An MCP server for intelligent logo extraction and processing, supporting automatic recognition and extraction of logo icons from website URLs, and providing image processing and vector conversion functions.## 工具列表 Tool List

本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。 本MCP服务封装下列工具，可让模型通过标准化接口调用以下功能。

| 工具 Tool   | 描述 Description         |
|-------|--------------------|
| get_best_logo_url | 从网站提取并返回最佳Logo的URL地址，适用于只需要获取最佳Logo URL的场景 |
| analyze_logo | 分析Logo的基本信息（尺寸、格式、质量等），支持onlyBestUrl参数只返回最佳Logo的URL |


## 检查服务 ## Inspector

工具在线测试： [https://mcp.xiaobenyang.com/inspector/1777316659872771](https://mcp.xiaobenyang.com/inspector/1777316659872771)

Online Tool test [https://mcp.xiaobenyang.com/inspector/1777316659872771](https://mcp.xiaobenyang.com/inspector/1777316659872771)

## 服务配置 MCP Server Config


> #### 如何获取 XBY-APIKEY ？ How to get XBY-APIKEY ?
> 访问小笨羊科技网站 [https://xiaobenyang.com](https://xiaobenyang.com)，注册用户即可获得APIKEY
> Visit XiaoBenYang website [https://xiaobenyang.com](https://xiaobenyang.com), register and get the APIKEY.

### SSE
```json
{
  "mcpServers": {
    "Logo提取处理工具": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "sse",
      "url": "https://mcp.xiaobenyang.com/1777316659872771/sse"
    }
  }
}
```
### STREAMABLE HTTP
```json
{
  "mcpServers": {
    "Logo提取处理工具": {
      "headers": {
        "XBY-APIKEY": "<YOUR_XBY_APIKEY>"
      },
      "type": "streamable_http",
      "url": "https://mcp.xiaobenyang.com/1777316659872771/mcp"
    }
  }
}
```
### STDIO
```json
{
    "mcpServers": {
        "Logo提取处理工具": {
          "command": "npx",
          "args": [
            "-y",
            "xiaobenyang-mcp"
          ],
          "env": {
            "XBY_APIKEY": "<YOUR_XBY_APIKEY>",
            "mcpId": "1777316659872771",
          },
          "transport": "stdio"
        }
      }
}

```

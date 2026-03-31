# hydro-annual — 浙江省水资源年报查询与导出工具

## Quick Reference

| 项目 | 路径/值 |
|------|---------|
| 入口文件 | `app.py` (Streamlit) |
| 数据目录 | `data/` + `src/annual/` |
| 公共模块 | `src/common/` |
| 线上地址 | https://hydro-annual.tianlizeng.cloud |
| Streamlit 配置 | `.streamlit/config.toml` |

## 常用命令

```bash
cd /Users/tianli/Dev/hydro-annual

# 本地启动
streamlit run app.py

# 依赖安装
pip install -r requirements.txt
```

## 项目结构

```
app.py              # Streamlit 主入口，页面逻辑
src/
  annual/           # 年报数据解析与查询逻辑
  common/           # 通用工具函数
data/
  sample/           # 内置数据集（无需上传）
.streamlit/
  config.toml       # 端口、主题等配置
```

## 核心功能

- 覆盖 2019–2024 年浙江省水资源年报数据（内置，无需上传）
- 按城市（地级市）、类别筛选，支持导出 Excel / CSV
- 无外部 API 依赖，数据纯本地

## 部署说明

VPS 上运行于 `/var/www/hydro-annual`，通过 Nginx 反代到 Streamlit 端口，域名 `hydro-annual.tianlizeng.cloud` 走 Cloudflare。修改后同步到 VPS：

```bash
ssh root@104.218.100.67
cd /var/www/hydro-annual && git pull

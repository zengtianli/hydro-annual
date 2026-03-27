# 📊 水资源年报

[![GitHub stars](https://img.shields.io/github/stars/zengtianli/hydro-annual)](https://github.com/zengtianli/hydro-annual)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Python 3.9+](https://img.shields.io/badge/Python-3.9+-blue.svg)](https://python.org)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.36+-FF4B4B.svg)](https://streamlit.io)

浙江省水资源年报数据查询与导出工具（2019–2024）。

![screenshot](docs/screenshot.png)

## 功能特点

- **多年查询** — 浏览 2019 至 2024 年水资源数据
- **城市与表名筛选** — 按地级市和报表类别过滤
- **数据概览** — 快速查看汇总统计和记录数
- **Excel / CSV 导出** — 下载筛选结果
- **内置数据集** — 预载 CSV 数据，无需上传

## 快速开始

```bash
git clone https://github.com/zengtianli/hydro-annual.git
cd hydro-annual
pip install -r requirements.txt
streamlit run app.py
```

## 部署（VPS）

```bash
git clone https://github.com/zengtianli/hydro-annual.git
cd hydro-annual
pip install -r requirements.txt
nohup streamlit run app.py --server.port 8504 --server.headless true &
```

## Hydro Toolkit 插件

本项目是 [Hydro Toolkit](https://github.com/zengtianli/hydro-toolkit) 的插件，也可独立运行。在 Toolkit 的插件管理页面粘贴本仓库 URL 即可安装。

## 许可证

MIT

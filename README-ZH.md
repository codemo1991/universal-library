<div align="center">
 <h1>📚 任意图书馆 📚</h1>
   <h2> <a href="README.md">🇺🇸 English Document</a></h2>
</div>

### 文档上传和文档搜索

## 🎯 整体构思
由于存在大量的文档和资料，很多场景需要根据某句话或者某个图片追踪到某个文档并且需要解读文档的内容。在传统的搜索业务上，借助搜索引擎和向量查询结合LLM就可以实现很多意想不到的拓展功能。

## 🏗️ 整体架构
- Elasticsearch 存储精确文本,提供精确查询
- Apache Tika 提取多种文本文档
- Milvus 存储向量数据，提供向量查询
- Minio 存储文件，提供文件上传和下载
- Streamlit 前端展示

## 📁 目录划分
- /test 测试目录
- /upload.py 文档上传与语义搜索，程序入口
- /requirements.txt 依赖定义
- /docker-compose.yml docker 文件 启动minio、milvus、elasticsearch、kibana

## ⚙️ 环境准备
- 启动docker-desktop
  - docker-compose down -v [minio、milvus、elasticsearch] 删除容器
  - docker-compose up -d [minio、milvus、elasticsearch] 启动容器
- 执行docker-compose.yml 启动minio、milvus、elasticsearch
- 执行 pip install -r requirements.txt 安装依赖
- streamlit run ./upload.py 启动程序

## 🎬 demo演示
### 📤 首页
![首页](./doc/1.png)

### 📤 文档上传
![文档上传](./doc/2.png)

### 📄 elasticsearch文件存储
![elasticsearch文件存储](./doc/3.png)

### 📄 Milvus文件存储
![Milvus文件存储](./doc/7.png)

### 📄 Minio文件存储
![Minio文件存储](./doc/4.png)

### 📄 语义搜索 & 精确搜索
![精确搜索](./doc/6.png)



## 🗺️ Roadmap
- [x] 支持文件上传
- [x] 支持精确搜索和语义搜索
- [ ] 支持定位指定文档位置&支持在线文档查看
- [ ] 支持LLM提问和回答
- [ ] 支持指定pdf提问和回答
- [ ] 其他功能

## 💬 Contact & Contribution
- 如果有疑问，请提交 Issue
- 如果有兴趣，欢迎提交 PR
- 其他问题，请联系我：codemo1991@gmail.com 或者 discord: https://discord.gg/z7MW5UK4

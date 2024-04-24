# 网关服务

该项目是一个网关服务，用于将请求转发到指定的目标服务。它具有以下特点：

简单易用：只需要一个可用的代理，即可实现 1:1 的官网界面。
多用途：可以作为各种地方的网关，例如 share、mirror 等。

## 使用 Docker 部署

### 1. 使用 docker-compose 部署

1. 直接下载 [docker-compose.yaml](link-to-your-docker-compose-file) 文件。

2. 在命令行中执行以下命令启动网关服务：

   ```bash
   docker-compose up
   
### 2. 手动拉取镜像并运行容器

1. 首先，拉取网关服务的 Docker 镜像：

   ```bash
   docker pull hei782/gateway:1.2
   
2. 在命令行中执行以下命令启动网关服务：

   ```bash
   docker run -d -p 7999:7999 \
              -e "PROXY=http://your-proxy-address:port" \
              --name gateway \
              hei782/gateway:1.2


将 "http://your-proxy-address:port" 替换为可访问 GPT 的代理地址。

## 访问网关服务：

现在你可以通过访问 "http://IP:7999" 来使用网关服务了。你可以根据需要修改端口号和其他配置。

## 参与贡献

欢迎提出问题和改进建议！如果你发现了 Bug 或者有新功能的想法，请提交一个 Issue 或者直接发起一个 Pull Request。

## 版权和许可

MIT 许可证 © [hei]

网关服务

该项目是一个网关服务，用于将请求转发到指定的目标服务。它具有以下特点：

简单易用：只需要一个可用的代理，即可实现 1:1 的官网界面。
多用途：可以作为各种地方的网关，例如 share、mirror 等。
使用 Docker 部署

构建 Docker 镜像：

首先，确保你已经安装了 Docker。然后在项目根目录执行以下命令构建 Docker 镜像：

docker build -t hei782/gateway:1.2 .

运行 Docker 容器：

运行以下命令启动网关服务的 Docker 容器：

docker run -d -p 7999:7999 --name gateway -e PROXY=http://your-proxy-address:port hei782/gateway:1.2

将 "http://your-proxy-address:port" 替换为可访问 GPT 的代理地址。

访问网关服务：

现在你可以通过访问 "http://localhost:7999" 来使用网关服务了。你可以根据需要修改端口号和其他配置。

参与贡献

欢迎提出问题和改进建议！如果你发现了 Bug 或者有新功能的想法，请提交一个 Issue 或者直接发起一个 Pull Request。

版权和许可

MIT 许可证 © [hei]

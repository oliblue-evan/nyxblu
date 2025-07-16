<img align="right" width="150" alt="logo" src="https://user-images.githubusercontent.com/5889006/190859553-5b229b4f-c476-4cbd-928f-890f5265ca4c.png">

# Hugo Theme Stack 快速启动模板

这是 [Hugo theme Stack](https://github.com/CaiJimmy/hugo-theme-stack) 的快速启动模板。它使用 [Hugo modules](https://gohugo.io/hugo-modules/) 功能加载主题。

模板包含基本的主题结构和配置。GitHub Action 已设置为自动将主题部署到公开的 GitHub 页面，并且有一个定时任务每天自动更新主题。

## 开始使用

1. 点击 *Use this template*，在 GitHub 上创建名为 `<username>.github.io` 的仓库。
![步骤 1](https://user-images.githubusercontent.com/5889006/156916624-20b2a784-f3a9-4718-aa5f-ce2a436b241f.png)

2. 仓库创建后，创建与其关联的 GitHub Codespace。
![创建 Codespace](https://user-images.githubusercontent.com/5889006/156916672-43b7b6e9-4ffb-4704-b4ba-d5ca40ffcae7.png)

3. 一切就绪！Codespace 已配置最新版本的 Hugo 扩展版，只需在终端运行 `hugo server` 即可查看新网站。

4. 查看 `config` 文件夹中的配置文件，您可以根据需要进行编辑。确保将 `config/_default/config.toml` 中的 `baseurl` 属性更新为您网站的 URL。

5. 打开设置 -> Pages，将构建分支从 `master` 更改为 `gh-pages`。
![构建](https://github.com/namanh11611/hugo-theme-stack-starter/assets/16586200/12c763cd-bead-4923-b610-8788f388fcb5)

6. 编辑网站完成后，提交并推送更改。GitHub Action 将自动将网站部署到与仓库关联的 GitHub 页面。
![GitHub Action](https://user-images.githubusercontent.com/5889006/156916881-90b8bb9b-1925-4e60-9d7a-8026cda729bf.png)

---

如果不想使用 GitHub Codespace，您也可以在本地计算机上运行此模板。**您需要在本地安装 Git、Go 和 Hugo 扩展版。**

## 手动更新主题

运行以下命令：

```bash
hugo mod get -u github.com/CaiJimmy/hugo-theme-stack/v3
hugo mod tidy
```

> 此启动模板已配置为使用主题的 `v3` 版本。由于 Go 模块的限制，一旦主题发布 `v4` 或更高版本，您需要手动更新主题（修改 `config/module.toml` 文件）。

## 部署到其他静态页面托管服务

如果要使用其他静态页面托管服务构建此网站，需要确保托管服务的机器上已安装 Go。

<details>
  <summary>Vercel</summary>
  
您需要覆盖构建命令以手动安装 Go：

```
amazon-linux-extras install golang1.11 && hugo --gc --minify
```

![](https://user-images.githubusercontent.com/5889006/156917172-01e4d418-3469-4ffb-97e4-a905d28b8424.png)

如果使用 Node.js 20，需要覆盖安装命令以手动安装 Go：

```
dnf install -y golang
```

![image](https://github.com/zhi-yi-huang/hugo-theme-stack-starter/assets/83860323/777c1109-dfc8-4893-9db7-1305ec027cf5)


确保在环境变量 `HUGO_VERSION` 中指定 Hugo 版本（使用最新版本的 Hugo 扩展版）：

![环境变量](https://user-images.githubusercontent.com/5889006/156917212-afb7c70d-ab85-480f-8288-b15781a462c0.png)
</details>

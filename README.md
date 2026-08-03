# zouyihong.com - 邹宜洪个人主页

邹宜洪 (Zou Yihong) 个人主页，部署在 [s9.serv00.com](https://s9.serv00.com)。

- 🌐 线上：<https://zouyihong.com>
- 📝 后台：<https://zouyihong.com/admin/> (Decap CMS)
- 💬 论坛：<https://forum.zouyihong.com>
- 🛒 阿里国际站：<https://ailita4x4.com/our-alibaba-com-stores/>

## 技术栈

- **[Hugo](https://gohugo.io/)** 0.151.0 - 静态站点生成
- **[PaperMod](https://github.com/adityatelange/hugo-PaperMod)** - Hugo 主题
- **Decap CMS** - Git-based 内容管理后台
- **s9.serv00.com** (FreeBSD 14.3) - 部署服务器
- **Cloudflare** - DNS / CDN / SSL

## 本地开发

```bash
# 拉 submodules
git submodule update --init --recursive

# 跑 hugo dev server
hugo server -D

# 构建
hugo --minify
```

## 部署

`deploy.sh` 在 `~/hugo_projects/` 父目录：

```bash
~/hugo_projects/deploy.sh
```

会自动：
1. `hugo --minify` 编译
2. 备份当前 webroot（保留 10 个）
3. 同步到 `~/domains/zouyihong.com/public_html/`
4. 重启 PHP -S
5. 验证 3 个核心页面

## 内容管理

- **直接编辑**：`content/` 下的 Markdown 文件
- **Decap CMS 后台**：<https://zouyihong.com/admin/>
- **CLI 部署**：`~/hugo_projects/deploy.sh`

## 维护

- **作者**：邹宜洪 (Zou Yihong) - ryan@zouyihong.com
- **Jade (小鱼)** - Hermes Agent 助手，负责自动部署与运维

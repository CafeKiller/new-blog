---
title: '常见问题'
description: '常见问题解答'
order: 4
---

## 路径

### 博客特定路径

将博客路由格式设置为 `/blog/:year/:id`

参见 [4.0.2-beta如何使文章链接中包含年份](https://github.com/cworld1/astro-theme-pure/discussions/37#discussioncomment-11905851)。

## 内容

### 为 `heroImage` 支持网络图片

需要配合 `inferSize: true` 来获取图片尺寸。示例：

```yaml
heroImage:
  { src: 'https://img.tukuppt.com/ad_preview/00/15/09/5e715a320b68e.jpg!/fw/980', inferSize: true }
```

## 构建

### Vite 阻止请求

```log
Blocked request. This host ("xxx")is not allowed.
To allow this host, add "xxx" to `preview.allowedHosts` in vite.config.js.
```

参见 [option server.allowedHosts doesn't take into account "true"](https://github.com/vitejs/vite/issues/19242)

### `BUN_LINK_PKG` 问题

参见 [BUN_LINK_PKG 环境变量无法设置成功](https://github.com/cworld1/astro-theme-pure/issues/51)

### 构建时 No "Exports" Main Defined 错误

```log
07:39:23 [ERROR] [@astrojs/vercel] An unhandled error occurred while running the "astro:build:done" hook
No "exports" main defined in /vercel/path0/node_modules/estree-walker/package.json
  Stack trace:
    ...
```

尝试在不使用现有构建缓存的情况下重新部署项目。

详情：[oven-sh/bun/issues: error No "exports" main defined in /vercel/path0/node_modules/estree-walker/package.json](https://github.com/oven-sh/bun/issues/7241)

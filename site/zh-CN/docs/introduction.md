# 介绍

Pagic 是一个由 Deno + React 驱动的静态网站生成器。

它配置简单，支持将 `md/tsx` 文件渲染成静态页面，而且还有大量的官方或第三方主题和插件可供扩展。

## 特性

### 配置简单

Pagic 遵循[约定优于配置](https://zh.wikipedia.org/wiki/%E7%BA%A6%E5%AE%9A%E4%BC%98%E4%BA%8E%E9%85%8D%E7%BD%AE)的理念，尽可能的减少配置项，通过一些符合直觉的设计，降低用户的理解成本，而又不失灵活性。

### 支持 md 和 tsx

Pagic 不仅支持将 `md/tsx` 文件渲染成静态页面，而且还能运行 `tsx` 中的 Hooks，借助 React 组件的可编程性，极大的扩展了静态网站的能力。

值得注意的是，每一个由 Pagic 生成的页面都带有预渲染好的 HTML，也因此具有极致的加载性能和搜索引擎优化（SEO）。同时，一旦页面被加载，React 将接管这些静态内容，并将其转换成一个完整的单页应用（SPA），其他的页面则会只在用户浏览到的时候才按需加载。

### 主题和插件

Pagic 拥有官方的 default, docs, blog 等主题，我们可以使用官方主题轻松的生成一个网站，也可以创建个性化的主题，甚至还可以扩展某个主题——这些能力都得益于 Pagic 符合直觉的 `_layout.tsx` 设计。

插件是 Pagic 最核心的功能之一。Pagic 将整个构建过程拆分为一个个内置插件，使得其他插件可以插入到构建过程中的任意位置，甚至可以通过替换内置插件完全的更改 Pagic 的构建过程，这给 Pagic 提供了无与伦比的灵活性。

Pagic 参考了 Deno 的设计，要求用户通过一个完整的 URL 来引入第三方主题或插件。

## 竞品对比

作为一个「静态网站生成器狂热爱好者」，大部分流行的静态网站生成器我都使用过，它们都很优秀，但 Pagic 尝试了一些新的设计理念。下面列出一些关键性差异：

|           | Pagic | VuePress | Hexo | Jekyll | Hugo |
| --------- | ----- | -------- | ---- | ------ | ---- |
| 支持 md   | ✓     | ✓        | ✓    | ✓      | ✓    |
| React/Vue | ✓     | ✓        |      |        |      |
| SPA       | ✓     | ✓        |      |        |      |
| ...       |       |          |      |        |      |

Pagic 站在了巨人的肩膀上，参考了一些其他静态网站生成器的配置项、文档等，在此给予这些开源软件及开源社区最诚挚的感谢。
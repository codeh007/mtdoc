# mmtadmin 前端

# 富文本编辑器

- <https://github.com/manakuro/project-management-demo-frontend> (使用了<https://prosemirror.net/> Chakra UI Apollo Client)

- <https://github.com/TypeCellOS/BlockNote> (基于 Prosemirror 和 Tiptap 的概念式基于block的可扩展文本编辑器🔗)

# 一些热门 ui 库备忘

- (精品)<https://github.com/shadcn/ui>
  Radix UI + Tailwind + nextjs (10k starts) (在线演示：<https://ui.shadcn.com/>)
  另一个在 shadcn ui 基础上做的扩展： https://github.com/BelkacemYerfa/shadcn-extension


- <https://react-cmdk.com/>
- [<https://tailwindcss-radix.vercel.app/>-](https://github.com/mckaywrigley/chatbot-ui) chatgpt 界面： 15.5k stars
- <https://github.com/cruip/tailwind-dashboard-template.git>

# tailwindcss 相关

- <https://tailwind-elements.com/docs/standard/navigation/sidenav/>

## webssh 参考项目

- <https://github.com/billchurch/webssh2>

## 动画库

- [gsap] <https://github.com/greensock/GSAP> 有大量的优秀的网站都在使用它, 也适合在 react 下使用

## 在线随机图片

- <https://source.unsplash.com/collection/1346951/1000x500?sig=1>

## 富文本编辑器

- 首选 <https://github.com/facebook/lexical>
  原因是 meta 出品，react 原生，且对自定义组件支持足够好

## 树状 UI

- <https://github.com/minop1205/react-dnd-treeview> 特点：headless，基于 react-dnd 实现可拖放，数据结构跟后端搭配。sh
- <https://github.com/brimdata/react-arborist> 自带完整树状功能，typescript + react 很适合做左侧导航栏。2k stars 演示： <https://react-arborist.netlify.app/gmail>

## 代码备忘

判断 dom 点击是否是自身

```js
function isModifiedEvent(event: React.MouseEvent): boolean {
    const eventTarget = event.currentTarget as HTMLAnchorElement | SVGAElement;
    const target = eventTarget.getAttribute('target');
    return (
        (target && target !== '_self') ||
        event.metaKey ||
        event.ctrlKey ||
        event.shiftKey ||
        event.altKey || // triggers resource download
        (event.nativeEvent && event.nativeEvent.which === 2)
    );
}
```

## tailwind css 在线范例参考

- <https://supastarter.dev/products/starter-kits/nextjs>

# 布局参考

- <https://mui.com/blog/first-look-at-joy/>

# pnpm + next + monorepo 参考

- <https://github.com/vercel/examples/blob/main/solutions/monorepo/packages/ui/package.json>

1: 如果需要使用 turborepo 的方式，参考:<https://github.com/t3-oss/create-t3-turbo>
turborepo 其实大大增加了复杂性。
turborepo 应该用来做公共库，结合 changeset 发布工具，将常用的代码放到库里面公开发布到 npm
2: 如果是简单的单个 project 的方式，可以使用`npx create-t3-app`, 快速建立 prisma + nextjs13 + tRpc 的技术栈。

# 旧

1：作为代理其他商品销售的网站，也就是说商品数据通过 api 的形式获取，在页面上销售。

第一步： 做成全栈形式的站点，目前主要以虚拟商品为主。

对标：

- <http://ebay33.cn/>
- <https://www.viewpals.co/>
- <https://www.app.tubekick.co/tiktok/create-order>
- <https://grabsocial.net/tiktok/shop/index1.html>

## 第三方 点赞平台（收费）

<https://www.viralstamp.com/vip/buy-tiktok-likes>
<https://www.tokrush.com/checkout?quantity=20&id=3> 比较便宜

## 对于公开的视频，完全可以用 http fetch 自行解释 html 响应的方式获取数据

##

1: xvfb-run 可以让程序运行在一个虚拟的 xserver 上， 那么对于如果 Playwright 在 headless 的情况下功能不正常时，也许有点帮助。

## 另一个爬网引擎
<https://github.com/projectdiscovery/katana>

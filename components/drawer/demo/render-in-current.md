## zh-CN

渲染在当前 dom 里。自定义容器，查看 `getContainer`。

注意：在 v5 中 `style` 与 `className` 迁移至 Drawer 面板上与 Modal 保持一致，原 `style` 与 `className` 替换为 `rootStyle` 与 `rootClassName`。

## en-US

Render in current dom. custom container, check `getContainer`.

Note: `style` and `className` is move to Drawer panel in v5 which is align with Modal component. Origin `style` and `className` is replaced by `rootStyle` and `rootClassName`.

```css
.site-drawer-render-in-current-wrapper {
  position: relative;
  height: 200px;
  padding: 48px;
  overflow: hidden;
  text-align: center;
  background: #fafafa;
  border: 1px solid #ebedf0;
  border-radius: 2px;
}
```

<style>
[data-theme="dark"] .site-drawer-render-in-current-wrapper {
  background: #000;
  border: 1px solid #303030;
}
</style>

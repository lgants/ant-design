---
category: Components
group: Data Display
title: Tabs
cover: https://mdn.alipayobjects.com/huamei_7uahnr/afts/img/A*72NDQqXkyOEAAAAAAAAAAAAADrJ8AQ/original
---

Tabs make it easy to switch between different views.

### When To Use

Ant Design has 3 types of Tabs for different situations.

- Card Tabs: for managing too many closeable views.
- Normal Tabs: for functional aspects of a page.
- [Radio.Button](/components/radio/#components-radio-demo-radiobutton): for secondary tabs.

### Usage upgrade after 4.23.0

<Alert message="After version 4.23.0, we provide a simpler usage &lt;Tabs items={[...]} /&gt; with better performance and potential of writing simpler code style in your applications. Meanwhile, we deprecated the old usage in browser console, we will remove it in antd 5.0."></Alert>

```jsx
// works when >=4.23.0, recommended ✅
const items = [
  { label: 'Tab 1', key: 'item-1', children: 'Content 1' }, // remember to pass the key prop
  { label: 'Tab 2', key: 'item-2', children: 'Content 2' },
];
return <Tabs items={items} />;

// works when <4.23.0, deprecated when >=4.23.0 🙅🏻‍♀️
<Tabs>
  <Tabs.TabPane tab="Tab 1" key="item-1">
    Content 1
  </Tabs.TabPane>
  <Tabs.TabPane tab="Tab 2" key="item-2">
    Content 2
  </Tabs.TabPane>
</Tabs>;
```

## Examples

<!-- prettier-ignore -->
<code src="./demo/deprecated.tsx">Basic usage (deprecated syntactic sugar)</code>
<code src="./demo/basic.tsx">Basic</code>
<code src="./demo/disabled.tsx">Disabled</code>
<code src="./demo/centered.tsx">Centered</code>
<code src="./demo/icon.tsx">Icon</code>
<code src="./demo/slide.tsx">Slide</code>
<code src="./demo/extra.tsx">Extra content</code>
<code src="./demo/size.tsx">Size</code>
<code src="./demo/position.tsx">Position</code>
<code src="./demo/card.tsx">Card type tab</code>
<code src="./demo/editable-card.tsx">Add & close tab</code>
<code src="./demo/card-top.tsx">Container of card type Tab</code>
<code src="./demo/custom-add-trigger.tsx">Customized trigger of new tab</code>
<code src="./demo/custom-tab-bar.tsx">Customized bar of tab</code>
<code src="./demo/custom-tab-bar-node.tsx">Draggable Tabs</code>
<code src="./demo/animated.tsx" debug>Animated</code>
<code src="./demo/nest.tsx" debug>Nest</code>

## API

### Tabs

<!-- prettier-ignore -->
| Property | Description | Type | Default | Version |
| --- | --- | --- | --- | --- |
| activeKey | Current TabPane's key | string | - |  |
| addIcon | Customize add icon | ReactNode | - | 4.4.0 |
| animated | Whether to change tabs with animation. Only works while `tabPosition="top"` | boolean \| { inkBar: boolean, tabPane: boolean } | { inkBar: true, tabPane: false } |  |
| centered | Centers tabs | boolean | false | 4.4.0 |
| defaultActiveKey | Initial active TabPane's key, if `activeKey` is not set | string | - |  |
| hideAdd | Hide plus icon or not. Only works while `type="editable-card"` | boolean | false |  |
| items | Configure tab content | [TabItemType](#TabItemType) | [] | 4.23.0 |
| moreIcon | The custom icon of ellipsis | ReactNode | &lt;EllipsisOutlined /> | 4.14.0 |
| popupClassName | `className` for more dropdown. | string | - | 4.21.0 |
| renderTabBar | Replace the TabBar | (props: DefaultTabBarProps, DefaultTabBar: React.ComponentClass) => React.ReactElement | - |  |
| size | Preset tab bar size | `large` \| `middle` \| `small` | `middle` |  |
| tabBarExtraContent | Extra content in tab bar | ReactNode \| {left?: ReactNode, right?: ReactNode} | - | object: 4.6.0 |
| tabBarGutter | The gap between tabs | number | - |  |
| tabBarStyle | Tab bar style object | CSSProperties | - |  |
| tabPosition | Position of tabs | `top` \| `right` \| `bottom` \  | `left` | `top` |  |
| destroyInactiveTabPane | Whether destroy inactive TabPane when change tab | boolean | false |  |
| type | Basic style of tabs | `line` \| `card` \| `editable-card` | `line` |  |
| onChange | Callback executed when active tab is changed | function(activeKey) {} | - |  |
| onEdit | Callback executed when tab is added or removed. Only works while `type="editable-card"` | (action === 'add' ? event : targetKey, action): void | - |  |
| onTabClick | Callback executed when tab is clicked | function(key: string, event: MouseEvent) | - |  |
| onTabScroll | Trigger when tab scroll | function({ direction: `left` \| `right` \| `top` \| `bottom` }) | - | 4.3.0 |

More option at [rc-tabs tabs](https://github.com/react-component/tabs#tabs)

### TabItemType

| Property | Description | Type | Default |
| --- | --- | --- | --- |
| closeIcon | Customize close icon in TabPane's head. Only works while `type="editable-card"` | ReactNode | - |
| disabled | Set TabPane disabled | boolean | false |
| forceRender | Forced render of content in tabs, not lazy render after clicking on tabs | boolean | false |
| key | TabPane's key | string | - |
| label | TabPane's head display text | ReactNode | - |
| children | TabPane's head display content | ReactNode | - |

# 对话框 Dialog

执行之前，请确认。

<n-alert title="使用前提" type="warning">
  如果你想使用对话框，你需要把调用其方法的组件放在 <n-text code>n-dialog-provider</n-text> 内部并且使用 <n-text code>useDialog</n-text> 去获取 API。
</n-alert>

例如：

```html
<!-- App.vue -->
<n-dialog-provider>
  <content />
</n-dialog-provider>
```

```js
import { useDialog } from 'naive-ui'

// content
export default {
  setup () {
    const dialog = useDialog()
    return {
      warning () {
        dialog.warning(options)
      }
    }
  }
}
```

## 演示

```demo
basic
async
use-component
```

## API

### `useDialog` API

| 名称 | 类型 | 说明 |
| --- | --- | --- |
| destroyAll | `() => void` | 销毁所有弹出的对话框 |
| create | `(options: DialogOption) => DialogReactive` | 创建对话框 |
| error | `(options: DialogOption) => DialogReactive` | 调用 error 类型的对话框 |
| info | `(options: DialogOption) => DialogReactive` | 调用 info 类型的对话框 |
| success | `(options: DialogOption) => DialogReactive` | 调用 success 类型的对话框 |
| warning | `(options: DialogOption) => DialogReactive` | 调用 warning 类型的对话框 |

### DialogOption Properties

| 名称 | 类型 | 默认值 | 说明 |
| --- | --- | --- | --- |
| bordered | `boolean` | `false` | 是否显示 border |
| closable | `boolean` | `true` | 是否显示 close 图标 |
| content | `string \| (() => VNodeChild)` | `undefined` | 对话框内容，可以是 render 函数 |
| icon-placement | `'left' \| 'top'` | `'left'` | 图标的位置 |
| icon | `() => VNodeChild` | `undefined` | 对话框 icon, 需要是 render 函数 |
| loading | `boolean` | `false` | 是否显示 loading 状态 |
| negative-text | `string` | `undefined` | 不填对应的按钮不会出现 |
| positive-text | `string` | `undefined` | 不填对应的按钮不会出现 |
| show-icon | `boolean` | `true` | 是否显示 icon |
| title | `string \| (() => VNodeChild)` | `undefined` | 标题，可以是 render 函数 |
| type | `'error \| 'success' \| 'warning'` | `'warning'` | 对话框类型 |
| onClose | `() => boolean \| Promise<boolean> \| any` | `undefined` | 默认行为是关闭确认框。返回 `false` 或者 resolve `false` 或者 Promise 被 reject 会避免默认行为 |
| onNegativeClick | `() => boolean \| Promise<boolean> \| any` | `undefined` | 默认行为是关闭确认框。返回 `false` 或者 resolve `false` 或者 Promise 被 reject 会避免默认行为 |
| onPositiveClick | `() => boolean \| Promise<boolean> \| any` | `undefined` | 默认行为是关闭确认框。返回 `false` 或者 resolve `false` 或者 Promise 被 reject 会避免默认行为 |

### DialogReactive API

#### DialogReactive Properties

下列属性都可以被动态修改。

| 名称 | 类型 | 说明 |
| --- | --- | --- |
| bordered | `boolean` | 是否显示 border |
| closable | `boolean` | 是否显示 close 图标 |
| content | `string \| (() => VNodeChild)` | 对话框内容，可以是 render 函数 |
| icon-placement | `'left' \| 'top'` | 图标的位置 |
| icon | `() => VNodeChild` | 对话框 icon，需要是 render 函数 |
| loading | `boolean` | 是否显示 loading 状态 |
| negative-text | `string` | 不填对应的按钮不会出现 |
| positive-text | `string` | 不填对应的按钮不会出现 |
| show-icon | `boolean` | 是否显示 icon |
| title | `string \| (() => VNodeChild)` | 可以是 render 函数 |
| type | `'error \| 'success' \| 'warning'` | 对话框类型 |
| onClose | `() => boolean \| Promise<boolean> \| any` | 默认行为是关闭确认框。返回 `false` 或者 resolve `false` 或者 Promise 被 reject 会避免默认行为 |
| onNegativeClick | `() => boolean \| Promise<boolean> \| any` | 默认行为是关闭确认框。返回 `false` 或者 resolve `false` 或者 Promise 被 reject 会避免默认行为 |
| onPositiveClick | `() => boolean \| Promise<boolean> \| any` | 默认行为是关闭确认框。返回 `false` 或者 resolve `false` 或者 Promise 被 reject 会避免默认行为 |

#### DialogReactive Methods

| 名称    | 类型 | 说明        |
| ------- | ---- | ----------- |
| destroy | `()` | 关闭 Dialog |

## Props

### Dialog Props

| 名称 | 类型 | 默认值 | 说明 |
| --- | --- | --- | --- |
| bordered | `boolean` | `false` | 是否显示 border |
| closable | `boolean` | `true` | 是否显示 close 图标 |
| content | `string \| (() => VNodeChild)` | `undefined` | 对话框内容，可以是 render 函数 |
| icon | `() => VNodeChild` | `undefined` | 需要是 render 函数 |
| loading | `boolean` | `false` | 是否显示 loading 状态 |
| negative-text | `string` | `undefined` | 不填对应的按钮不会出现 |
| positive-text | `string` | `undefined` | 不填对应的按钮不会出现 |
| show-icon | `boolean` | `true` | 是否显示 icon |
| title | `string \| (() => VNodeChild)` | `undefined` | 对话框标题，可以是 render 函数 |
| type | `'error \| 'success' \| 'warning'` | `'warning'` | 对话框类型 |
| on-close | `() => void` | 关闭时执行的回调函数,默认行为是关闭确认框。返回 `false` 或者 resolve `false` 或者 Promise 被 reject 会避免默认行为 |
| on-negative-click | `() => void` | 执行 negative 时执行的回调函数，默认行为是关闭确认框。返回 `false` 或者 resolve `false` 或者 Promise 被 reject 会避免默认行为 |
| on-positive-click | `() => void` | 执行 positive 时执行的回调函数，默认行为是关闭确认框。返回 `false` 或者 resolve `false` 或者 Promise 被 reject 会避免默认行为 |

## Slots

### Dialog Slots

| 名称    | 参数 | 说明        |
| ------- | ---- | ----------- |
| action  | `()` | action 内容 |
| default | `()` | 对话框内容  |
| header  | `()` | header 内容 |
| icon    | `()` | icon 内容   |

# Input

Many years ago, people used punched card to input.

## Demos

```demo
basic
size
round
icon
password
disabled
clearable
autosize
pair
input-group
passively-activated
count
focus
```

## Props

### Input Props

| Name | Type | Default | Description |
| --- | --- | --- | --- |
| autofocus | `boolean` | `false` |  |
| autosize | `boolean \| { minRows?: number, maxRows?: number }` | `false` |  |
| clearable | `boolean` | `false` |  |
| default-value | `string \| [string, string] \| null` | `null` |  |
| disabled | `boolean` | `false` |  |
| input-props | `object` | `undefined` | The props of the input element inside the component. It doesn't work with `pair` input. |
| loading | `boolean` | `undefined` | Whether to show loading indicator. Set to non `undefined` value will take space for loading indicator. |
| maxlength | `number` | `undefined` |  |
| minlength | `number` | `undefined` |  |
| pair | `boolean` | `false` | Whether to input pairwise value. |
| passively-activated | `boolean` | `false` |  |
| placeholder | `string \| [string, string]` | `undefined` | Placeholder of input. When `pair` is `true`, placeholder is an array. |
| readonly | `boolean` | `false` |  |
| round | `boolean` | `false` |  |
| rows | `number` | `3` |  |
| separator | `string` | `undefined` | The separator bewteen pairwise inputs. |
| show-count | `boolean` | `false` | Whether to show word count. |
| show-password-toggle | `boolean` | `false` | Controls the display and hiding of passwords |
| size | `'small' \| 'medium' \| 'large'` | `'medium'` |  |
| type | `'text' \| 'password' \| 'textarea'` | `'text'` |  |
| value | `string \| [string, string] \| null` | `undefined` | Value of input. When `pair` is `true`, `value` is an array. |
| on-blur | `() => void` | `undefined` |  |
| on-change | `(value: string \| [string, string]) => void` | `undefined` |  |
| on-clear | `() => void` | `undefined` |  |
| on-focus | `() => void` | `undefined` |  |
| on-update:value | `(value: string \| [string, string]) => void` | `undefined` |  |

## Slots

### Input Slots

| Name      | Parameters | Description |
| --------- | ---------- | ----------- |
| prefix    | `()`       |             |
| suffix    | `()`       |             |
| separator | `()`       |             |

### Input Group Slots

| Name    | Parameters | Description |
| ------- | ---------- | ----------- |
| default | `()`       |             |

### Input Group Label Slots

| Name    | Parameters | Description |
| ------- | ---------- | ----------- |
| default | `()`       |             |

## Methods

### Input Methods

| Name  | Type       | Description          |
| ----- | ---------- | -------------------- |
| blur  | () => void | Blur input element.  |
| focus | () => void | Focus input element. |

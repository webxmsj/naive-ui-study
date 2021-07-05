# CHANGELOG

## 2.15.3 (2021-07-05)

### Feats

- `n-loading-bar` export `LoadingBarApi` type.
- `n-image` add `imgProps` prop.
- Add native `title` attributes to some components to enhance the experience.
- `n-tree` add `prefix` and `suffix` in TreeOption.
- `n-carousel` add `dot-placement` prop.
- `n-auto-complete` add `loading` prop, closes [#241](https://github.com/TuSimple/naive-ui/issues/241).
- `n-slider` add `tooltip` prop, closes [#362](https://github.com/TuSimple/naive-ui/issues/362).
- `n-input` add `loading` prop

### Fixes

- Fix `n-upload` `multiple=false` doesn't work for drag & drop, closes [#363](https://github.com/TuSimple/naive-ui/issues/363).
- Fix `n-dropdown`'s inner `<a />`'s style.
- Fix `n-menu` tooltip's inner `<a />`'s style, closes [#338](https://github.com/TuSimple/naive-ui/issues/338).
- Fix `n-carousel` doesn't work with `v-for` children.
- Fix `n-form` `label-align` prop not working, closes [#213](https://github.com/TuSimple/naive-ui/issues/213)
- Fix `n-data-table` fixed column shadow doesn't work when `max-height` is set, closes [#376](https://github.com/TuSimple/naive-ui/issues/376).

## 2.15.2 (2021-07-02)

### Feats

- `n-carousel` add `trigger` prop.
- `n-menu` add `dropdown-placement` prop.
- `n-upload` add `before-upload` prop.
- `n-image` add `alt` prop.
- Support the enter key on the numeric keypad.
- `n-spin` support `icon` slot for icon customizing, closes[#260](https://github.com/TuSimple/naive-ui/issues/260).
- `n-spin` add `rotate` prop fro slot icon to rotate.
- `n-form` export `FormItemRule` & `FormRules` type.
- `n-select` add `render-tag` prop.

### Fixes

- Fix `n-log` warn on highlight.js when no language is set, closes [#327](https://github.com/TuSimple/naive-ui/issues/327).
- Remove `n-calendar`'s useless `console.log`.
- Fix loading-bar disappears unexpectl, closes [#343](https://github.com/TuSimple/naive-ui/issues/343).
- Fix `n-select` doesn't scroll to selected item when menu is opened, closes [#346](https://github.com/TuSimple/naive-ui/issues/346).
- Fix `n-tab-pane` throws error when using v-if.
- Fix `n-modal` still closes when `on-negative-click` returns `false`.
- Fix `n-collapse` `defaultExpandedNames` does not work in accrodion mode, closes [#350](https://github.com/TuSimple/naive-ui/issues/350).
- Fix `n-tag` lacks `on-update-checked` prop.
- Fix `n-menu` `render-label` not working for dropdown in collapsed mode.

## 2.15.1 (2021-06-30)

- Fix no `web-types.json`.

## 2.15.0 (2021-06-29)

### Breaking Changes

- `n-select`'s `SelectOption`'s `render` no longer render label but the entire option.

### Feats

- `n-carousel` supports touch operation, closes [#271](https://github.com/TuSimple/naive-ui/issues/271).
- `n-input` add `input-props` prop.
- `n-message` optimize the error message of `useMessage` when there is no `n-message-provider`, add the related document link.
- Add `web-types.json` for webstorm, however I recommend using VSCode and Volar. `web-types.json` only provides limited information for coding.
- `n-tree-select` add `leaf-only` prop.
- `n-tree` add `leaf-only` prop.
- `n-select`'s `SelectOption`'s `label` supports render function.
- `n-select` add `render-option` prop.
- `n-select` export `SelectOption` & `SelectGroupOption` type.
- `n-popover` add `header` slot.
- `n-dropdown` add `render-label` prop.

### Fixes

- Fix `n-date-picker` `n-provider` pass `date-locale` not work, closes [#250](https://github.com/TuSimple/naive-ui/issues/250).
- Fix `n-input` clear button placeholder prevent clicking on actual component [#288](https://github.com/TuSimple/naive-ui/issues/288)
- Fix `n-carousel` click the at current item button, the component behaves abnormally.
- Fix `n-menu` `render-label` not working for tooltip in collapsed mode.
- Fix `n-dropdown` can't render `n-popover` in option.

## 2.14.0 (2021-06-23)

### Breaking Changes

- `n-element` removes `abstract` prop.
- `n-element` doesn't return theme variables in default slot. Please use `useThemeVars` instead.

### Feats

- Add `n-carousel` component.
- Add `useThemeVars` composable to provide theme variables.
- `n-upload` add `on-update:file-list` prop, closes [#135](https://github.com/TuSimple/naive-ui/issues/135).
- `n-date-picker` add `update-value-on-close` prop.

### Fixes

- Fix `n-select` can't input in filterable mode in single mode in iOS Safari, closes [#230](https://github.com/TuSimple/naive-ui/issues/230)
- Fix `n-input-number` lacks `on-update-value` prop.
- Fix `n-input-number`'s value can't be null.
- Fix `n-input-number`'s button doesn't work after value is cleared, closes [#251](https://github.com/TuSimple/naive-ui/issues/251).
- Fix `n-data-table` expand trigger's cursor is not pointer, closes [#261](https://github.com/TuSimple/naive-ui/issues/261).

## Refactors

- `n-input-number` will focus directly, closes [#244](https://github.com/TuSimple/naive-ui/issues/244).

## 2.13.0 (2021-06-21)

### Feats

- `n-dropdown` add `on-clickoutside` prop, closes [#123](https://github.com/TuSimple/naive-ui/issues/123).
- `n-menu` add `render-label` prop, closes [#84](https://github.com/TuSimple/naive-ui/issues/84)
- `n-tree` supports keyboard operations.
- Add `n-tree-select` component.

### Fixes

- Fix `n-tree` drag over leaf node causes error, closes [#200](https://github.com/TuSimple/naive-ui/issues/200).
- Fix `n-tree` misses `on-update-expanded-keys`, `on-update-selected-keys`, `on-update-checked-keys` prop.
- Fix `n-tree`'s `selected-keys` prop influences original array.
- Fix `n-select`'s input has useless empty row in multiple filterable mode.
- Fix `n-button`'s loading icon doesn't show on iOS Safari, closes [#219](https://github.com/TuSimple/naive-ui/issues/219).
- Fix `n-date-picker` doesn't show icon when clearable.
- Fix `n-time-picker` icon mis-aligned when clearable, closes [#222](https://github.com/TuSimple/naive-ui/issues/222).

## 2.12.2 (2021-06-19)

### Fixes

- Fix `n-form-item` always show require mark.

## 2.12.1 (2021-06-19)

### Feats

- `n-form`, `n-form-item` enhance `show-require-mark` prop，closes [#171](https://github.com/TuSimple/naive-ui/issues/171)
- `n-dropdown` support class attr, closes [#180](https://github.com/TuSimple/naive-ui/issues/180).
- `n-input` add `show-password-toggle` prop.
- `n-popselect` support class attr.
- `n-select` add `render-label` prop.
- `n-popselect` add `render-label` prop.

### Fixes

- Fix `n-input` baseline shifts when mix Chinese and English characters in input, closes [#174](https://github.com/TuSimple/naive-ui/issues/174).
- Fix `n-icon` use setup script, `$parent` is an empty object by default, and access `$parent.$options` will be `undefined`.
- Fix `n-notification` position not correct.
- Fix `n-message` content & option type not correct.

## 2.12.0 (2021-06-16)

### Breaking Changes

- `n-a`'s `to` prop is removed. Now if you want to use `n-a` like a router link, you can follow the doc site.

### Feats

- `n-tree` support `disabled` & `checkboxDisabled` on option.
- `n-input-number` support keyboard events ArrowUp and ArrowDown operations.

### Fixes

- Fix `n-cascader` text blur in win10 Chrome.
- Fix `n-tree` click on indent won't trigger select in block line mode.

## 2.11.12 (2021-06-16)

### Feats

- `n-drawer-content` add `closable` prop, closes [#139](https://github.com/TuSimple/naive-ui/issues/139).
- `n-element` pass `themeVars` to default slot.
- `n-element` add `abstract` prop.

### Fixes

- Fix `n-radio-group` doesn't trigger form item validation.
- Fix `n-auto-complete` customizing input not working.

## 2.11.11 (2021-06-15)

### Feats

- `n-tag` add `RTL` support

### Fixes

- Move `vue` & `vue-router` to peer dependencies to avoid redundant bundle.

## 2.11.9 (2021-06-15)

### Feats

- `n-space` supports wai-aria.
- `n-button-group` supports wai-aria.
- `n-progress` supports wai-aria.
- `n-menu` supports use `<a />` and `<router-link />` as label, closes [#84](https://github.com/TuSimple/naive-ui/issues/84).
- `n-input-number` add `show-button` prop.
- `n-rate` support `default` slot for icon customizing.
- `n-rate` add color prop.
- `n-rate` add size prop.

### Fixes

- Fix `n-card`'s `header-style` it not applied to header. [#103](https://github.com/TuSimple/naive-ui/issues/103)
- Fix `n-dialog` misses `destroyAll` method.
- Fix `n-data-table` misses `on-update-sorter`, `on-update-filters`, `on-update-page` and `on-update-page-size` props.

## 2.11.8 (2021-06-13)

### Feats

- `n-data-table` exports `DataTableCreateRowClassName`, `DataTableCreateRowKey` and `DataTableCreateRowProps` type.

### Fixes

- Fix `n-calendar`'s `on-update:value` prop type.
- Fix `n-form-item`'s style attribute `grid-template-columns` influence on the layout of child elements. [#93](https://github.com/TuSimple/naive-ui/pull/93)
- Fix `n-data-table`'s prop types of `rowKey`, `rowClassName`, `rowProps`, `summary` aren't compatible with expected value.

## 2.11.7 (2021-06-12)

### Fixes

- Fix `n-slider` doesn't prevent scrolling when touchstart.
- Fix `n-color-picker`'s default value doesn't follow modes.
- Fix not `lodash` & `lodash-es` type.

## 2.11.6 (2021-06-11)

### Feats

- `n-spin`'s `size` prop support number.
- `n-date-picker` add `footer` slot.

### Fixes

- Fix `n-slider` doesn't support touch events
- Fix `n-button` causes crash when it's imported in script inside head tag. [#68](https://github.com/TuSimple/naive-ui/pull/68)
- Fix `n-spin` animation shifts.
- Fix `n-menu` lack `on-update-value` and `on-update-expanded-keys` props.
- Fix `n-popconfirm` icon slot not working.
- Fix `n-tabs` logs useless info.
- Fix `n-color-picker` set `modes` not working. [#77](https://github.com/TuSimple/naive-ui/issues/77)

## 2.11.5 (2021-06-10)

### Feats

- `n-dropdown` add `disabled` prop
- `n-card` add `:target` style

### Fixes

- Fix `n-popover` sometimes won't sync position in manual mode.
- Fix `n-transfer`'s empty icon is no toggling transition.
- Fix `n-message` API option is not optional.
- Fix `n-calendar` date calculate incorrectly.
- Fix `n-input` misses the `password` type declaration.
- Fix `n-menu` the type definition of `extra` property of menu and submenu.
- Fix `n-dropdown` mouse cursor is not pointer.

## 2.11.4

### Feats

- `n-button` supports wai-aria.
- `n-card` supports wai-aria.
- `n-switch` supports wai-aria.
- `n-menu` supports basic wai-aria.
- `n-divider` supports basic wai-aria.
- `n-data-table` add `row-props` prop.
- `n-date-picker` add `ranges` prop.

### Fixes

- Fix `n-tab-pane` `display-directive` not working.
- Fix `n-drawer` animation.
- Fix `n-scrollbar`'s track may be overlayed in chrome windows.

## 2.11.3

- Fix `n-collapse` `default-expanded-names` not working.

## 2.11.2

### Fixes

- Fix `n-dropdown` default placement is not `bottom`.
- Fix `n-date-picker`'s input theme is not set in `date` & `datetime` type.
- Fix `n-config-provider` doesn't merge inherited theme.

### Feats

- `n-collapse` add `arrow` slot

## 2.11.1

Update package.json & README.md.

## 2.11.0

### Breaking Changes

- `n-affix`'s `listen-to` prop is `document` by default (first scrollable parent before).

### Feats

- `n-affix`'s `listen-to` prop support `Window | Document | HTMLElement`.
- `n-anchor` add `offset-target` prop.
- `n-select` add `virtual-scroll` prop.
- `n-select` add `consistent-menu-width` prop.
- `n-date-picker` update value after confirm is clicked.

### Fixes

- Fix `n-date-picker` doesn't disable start date correctly when value is empty.
- Fix `n-input-number` not restore valid value after blur.
- Fix `n-date-picker` display selected date when value is null in date mode.

### Deprecated

- `n-affix`'s `offset-top` prop is deprecated, please use `trigger-top` instead.
- `n-affix`'s `offset-bottom` prop is deprecated, please use `trigger-bottom` instead.
- `n-anchor`'s `listen-to` prop is removed.

## 2.10.0

### Breaking Changes

- `n-popover`'s `placement` prop default value is set to `'top'`.

### Feats

- `n-tabs` add `on-close` prop.
- `n-tabs` add `on-add` prop.
- `n-tabs` add `tab` slot.
- `n-tab-pane`'s `tab` prop support render function & VNode.
- `n-tabs`'s `type` prop support `'line'` option.
- `n-tabs` add box shadow to indicate scroll status.
- `n-tabs` add `pane-style` prop

### Fixes

- Fix `n-layout`'s `scrollTo` not working when using native scrollbar.

### Deprecated

- `n-tab-pane`'s `label` prop is deprecated. Please use `tab` prop instead.

## 2.9.0

### Breaking Changes

- `n-layout-sider` removed `show-content` prop. Please use `show-collapsed-content` instead.

### Feats

- `n-data-table` support tree data.
- `n-data-table` add `cascade` prop.
- `n-data-table` add `children-key` prop.
- `n-data-table` add `indent` prop.
- `n-button` add `tag` prop.
- `n-data-table` add `table-layout` prop.
- `n-tree` add `block-line` prop.
- `n-tree` support drag & drop.
- `n-menu` add `inverted` prop.
- `n-dropdown` add `inverted` prop.
- `n-tabs` add `addable` prop.
- `n-tabs` add `tab-style` prop.
- `n-tabs` add `tabs-padding` prop.
- `n-tabs` add `default-value` prop.
- `n-layout-sider` & `n-layout-footer` & `n-layout-header` add `inverted` prop.
- `n-data-table`'s `max-height` & `min-height` prop accept CSS value.
- `n-layout` & `n-layout-content` add `embedded` prop.

### Fixes

- `n-layout` & `n-layout-sider`'s `scrollTo` not working with native scrollbar.
- `n-layout-sider`'s `collapse-mode` not working.
- Internal selection component's theme peers has wrong key for popover.

## 2.8.0

### Perf

- Optimize `n-data-table` init render count.
- Optimize `n-select` open duration after first opening.
- Optimize `n-anchor` scroll performance.

### Feats

- `n-tree` add `virtual-scroll` prop.
- `n-data-table` add `virtual-scroll` prop.
- `n-cascader` add `virtual-scroll` prop.
- `n-pagination` add `item-count` prop.
- `n-pagination` add `prefix` prop.
- `n-pagination` add `prefix` slot.
- `n-pagination` add `suffix` prop.
- `n-pagination` add `suffix` slot.
- `n-input` add `show-count` prop.

### Fixes

- Fix `n-layout-sider` doesn't show menu after collapsed.
- Fix `n-input-number` doesn't reset to origin value when blur with invalid value.
- Fix `n-pagination` doesn't update page in uncontrolled mode.

## 2.7.4

### Feats

- `n-form-item` works without `n-form`.

### Fixes

- Fix `n-checkbox` check mark not displayed.
- Fix `n-date-picker` icon transition style in trigger.
- Fix `n-p`, `n-ol`, `n-ul` margin bottom is not 0 when they are last child.
- Fix `n-checkbox-group` not working in uncontrolled mode.
- Fix `n-data-table` clear check all in table now working.

## 2.7.3

### Feats

- `n-data-table` highlight sorted col.
- `n-data-table` col add `render-filter` prop.
- `n-data-table` col add `render-filter-icon` prop.

### Fixes

- `n-data-table` fixed column box-shadow more clear in dark theme.
- Fix `n-color-picker` value has line wrap.
- Fix `n-form` FormRuleItem.trigger types.

## 2.7.2

### Feats

- `n-data-table` add `summary` prop.
- `n-data-table` add `options` on `'type=selection'` column.

### Fixes

- Fix `n-layout` overflow on horizontal direction.

## 2.7.1

### Feats

- `n-checkbox` add `focusable` prop.
- `n-cascader` add `action` slot.

### Fixes

- Fix `n-cascader` loading triggered when click checkbox.
- Fix `n-cascader` menu mask style.

## 2.7.0

### Breaking Changes

- `n-drawer` doesn't have padding by default. `n-drawer-content` is provided to fill the drawer.

## 2.6.0

### Feats

- `n-drawer` add `content-style` prop.
- `n-layout` add `content-style` prop.
- `n-layout-sider` add `content-style` prop.

### Feats

- `n-config-provider` Add `cls-prefix` prop.

### Fixes

- Fix `n-popover` may influence other popover when static props is hoisted.

## 2.5.1

### Feats

- `n-color-picker` add `show-alpha` prop.

### Fixes

- Fix `n-select` default `fallback-option` breaks the component.

## 2.5.0

### Feats

- Add `n-skeleton` component.
- Add `n-calendar` component.
- Add `n-color-picker` component.
- `n-date-picker` locale add `firstDayOfWeek`.
- `n-select` add `showArrow` prop.

### Fixes

- Fix `n-date-picker` trigger has no focus style in focus is in panel.
- Fix `n-button` loading's fade-in transtion drifts.
- Fix `n-time-picker` close animation drifts in `n-date-picker`.
- Fix detached components in popover should stay in popover.

## 2.4.2

### Feats

- Add `n-form-item-gi` component.

### Fixes

- Fix `n-ellipsis` & `n-data-table` ellpisis cell mis-vertical-aligned.
- Fix `n-select` filterable doesn't work with composite events.

## 2.4.1

### Fixes

- Fix `n-select` caret color in single filter mode.
- Fix `n-select` menu action part can't be focused.

## 2.4.0

### Feats

- Add `n-image` component.
- Add `n-global-style` component.
- Add `n-theme-editor` component.
- Add `n-page-header` component.
- `n-statistic` add `label` slot.
- `n-breadcrumb-item` add `separator` slot & prop.
- `n-button` add `bordered` prop.
- `n-card` add `footer-style` prop.

### Refactors

- Refactor `n-statistic`'s style
- `n-menu` add `options` prop to replace `items` prop, `items` prop is deprecated.

### Fixes

- Fix `n-anchor` `ignore-gap` not working
- Fix `n-collapse` content is truncated by `overflow: hidden`.
- Fix `n-select` tag text overflow.
- Fix `n-popover` doesn't hide as expected in mobile phone.

## 2.3.1

### Fixes

- Fix `n-layout-sider` horizontal content overflows.

## 2.3.0

### Breaking Changes

- Collapsing won't work for `n-layout-sider` with `position="absolute"`.
- For `n-layout` contains `n-layout-sider` as a direct child `has-sider` must be set.

## 2.2.0

### Feats

- Add `n-mention` component.
- `n-data-table` supports expanding rows.

### Fixes

- Fix `n-input` focused background color not correct in warning & error status in dark theme.
- Fix `n-input` caret color not correct in warning & error status.
- Fix `n-select`'s namespace not correct.
- Fix `n-cascader`'s namespace not correct.
- Fix `n-input` in textarea mode can't select text.
- Fix `n-input` in textarea mode has no box-shadow.
- Fix `n-input` in textarea mode `autosize` line not correct due to inconsistant font family.
- Fix `n-input` in textarea mode `autosize` rows not changed if props.value is changed from outside.

### Refactors

- Change `n-empty`'s icon and make it size larger

## 2.1.3

### Fixes

- Fix `n-data-table` has no right border of non-last td.
- Fix `n-data-table` header has no enough width when table width is more than `scroll-x`

## 2.1.2

### Feats

- `n-data-table`'s column add `colSpan` and `rowSpan` prop.
- `n-data-table`'s column add `titleColSpan` prop.

### Fixes

- Fix `n-dropdown` with `x` and `y` set logs errors when mouse move outside it.

## 2.1.1

### Fixes

- Fix `n-select` selection overflow counter wrong popover trigger area

## 2.1.0

### Breaking Changes

- `n-popover` default `duration` is set to `100`.
- `n-popover` default `delay` is set to `100`.
- `n-tooltip` default `showArrow` is set to `true`.

### Feats

- `n-config-provider` prop `theme-overrides` support inheritance.
- `n-card` add `hoverable` prop.
- `n-select` add `max-tag-count` prop.
- `n-cascader` add `max-tag-count` prop.
- `n-popover` add `get-disabled` prop.
- add `n-ellipsis` component.
- `n-popover`'s `width` prop add `'trigger'` option.
- `n-data-table`'s columns's `ellipsis` prop can be set as props of `n-ellipsis`.

### Fixes

- Fix `n-cascader` menu appears after click clear button.
- Fix `n-card`'s action not placed at bottom after style height is set.
- Fix `n-popover`'s `duration` and `delay` prop works unexpectly.

## 2.0.1

### Feats

- `n-layout-sider` add `default-collapsed` prop.
- `n-modal` support custom position.

### Fixes

- Fix `n-menu` tooltip of `n-menu-item` won't show when vertical collapsed.
- Fix `n-menu` `collapsed-icon-size` not working.
- Fix `n-menu` callback props validate array with error.
- Fix `n-layout-sider` toggle button is covered.

## 2.0.0

See vue3.md

## 1.6.0

### Fixes

- Fix the problem that `n-auto-complete`'s menu can't be closed when use `textarea` as input.
- Fix the problem that nested `n-icon` is not flattened.
- Fix the problem that `n-date-picker` has no year in panel when type is `date` and `datetime`.

### Features

- `n-button` add `dashed` props
- Add `n-space` component.
- Make `n-drawer` content scrollable.

### Localization

- Add zhCN for `n-log`

## 1.5.5 (2020-08-15)

### Breaking Changes

- Fix all typos of `separator`. (Originally it was `seperator`.)

### Fixes

- Fix the problem that when theme is not set, style errors will be logged.
- Fix the text color of `n-select`'s placeholder when `single` `filterable`.

## 1.5.4 (2020-08-08)

### Fixes

- Fix the problem that Message, Notification, Confirm doesn't follow theme change.

## 1.5.3 (2020-07-23)

### Fixes

- Fix the problem that `n-select` display with mistakes when `placeholder` is empty.

## 1.5.2 (2020-07-22)

### Fixes

- Fix the problem that `n-radio` can not be focused.
- Fix the problem that `n-data-table`'s `max-height` style is broken. https://bugs.chromium.org/p/chromium/issues/detail?id=1107223

### Refactors

- Refactor `n-tag` styles.

## 1.5.1 (2020-07-20)

### Features

- Add `disabled` for `n-time-picker`.

### Fixes

- Fix the child elements of `n-radio` cannot focus.

## 1.5.0 (2020-07-09)

### Breaking Changes

- Refactor experimental setting primary color feature.

### Fixes

- Fix some style glitches.

## 1.4.1 (2020-06-23)

### Features

- Add `autofocus` for `n-select`.

## 1.4.0 (2020-06-19)

### Breaking Changes

- `n-menu` doesn't support slot API anymore.

### Features

- Add experimental setting primary color feature.

## 1.3.5 (2020-06-06)

### Features

- Add `attr-type` for `n-button`

### Fixes

- Fix the problem that if `n-input` is too width, its inner input elements' width won't expand.
- Fix style glitches of border of a `n-input-number` inside a `n-input-group`.

## 1.3.4 (2020-06-05)

### Fixes

- Fix the problem that `n-a`'s `to` prop can't be a object.

## 1.3.3 (2020-06-03)

### Features

- Add `$NOs.theme` to get the current theme of the OS.

## 1.3.2 (2020-06-02)

### Fixes

- Fix the problem that `n-log`'s loading indicator uses monospace font.
- Fix the problem that icon-related class name isn't applied properly.

## 1.3.1 (2020-06-01)

### Fixes

- Fix the problem that checkbox in the selection column of `n-data-table` is not center aligned.
- Fix the problem that header of `n-data-table` has no border-color transition.
- Fix the problem that `show-icon` & `closable` & `bordered` props of `$NConfirm` don't work.

### Features

- Add and adjust some colors in the style scheme of `n-config-consumer`.

## 1.3.0 (2020-06-01)

### Breaking Changes

- Default UI CSS bundle won't include external font files. If you need using it you should import it explicitly.

### Features

- Add `themed-style` prop on `n-layout`.

### Fixes

- Fix the problem that round toggle button won't rotate `n-layout-sider` when collapsed status is changed.
- Fix the problem that `n-form-item`'s feedback has no leave animation if it is set at first.
- Fix the problem that max-height related styles of `n-data-table` are applied all the time.
- Fix some style glitches.

### Refactors

- Refactor some components' styles in the light theme.

## 1.2.1 (2020-05-29)

### Fixes

- Fix the problem that `n-slider` tooltip has no z-index.

## 1.2.0 (2020-05-29)

### Features

- Add `feedback` and `validation-status` props for `n-form-item`.

## 1.1.5 (2020-05-28)

### Features

- Add `display-directive` prop for `n-collapse` and `n-collapse-item`.
- Add `class` and `style` prop for `n-select`'s `option`.
- Add `debug` prop for `n-select`.

### Fixes

- Fix the problem that `n-select` can still be cleared when disabled.

## 1.1.4 (2020-05-28)

### Fixes

- Fix the problem that the input value of `n-select` may be modified directly.

### Refactors

- An UI instance can be install to a Vue instance for no more than once.

## 1.1.3 (2020-05-20)

### Chores

- Update css-render dependencies.

### Fixes

- Fix the problem that `n-transfer`'s animation disorder when value changes.

## 1.1.2 (2020-05-19)

### Features

- Add content slot for `n-step`.
- Add `label` prop for `n-checkbox`.

### Performance Improvements

- All placeable components register listeners on demand.
- Use cache when finding scrollable parent node.
- Imporve performance of `n-button`'s beforeDestroy.
- Reduce the useless re-rendering of `n-checkbox` when checked status isn't changed.
- Imporve performance of text typed `n-avatar`.

## 1.1.1 (2020-05-18)

### Fixes

- Update css-render dependencies.
- Color of default typed button icon.

### Performance Improvements

- Reduce useless re-renders of `n-menu-item`.
- Reduce useless re-renders of doc page.

### Refactors

- Refactor the codes of `n-nimbus-service-layout` for performance reason, may be there will be some bugs.

## 1.1.0 (2020-05-16)

### Features

- `n-button` now accepts custom color.

### Refactors

- Replace all $slots by $scopedSlots for better robustness.
- Move some static button styles inside button component to create dynamically.

## 1.0.14 (2020-05-15)

### Fixes

- Fix the problem that `line` typed `n-tabs`'s line position stays still when `activeName` changes.
- Fix the problem that `n-tabs` scroll button is not triggered when tabs' width changes.
- Fix the problem that height change of `n-tabs` will unexpectly trigger some re-render callbacks.

## 1.0.13 (2020-05-14)

### Fixes

- Fix the problem that label slot of the `n-form-item-col` & `n-form-item-row` cannot display.

## 1.0.12 (2020-04-30)

### Fixes

- Fix the problem that some CSS length props are badly formated.

## 1.0.11 (2020-04-30)

### Features

- Add `fallback-option` prop for `n-select` to deal with the value with no corresponding option.

### Fixes

- Fix the problem that `max-height` and `min-height` are ill displayed on `n-data-table`.

### Breaking Changes

- `n-data-table`'s `max-height` and `min-height` will be applied to the entire table part, not only body.
- `n-select` will display value with no corrensponding option.

## 1.0.10 (2020-04-28)

### Features

- Add `arrow-placement` prop on `n-collapse`.
- Add `arrow` slot on `n-collapse-item`.

### Fixes

- Fix the problem that detachable components detached in wrong place when nested like `modal > drawer > component`.

## 1.0.9 (2020-04-23)

### Features

- Add `autofocus` prop on `n-input`.
- Add `closable` option on `NMessage`.

### Fixes

- Fix the problem that the default value of `n-tag` `closable` is set to `true`.
- Fix the problem that `n-data-table` can't use all `pagination`'s props.
- Fix the problem that `n-pagination`'s `on-page-size-change` prop doesn't work.

## 1.0.8 (2020-04-22)

### Features

- Add `n-dynamic-tags`.
- Add `tableHeaderOverlayBackgroundColor` & `inputOverlayBackgroundColor` to `styleScheme`

## 1.0.7 (2020-04-10)

### Features

- Add `filter-option-value` prop for `n-data-table`'s `column` to better deal with single filter mode.

### Fixes

- Fix the problem that `n-collpase-item` don't support `number` typed `name`.

## 1.0.6 (2020-04-03)

### Fixes

- Fix the problem that all the `console` statements are stripped in the bundle.

## 1.0.5 (2020-03-27)

### Features

- Change the data type of `n-data-table`'s filters from Array to Object.

### Fixes

- `n-data-table` cannot be filtered correctly when there are multiple filtered columns.

## 1.0.4 (2020-03-26)

### Features

- Filter menu in `n-data-table` is scrollable when there are too many items.

## 1.0.3 (2020-03-25)

### Features

- `$NMessage`, `$NNotification`, `$NConfirm`'s theme will be applied on their children components.

### Fixes

- View measuring element will confict when multiple naive-ui exist.
- `validate` method of `n-form-item` won't be resolved for some validator.
- `$NConfirm`'s theme doesn't follow `n-config-provider`'s theme.

## 1.0.2 (2020-03-23)

### Fixes

- `n-transfer`'s options are not reinitialized after value changes.
- `n-nimbus-service-layout` (deprecated) doesn't deal with the compatibility of Vue Router(under 3.1)'s `push` method.

## 1.0.1 (2020-03-21)

### Features

- Add `'bar'` & `'arrow-circle'` on `show-trigger` prop of `n-layout-sider`.

### Fixes

- Rails of `n-scrollbar` shadow mouse event.

### Features

- `n-date-table` add `empty` slot. [#86](https://github.com/TuSimple/naive-ui/issues/86)

## Slider

A form element that allows users to select a value from a specified range by sliding a handle along a track.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `fullWidth` | `boolean` | | | `false` |
| `inline` | `boolean` | (Part of Config type, but not directly used in this component's logic) | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `maximumValue` | `number` | The maximum value of the slider. | | `undefined` |
| `meta` | `MetaShape` | Additional metadata for the field. | | `undefined` |
| `minimumValue` | `number` | The minimum value of the slider. | | `undefined` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `step` | `number` | The granularity with which the slider can step through values. | | `undefined` |
| `variant` | `keyof typeof Variant` | Specifies the visual style of the component. | | `'standard-inlined'` |

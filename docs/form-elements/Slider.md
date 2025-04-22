# Slider

A form element that allows users to select a value from a specified range by sliding a handle along a track.

## Props

| Name           | Type                               | Description                                                               | Required | Default           |
| :------------- | :--------------------------------- | :------------------------------------------------------------------------ | :------- | :---------------- |
| `label`        | `string`                           | The text label displayed for the slider.                                  | Yes      |                   |
| `fullWidth`    | `boolean`                          | If true, the component takes up the full width of its container.          | No       | `false`           |
| `margin`       | `'none' \| 'dense' \| 'normal'`    | Defines the margin spacing around the control.                            | No       | `'normal'`        |
| `required`     | `boolean`                          | Marks the field as required, often indicated visually.                    | No       | `false`           |
| `paddingBottom`| `'none' \| 'dense' \| 'normal'`    | Defines the bottom padding spacing.                                       | No       | `undefined`       |
| `minimumValue` | `number`                           | The minimum value of the slider.                                          | No       | `undefined`       |
| `maximumValue` | `number`                           | The maximum value of the slider.                                          | No       | `undefined`       |
| `step`         | `number`                           | The granularity with which the slider can step through values.            | No       | `undefined`       |
| `variant`      | `keyof typeof Variant`             | The visual style variant of the form control. (Currently fixed internally) | No       | `'standard-inlined'` |
| `inline`       | `boolean`                          | (Part of Config type, but not directly used in this component's logic)    | No       | `false`           |
| `meta`         | `MetaShape`                        | Additional metadata for the field.                                        | No       | `undefined`       |
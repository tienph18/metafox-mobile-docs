# SFTabSelect

A form element that renders a horizontal list of tabs, allowing the user to select one option. The selected value is stored in the form state.

## Props

Props are passed via the `config` object within the form definition.

| Name      | Type                                                               | Description                                                                                                                               | Required | Default   |
| :-------- | :----------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------- | :------- | :-------- |
| `options` | `Array<{ label: string, value: any, showWhen?: Record<string, any> }>` | An array of objects defining the tabs. Each object should have a `label` (display text) and a `value`. Can include `showWhen` conditions. | Yes      | `[]`      |
| `bounces` | `boolean`                                                          | Determines if the horizontal tab list bounces when scrolled to the end.                                                                   | No       | `false`   |
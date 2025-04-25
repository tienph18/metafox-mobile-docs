## SFTabSelect

A form element that renders a horizontal list of tabs, allowing the user to select one option. The selected value is stored in the form state.

*Note: This element is only used in a search form.*

### Props

Props are passed via the `config` object within the form definition.

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `bounces` | `boolean` | Determines if the horizontal tab list bounces when scrolled to the end. | | `false` |
| `options` | `Array<{ label: string, value: any, showWhen?: Record<string, any> }>` | An array of objects defining the tabs. Each object should have a `label` (display text) and a `value`. Can include `showWhen` conditions. | Yes | `[]` |

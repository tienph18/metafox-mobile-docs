# Row

Renders child form elements horizontally in a row, allowing control over their alignment.

## Props

| Name           | Type                                                                                   | Description                                                    | Required | Default         |
| -------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------- | -------- | --------------- |
| `elements`     | `Record<string, FormElementConfig>`                                                    | Configuration for child form elements to render within the row | Yes      |                 |
| `justifyContent` | `'space-between' \| 'flex-start' \| 'flex-end' \| 'center' \| 'space-around' \| 'space-evenly'` | Specifies the alignment of child elements along the main axis. | No       | `'space-between'` |
| `style`        | `ViewStyle`                                                                            | Custom styles applied to the row container.                    | No       |                 |
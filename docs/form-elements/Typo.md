# Typo

Renders styled text content within a form, suitable for labels, descriptions, or simple HTML snippets.

## Props

| Name            | Type     | Description                                                              | Required | Default     |
| --------------- | -------- | ------------------------------------------------------------------------ | -------- | ----------- |
| `label`         | `string` | The main text label to display.                                          | No       | `undefined` |
| `numberOfLines` | `number` | Maximum number of lines for the label and description.                   | No       | `undefined` |
| `plainText`     | `string` | HTML content to render. Takes precedence over label/description if provided. | No       | `undefined` |
| `description`   | `string` | Additional descriptive text displayed below the label.                   | No       | `undefined` |
| `style`         | `object` | Custom style object for the label.                                       | No       | `undefined` |
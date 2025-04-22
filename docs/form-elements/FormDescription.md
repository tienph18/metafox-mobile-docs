# FormDescription

Displays a description text within a form, supporting simple HTML content.

## Props

| Name          | Type   | Description                                                    | Required | Default     |
| ------------- | ------ | -------------------------------------------------------------- | -------- | ----------- |
| `style`       | object | Custom styling for the description container View.             | No       | `{}`        |
| `description` | string | The text content to display. Can contain simple HTML.        | No       | `null`      |
| `numberOfLines`| number | Limits the number of lines displayed for the description text. | No       | `undefined` |
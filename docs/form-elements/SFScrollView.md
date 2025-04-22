# SFScrollView

A form element that renders its child elements within a horizontal ScrollView. It allows users to scroll horizontally through a set of form inputs or components.

## Props

| Name          | Type                                | Description                                                                          | Required | Default         |
| ------------- | ----------------------------------- | ------------------------------------------------------------------------------------ | -------- | --------------- |
| `elements`      | `Record<string, ElementConfig>` | Defines the child form elements to render within the scroll view.                  | Yes      | N/A             |
| `paddingBottom` | `string`                            | Sets the bottom padding of the scroll view. If set to 'none', padding is 0. | No       | `paddingBase` |
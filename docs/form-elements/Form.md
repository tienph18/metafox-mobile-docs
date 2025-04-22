# Form

The `Form` element acts as a container for rendering other form elements. It provides layout options and handles scrolling, including keyboard awareness and integration with bottom sheets. When `scrollable` is enabled, it groups elements into `top`, `bottom`, `full_space`, and other categories for layout purposes.

## Props

| Name                  | Type                   | Description                                                                                                | Required | Default |
| :-------------------- | :--------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :------ |
| `elements`            | `Record<string, any>`  | An object containing configurations for nested form elements.                                                | Yes      | `{}`    |
| `isBottomSheet`       | `boolean`              | If true, adapts scrolling behavior for use within a bottom sheet.                                          | No       | `false` |
| `scrollable`          | `boolean`              | If true, wraps the main elements in a scrollable container with keyboard awareness.                          | No       | `false` |
| `disableContainerStyle` | `boolean`              | If true and `scrollable` is true, disables the default `flex: 1` style applied to the scroll container. | No       | `false` |
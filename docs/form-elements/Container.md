## Container

The `Container` element acts as a layout wrapper for grouping other form elements. It provides options for labeling, description, different layout variants (vertical, horizontal, livestream), and optional collapsibility.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `className` | `string` | CSS class name for the wrapper (primarily for web). | | `undefined` |
| `collapsed` | `boolean` | Sets the initial collapsed state when `collapsible` is true. | | `false` |
| `collapsible` | `boolean` | If true, allows the user to collapse and expand the container. | | `false` |
| `description` | `string` | | | `undefined` |
| `elements` | `Record<string, FormFieldConfig>` | An object defining the form elements nested within this container. | Yes | `{}` |
| `full_space` | `boolean` | When true, the container attempts to occupy full available space. | | `false` |
| `label` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `sx` | `object` | Style object for applying custom styles to the root wrapper component. | | `{}` |
| `variant` | `'vertical' \| 'horizontal' \| 'livestream'` | Specifies the visual style of the component. | | `'vertical'` |
| `wrapAs` | `React.ElementType` | A custom React component to use as the wrapper instead of the default `View`. | | `undefined` |
| `wrapperProps` | `object` | Additional props to pass directly to the root wrapper component. | | `{}` |

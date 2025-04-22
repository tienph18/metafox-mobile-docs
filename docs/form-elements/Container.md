# Container

The `Container` element acts as a layout wrapper for grouping other form elements. It provides options for labeling, description, different layout variants (vertical, horizontal, livestream), and optional collapsibility.

## Props

| Name          | Type                                        | Description                                                                 | Required | Default      |
|---------------|---------------------------------------------|-----------------------------------------------------------------------------|----------|--------------|
| `label`       | `string`                                    | The main label displayed above the contained elements.                      | No       | `undefined`  |
| `description` | `string`                                    | Additional descriptive text displayed below the label.                      | No       | `undefined`  |
| `elements`    | `Record<string, FormFieldConfig>`           | An object defining the form elements nested within this container.          | Yes      | `{}`         |
| `variant`     | `'vertical' \| 'horizontal' \| 'livestream'` | Controls the layout arrangement of elements.                                | No       | `'vertical'` |
| `collapsible` | `boolean`                                   | If true, allows the user to collapse and expand the container.              | No       | `false`      |
| `collapsed`   | `boolean`                                   | Sets the initial collapsed state when `collapsible` is true.                | No       | `false`      |
| `required`    | `boolean`                                   | Marks the container's label as required (visually).                         | No       | `false`      |
| `wrapAs`      | `React.ElementType`                         | A custom React component to use as the wrapper instead of the default `View`. | No       | `undefined`  |
| `wrapperProps`| `object`                                    | Additional props to pass directly to the root wrapper component.            | No       | `{}`         |
| `className`   | `string`                                    | CSS class name for the wrapper (primarily for web).                         | No       | `undefined`  |
| `sx`          | `object`                                    | Style object for applying custom styles to the root wrapper component.      | No       | `{}`         |
| `full_space`  | `boolean`                                   | When true, the container attempts to occupy full available space.           | No       | `false`      |
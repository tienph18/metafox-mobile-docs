# MentionInput

The `MentionInput` element provides a text input field specifically designed for composing messages that can include user mentions (@username) and hashtags (#tag). It integrates with Formik for state management and validation.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :------- | :------ |
| `label` | `string` | The text label displayed above the input field. | Yes | `''` |
| `required` | `boolean` | Indicates if the field is mandatory. | | `false` |
| `variant` | `'standard'`, `'outlined'`, `'filled'`, `'standard-inlined'` | The visual style variant of the input. | | `'standard-inlined'` |
| `margin` | `'none'`, `'dense'`, `'normal'` | Controls the margin around the component. | | `'normal'` |
| `fullWidth` | `boolean` | If true, the input stretches to the full width of its container. | | `false` |
| `paddingBottom` | `'none'`, `'dense'`, `'normal'` | Controls the bottom padding of the component. | | `'none'` |
| `editable` | `boolean` | If false, the text content cannot be modified by the user. | | `true` |
| `testId` | `string` | A unique identifier used for testing purposes. | | `''` |
| `meta` | `MetaShape` | Additional metadata associated with the field. | | `{}` |
| `inputWrapperStyle` | `ViewStyle` | Custom styles applied to the input's wrapping element. | | `{}` |
| `containerStyle` | `ViewStyle` | Custom styles applied to the main container element. | | `{}` |
| `styleLabel` | `ViewStyle` | Custom styles applied to the label element. | | `{}` |
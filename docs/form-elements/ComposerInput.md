## ComposerInput

A specialized text input field designed for composer interfaces within MetaFox forms. It renders an input area that, when pressed, opens a bottom sheet for text entry. It supports dynamic height adjustment based on content.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none' \| 'sentences' \| 'words' \| 'characters'` | Controls automatic capitalization behavior. | | `undefined` |
| `autoCorrect` | `boolean` | Enables or disables auto-correction. | | `undefined` |
| `autoFocus` | `boolean` | | | `false` |
| `clearButtonMode` | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | (iOS only) When to display the standard clear button. | | `undefined` |
| `contextualDescription` | `string` | Additional description text, often appended with the current field value. | | `undefined` |
| `description` | `string` | | | `undefined` |
| `disabled` | `boolean` | | | `false` |
| `findReplace` | `{ find: string, replace: string }` | Defines patterns for automatic find-and-replace operations on the value. | | `undefined` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | | `undefined` |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `maxLength` | `number` | | | `undefined` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

# SFFilterPrice

The `SFFilterPrice` element provides a form input for selecting a price range (minimum and maximum). It displays the selected range and opens a bottom sheet for users to enter or modify the 'from' and 'to' price values.

## Props

| Name                 | Type                     | Description                                                          | Required | Default        |
| :------------------- | :----------------------- | :------------------------------------------------------------------- | :------- | :------------- |
| `label`              | `string`                 | The main label displayed for the filter element.                     | Yes      | -              |
| `fromFieldName`      | `string`                 | The formik field name for the minimum price value.                   | No       | `'price_from'` |
| `toFieldName`        | `string`                 | The formik field name for the maximum price value.                   | No       | `'price_to'`   |
| `fromFieldLabel`     | `string`                 | Label for the minimum price input in the bottom sheet.               | No       | -              |
| `toFieldLabel`       | `string`                 | Label for the maximum price input in the bottom sheet.               | No       | -              |
| `fromFieldPlaceholder` | `string`                 | Placeholder text for the minimum price input in the bottom sheet.    | No       | -              |
| `toFieldPlaceholder` | `string`                 | Placeholder text for the maximum price input in the bottom sheet.    | No       | -              |
| `variant`            | `string`                 | Specifies the visual style ('standard', 'standard-outlined', etc.).  | No       | `'standard'`   |
| `fullWidth`          | `boolean`                | Controls if the element takes the full available width.              | No       | `false`        |
| `margin`             | `string`                 | Sets the margin around the element ('none', 'dense', 'normal').      | No       | -              |
| `paddingBottom`      | `string`                 | Sets the padding below the element ('none', 'dense', 'normal').      | No       | -              |
| `required`           | `boolean`                | Marks the field as required.                                         | No       | `false`        |
| `enable_search`      | `boolean`                | Configuration passed to the bottom sheet component (FilterPriceField). | No       | `false`        |
| `findReplace`        | `any`                    | Configuration passed to the bottom sheet component (FilterPriceField). | No       | -              |
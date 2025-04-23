## AdvertiseCalculatorCost

The `AdvertiseCalculatorCost` element is a specialized text input field designed for calculating advertising costs based on a selected placement and a numeric input value (e.g., number of impressions, clicks). It displays the calculated total cost dynamically based on the input and the price associated with the selected placement option.

For a visual reference, see [AdvertiseCalculatorCost Props Gallery](./form-elements/AdvertiseCalculatorCost.md)

### Props

| Name                  | Type                                                     | Description                                                                                                                               | Required | Default      |
| :-------------------- | :------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------- | :------- | :----------- |
| `label`               | `string`                                                 |                                                                                                                                   | No       |              |
| `description`         | `string`                                                 |                                                                                                                                   | No       |              |
| `placeholder`         | `string`                                                 |                                                                                                                                   | No       |              |
| `required`            | `boolean`                                                |                                                                                                                                   | No       | `false`      |
| `disabled`            | `boolean`                                                |                                                                                                                                   | No       | `false`      |
| `editable`            | `boolean`                                                | Whether the input is editable.                                                                                                            | No       | `true`       |
| `fullWidth`           | `boolean`                                                |                                                                                                                                   | No       | `false`      |
| `margin`              | `'none'`, `'dense'`, `'normal'`, `'small'`               |                                                                                                                                   | No       | `'normal'`   |
| `paddingBottom`       | `'none'`, `'dense'`, `'normal'`, `'small'`               |                                                                                                                                   | No       | `'normal'`   |
| `variant`             | `'standard'`, `'outlined'`, `'filled'`, `'standard-outlined'` | Specifies the visual style of the component.                                                                                              | No       | `'standard'` |
| `minHeight`           | `number`                                                 |                                                                                                                                   | No       |              |
| `maxLength`           | `number`                                                 |                                                                                                                                   | No       |              |
| `multiline`           | `boolean`                                                | Allows multiple lines of text input.                                                                                                      | No       | `false`      |
| `autoCorrect`         | `boolean`                                                | Enables auto-correction.                                                                                                                  | No       | `true`       |
| `autoCapitalize`      | `'none'`, `'sentences'`, `'words'`, `'characters'`       | Controls automatic capitalization.                                                                                                        | No       | `'sentences'`|
| `autoFocus`           | `boolean`                                                |                                                                                                                                   | No       | `false`      |
| `clearButtonMode`     | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | When to show the clear button (iOS only).                                                                                                 | No       | `'never'`    |
| `totalNameLabel`      | `string`                                                 | The translation key for the "Total Cost" label prefix.                                                                                    | No       | `total_cost` |
| `initialUnit`         | `number`                                                 | The base unit for the cost calculation (e.g., cost per 1000 impressions means `initialUnit` is 1000).                                      | Yes      |              |
| `pricePattern`        | `object`                                                 | An object defining the currency formatting (e.g., `{ thousand_separator: ',', decimal_separator: '.', precision: 2, symbol: '$', ... }`). | Yes      |              |
| `relatedInitialPrice` | `string`                                                 | The name of the form field holding the selected placement/option key.                                                                     | Yes      |              |
| `placementOptions`    | `object`                                                 | An object mapping placement keys to their details, including the price per unit (e.g., `{ placement1: { price: 10 }, ... }`).             | Yes      |              |
| `findReplace`         | `any`                                                    | Configuration for find and replace functionality (specific structure TBD).                                                                | No       |              |
| `contextualDescription`| `any`                                                    | Additional contextual description (specific structure TBD).                                                                               | No       |              |
| `...restProps`        | `TextInputProps`                                         | Accepts any other valid React Native `TextInput` props.                                                                                   | No       |              |

## Alert

Displays a styled alert box containing an HTML message. The appearance (color, icon) depends on the `severity` and `variant`.

### Props

| Name      | Type                                         | Description                                                                 | Required | Default     |
| :-------- | :------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :---------- |
| `message` | `string`                                     | The HTML content to display in the alert.                                   | Yes      |             |
| `variant` | `'standard'`                                 | Controls the overall style variant of the alert.                            | No       | `'standard'`|
| `severity`| `'success' \| 'info' \| 'warning' \| 'error'` | Determines the alert type (info, success, warning, error), affecting color and icon. | No       | `'info'`    |

## Attachment

The Attachment element allows users to upload one or more files (photos, videos, or other types) within a form. It provides options for selecting files from the device library or capturing directly from the camera.

### Props

| Name                  | Type                                       | Description                                                                 | Required | Default            |
| :-------------------- | :----------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------------- |
| `label`               | `string`                                   |                                                                             | No       |                    |
| `description`         | `string`                                   |                                                                             | No       |                    |
| `required`            | `boolean`                                  |                                                                             | No       | `false`            |
| `disabled`            | `boolean`                                  |                                                                             | No       | `false`            |
| `fullWidth`           | `boolean`                                  |                                                                             | No       | `false`            |
| `margin`              | `'none' \| 'dense' \| 'normal'`            |                                                                             | No       | `'normal'`         |
| `variant`             | `'standard' \| 'outlined' \| 'filled' \| 'standard-inlined'` | The display style variant.                                                  | No       | `'standard-inlined'` |
| `multiple`            | `boolean`                                  | Allows selecting multiple files if `true`.                                  | No       | `false`            |
| `file_type`           | `'photo' \| 'video' \| 'file'`             | Specifies the type of file allowed ('photo', 'video', or generic 'file').   | No       | `'photo'`          |
| `isVideoUploadAllowed`| `boolean`                                  | If `true`, allows video file uploads alongside photos.                      | No       | `false`            |
| `max_upload_filesize` | `object`                                   | An object defining maximum upload size per file type (e.g., `{ photo: 5242880, video: 10485760 }`). | No       | `{}`               |
| `max_files`           | `number`                                   | Maximum number of files that can be attached.                               | No       | `10`               |
| `min_files`           | `number`                                   | Minimum number of files required.                                           | No       | `1`                |
| `cropping`            | `boolean`                                  | Enables image cropping after selection (currently applies to photos only).  | No       | `false`            |
| `include_exif`        | `boolean`                                  | If `true`, includes EXIF data with uploaded images.                         | No       | `false`            |
| `item_type`           | `string`                                   | The backend item type associated with the attachment (e.g., 'photo', 'video'). | No       | `'unknown'`        |
| `maxFilesDescription` | `string`                                   | Custom description text related to the maximum file limit.                  | No       |                    |
| `current_files`       | `FileItemShape[]`                          | An array of pre-existing files (used when editing).                         | No       | `[]`               |
| `paddingBottom`       | `string`                                   |                                                                             | No       |                    |

## AttachPoll

Allows users to attach, view, edit, or remove a poll within a form. It presents a button to initiate the poll creation/editing process via a separate form screen (`form.edit` route) using the provided `config.formUrl`, and displays a preview of the attached poll using the `ui.AttachPollPreview` component.

### Props

| Name          | Type                               | Description                                                                 | Required | Default       |
| :------------ | :--------------------------------- | :-------------------------------------------------------------------------- | :------- | :------------ |
| `formUrl`     | `string`                           | API endpoint URL to fetch/submit the poll form data.                        | Yes      | `undefined`   |
| `label`       | `string`                           |                                                                             | No       | `undefined`   |
| `description` | `string`                           |                                                                             | No       | `undefined`   |
| `placeholder` | `string`                           |                                                                             | No       | `'attach_poll'` |
| `disabled`    | `boolean`                          |                                                                             | No       | `false`       |
| `fullWidth`   | `boolean`                          |                                                                             | No       | `true`        |
| `margin`      | `'none' \| 'normal' \| 'dense'`    |                                                                             | No       | `'normal'`    |
| `size`        | `'small' \| 'medium'`              | Defines the size of the control elements (like the button).                 | No       | `'medium'`    |

## AuthenticatorQrCode

Displays a QR code, typically used for setting up two-factor authentication (2FA). It shows the QR code image, a button to attempt opening a 2FA app, a manual setup key (description), and a button to copy the key.

### Props

| Name          | Type                                    | Description                                                                 | Required | Default      |
| :------------ | :-------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------- |
| `label`       | `string`                                |                                                                             | No       | `undefined`  |
| `content`     | `string`                                | The content/data to encode in the QR code and the URL to open 2FA apps.     | No       | `undefined`  |
| `description` | `string`                                |                                                                             | No       | `undefined`  |
| `placeholder` | `string`                                |                                                                             | No       | `undefined`  |
| `variant`     | `'standard'`, `'outlined'`, `'filled'`  | The visual style variant of the form control.                               | No       | `'standard'` |
| `margin`      | `'none'`, `'dense'`, `'normal'`         |                                                                             | Yes      | -            |
| `paddingBottom`| `'none'`, `'dense'`, `'normal'`         |                                                                             | Yes      | -            |
| `fullWidth`   | `boolean`                               |                                                                             | No       | `false`      |

## Autocomplete

A form element allowing users to select one or multiple options from a list, often populated dynamically via an API search. It presents the selected value(s) and opens a dedicated interface for searching and selecting options.

### Props

| Name              | Type                                  | Description                                                                 | Required | Default      |
| :---------------- | :------------------------------------ | :-------------------------------------------------------------------------- | :------- | :----------- |
| `variant`         | `string` ('outlined', 'standard', ...) | Visual style of the form field.                                             | No       | `'outlined'` |
| `label`           | `string`                              |                                                                             | Yes      |              |
| `size`            | `string` ('medium', 'small')          | The size of the form field.                                                 | No       | `'medium'`   |
| `margin`          | `string` ('normal', 'dense', 'none')  |                                                                             | No       | `'normal'`   |
| `placeholder`     | `string`                              |                                                                             | No       | `''`         |
| `required`        | `boolean`                             |                                                                             | No       | `false`      |
| `fullWidth`       | `boolean`                             |                                                                             | No       | `true`       |
| `search_endpoint` | `string`                              | API endpoint URL used to fetch options dynamically based on user input.     | Yes      |              |
| `search_params`   | `object`                              | Additional parameters to include in the API request to `search_endpoint`.   | No       | `{}`         |
| `multiple`        | `boolean`                             | If `true`, allows the user to select multiple options.                      | No       | `false`      |
| `enable_search`   | `boolean`                             | If `true`, enables a search input within the selection interface.           | No       | `true`       |
| `disable_uncheck` | `boolean`                             | If `true`, prevents unselecting the currently selected option (single mode). | No       | `false`      |
| `choice_type`     | `string`                              | Influences how choices are presented or handled internally.                 | No       | `undefined`  |
| `icon`            | `string` (IconName)                   | Name of the icon to display, primarily used in the 'livestream' variant.    | No       | `undefined`  |
| `paddingBottom`   | `string` ('normal', 'dense', 'none')  |                                                                             | No       | `undefined`  |

## AvatarUpload

A form element that allows users to select and upload an avatar image, displaying a preview. It integrates with the device's image picker and handles basic validation display.

### Props

| Name             | Type                    | Description                                                      | Required | Default     |
| :--------------- | :---------------------- | :--------------------------------------------------------------- | :------- | :---------- |
| `size`           | `string`                | Size of the avatar preview (e.g., 'small', 'medium', 'xxlarge'). | No       | `'xxlarge'` |
| `circle`         | `boolean`               | Renders the avatar preview as a circle.                          | No       | `true`      |
| `margin`         | `keyof typeof SizeEnum` |                                                                  | No       | `'none'`    |
| `paddingBottom`  | `keyof typeof SizeEnum` |                                                                  | No       | `undefined` |
| `fullWidth`      | `boolean`               |                                                                  | No       | `false`     |
| `required`       | `boolean`               |                                                                  | No       | `false`     |
| `variant`        | `Variant`               | Visual style variant of the form control.                        | No       | `undefined` |
| `spaceWidth`     | `number`              | Width of the space around the avatar image.                      | No       | `undefined` |
| `spaceColor`     | `string`              | Color of the space around the avatar image.                      | No       | `undefined` |
| `borderColor`    | `string`              | Color of the border around the avatar image.                     | No       | `undefined` |

## Birthday

The `Birthday` element provides a user-friendly interface for selecting a date, specifically intended for capturing a user's date of birth. It utilizes a native date picker interface.

### Props

| Name             | Type                             | Description                                                                 | Required | Default        |
| :--------------- | :------------------------------- | :-------------------------------------------------------------------------- | :------- | :------------- |
| `label`          | `string`                         |                                                                             | No       | -              |
| `placeholder`    | `string`                         |                                                                             | No       | -              |
| `required`       | `boolean`                        |                                                                             | No       | `false`        |
| `disabled`       | `boolean`                        |                                                                             | No       | `false`        |
| `description`    | `string`                         |                                                                             | No       | -              |
| `fullWidth`      | `boolean`                        |                                                                             | No       | `false`        |
| `margin`         | `'none' \| 'normal' \| 'dense'` |                                                                             | No       | `'normal'`     |
| `variant`        | `'standard' \| 'outlined' \| 'filled'` | Defines the visual style of the input field.                              | No       | `'standard'`   |
| `minDate`        | `string`                         | The earliest selectable date in ISO 8601 format (e.g., "1900-01-01").       | No       | -              |
| `maxDate`        | `string`                         | The latest selectable date in ISO 8601 format (e.g., "2024-12-31").         | No       | Current Date   |
| `initialValue`   | `string`                         | Sets the initial date displayed in ISO 8601 format.                         | No       | -              |
| `displayFormat`  | `string`                         | The format (using moment.js tokens) to display the selected date.         | No       | Locale default |

**Note:** This component internally uses a date picker (`DatePickerField`). While the underlying component supports time selection (`datePickerMode`), the `Birthday` element is intended for date selection only. The `maxDate` prop should typically be configured to prevent selecting future dates for birthdays.

## Button

A form element that renders a toggleable button. Its text changes based on its internal state (0 or 1), typically used to trigger an action or represent a binary choice within a form.

### Props

| Name          | Type                             | Description                                                                 | Required | Default    |
|---------------|----------------------------------|-----------------------------------------------------------------------------|----------|------------|
| label         | `string`                         | The text displayed on the button when its value is 1 (active state).        | Yes      |            |
| cancelLabel   | `string`                         | The text displayed on the button when its value is 0 (inactive state).      | Yes      |            |
| disabled      | `boolean`                        |                                                                             | No       | `false`    |
| fullWidth     | `boolean`                        |                                                                             | No       | `true`     |
| margin        | `'normal' \| 'dense' \| 'none'` |                                                                             | No       | `'normal'` |
| size          | `'small' \| 'medium'`          | The size applied to the surrounding form control.                           | No       | `undefined`|

## Checkbox

A form element that renders a checkbox input field. It allows users to toggle between a checked and unchecked state, typically representing a boolean value or a specific selection.

### Props

| Name                | Type                                                   | Description                                                     | Required | Default            |
| :------------------ | :----------------------------------------------------- | :-------------------------------------------------------------- | :------- | :----------------- |
| `label`             | `string`                                               |                                                                 | Yes      |                    |
| `fullWidth`         | `boolean`                                              |                                                                 | No       | `false`            |
| `margin`            | `'none' \| 'dense' \| 'normal'`                        |                                                                 | No       | `'normal'`         |
| `required`          | `boolean`                                              |                                                                 | No       | `false`            |
| `variant`           | `'standard' \| 'outlined' \| 'filled' \| 'standard-inlined'` | Visual style variant of the control.                            | No       | `'standard-inlined'` |
| `paddingBottom`     | `'none' \| 'dense' \| 'normal'`                        |                                                                 | No       | `'normal'`         |
| `checkedValue`      | `any`                                                  | The value submitted when the checkbox is checked.               | No       | `1`                |
| `uncheckedValue`    | `any`                                                  | The value submitted when the checkbox is unchecked.             | No       | `0`                |
| `description`       | `string`                                               |                                                                 | No       | `''`               |
| `disabled`          | `boolean`                                              |                                                                 | No       | `false`            |
| `isReverse`         | `boolean`                                              | If true, reverses the order of the label and checkbox control.  | No       | `false`            |

## CheckboxGroup

This element renders a group of checkboxes, allowing users to select multiple options from a predefined list. It integrates with Formik for state management and validation.

### Props

| Name             | Type                                     | Description                                                                 | Required | Default      |
| :--------------- | :--------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------- |
| `label`          | `string`                                 |                                                                             | Yes      |              |
| `options`        | `Array<{ label: string, value: any }>` | An array of objects defining the available checkbox options.                | Yes      | `[]`         |
| `variant`        | `'standard' \| 'outlined' \| 'filled'` | The visual style variant of the form control wrapper.                       | No       | `'standard'` |
| `margin`         | `'normal' \| 'dense' \| 'none'`        |                                                                             | No       | `undefined`  |
| `fullWidth`      | `boolean`                                |                                                                             | No       | `false`      |
| `disabled`       | `boolean`                                |                                                                             | No       | `false`      |
| `required`       | `boolean`                                |                                                                             | No       | `false`      |
| `hasFormOrder`   | `boolean`                                | If `true`, prepends the `order` number to the label.                        | No       | `false`      |
| `order`          | `number`                                 | The numerical order to display before the label (if `hasFormOrder` is true). | No       | `undefined`  |
| `paddingBottom`  | `string`                                 |                                                                             | No       | `undefined`  |

## Chip

Renders a group of selectable chip buttons. Selecting a chip updates the form's `title` and `description` fields with the corresponding values from the selected option.

### Props

| Name            | Type                  | Description                                                                                      | Required | Default     |
| :-------------- | :-------------------- | :----------------------------------------------------------------------------------------------- | :------- | :---------- |
| `label`         | `string`              |                                                                                                  | Yes      |             |
| `options`       | `RadioFieldOptions[]` | An array of option objects to render as chips. Each should have `title` and `description`.       | Yes      | `[]`        |
| `required`      | `boolean`             |                                                                                                  | No       | `false`     |

## ClearSearch

This element displays a title and a conditional "Reset" button within a form. The button allows users to reset specific form fields (defined by `targetFields`) back to their initial values. The button only appears when the current values of the target fields differ from their initial state.

### Props

| Name           | Type     | Description                                                                              | Required | Default                             |
| -------------- | -------- | ---------------------------------------------------------------------------------------- | -------- | ----------------------------------- |
| `targetFields` | `string[]` | An array of form field names that this element will reset when the button is pressed.    | No       | `['sort', 'when', 'category_id']` |
| `label`        | `string` | The localization key for the text displayed on the reset button.                         | No       | `'reset'`                           |
| `title`        | `string` | The localization key for the title displayed above the reset button.                     | No       | `'filter'`                          |
| `align`        | `string` | Alignment configuration (appears unused in the current implementation).                  | No       | `'right'`                           |

## Clickable

A form element that displays a label and a right arrow, acting as a button. When clicked, it dispatches a specified Redux action with given parameters. It's typically used to navigate to another screen or trigger a modal for further input or selection.

### Props

| Name          | Type                                       | Description                                                    | Required | Default     |
| ------------- | ------------------------------------------ | -------------------------------------------------------------- | -------- | ----------- |
| `name`        | `string`                                   | The name of the field in the form state.                       | Yes      |             |
| `label`       | `string`                                   |                                                                | Yes      |             |
| `action`      | `string`                                   | The Redux action type to dispatch on click.                    | Yes      |             |
| `params`      | `object`                                   | The payload to send with the dispatched action.                | Yes      |             |
| `fullWidth`   | `boolean`                                  |                                                                | No       | `false`     |
| `margin`      | `'normal' \| 'dense' \| 'none'`            |                                                                | No       | `'normal'`  |
| `variant`     | `'standard' \| 'outlined' \| 'filled'`     | The visual style variant.                                      | No       | `'standard'`|
| `paddingBottom`| `boolean`                                  |                                                                | No       | `false`     |
| `severity`    | `'error' \| 'warning' \| 'info' \| 'success'` | Sets the text color based on severity (e.g., for validation). | No       |             |

## ComposerInput

A specialized text input field designed for composer interfaces within MetaFox forms. It renders an input area that, when pressed, opens a bottom sheet for text entry. It supports dynamic height adjustment based on content.

### Props

| Name                  | Type                                                      | Description                                                                 | Required | Default     |
| :-------------------- | :-------------------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :---------- |
| `label`               | `string`                                                  |                                                                             | No       | `undefined` |
| `placeholder`         | `string`                                                  |                                                                             | No       | `undefined` |
| `description`         | `string`                                                  |                                                                             | No       | `undefined` |
| `variant`             | `'standard' \| 'outlined' \| 'filled'`                    | The visual style variant of the input.                                      | No       | `'standard'`|
| `margin`              | `'none' \| 'dense' \| 'normal'`                           |                                                                             | No       | `'normal'`  |
| `fullWidth`           | `boolean`                                                 |                                                                             | No       | `false`     |
| `required`            | `boolean`                                                 |                                                                             | No       | `false`     |
| `disabled`            | `boolean`                                                 |                                                                             | No       | `false`     |
| `maxLength`           | `number`                                                  |                                                                             | No       | `undefined` |
| `autoFocus`           | `boolean`                                                 |                                                                             | No       | `false`     |
| `autoCorrect`         | `boolean`                                                 | Enables or disables auto-correction.                                        | No       | `undefined` |
| `autoCapitalize`      | `'none' \| 'sentences' \| 'words' \| 'characters'`        | Controls automatic capitalization behavior.                                 | No       | `undefined` |
| `clearButtonMode`     | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | (iOS only) When to display the standard clear button.                       | No       | `undefined` |
| `findReplace`         | `{ find: string, replace: string }`                       | Defines patterns for automatic find-and-replace operations on the value.    | No       | `undefined` |
| `contextualDescription`| `string`                                                  | Additional description text, often appended with the current field value. | No       | `undefined` |

## Container

The `Container` element acts as a layout wrapper for grouping other form elements. It provides options for labeling, description, different layout variants (vertical, horizontal, livestream), and optional collapsibility.

### Props

| Name          | Type                                        | Description                                                                 | Required | Default      |
|---------------|---------------------------------------------|-----------------------------------------------------------------------------|----------|--------------|
| `label`       | `string`                                    |                                                                             | No       | `undefined`  |
| `description` | `string`                                    |                                                                             | No       | `undefined`  |
| `elements`    | `Record<string, FormFieldConfig>`           | An object defining the form elements nested within this container.          | Yes      | `{}`         |
| `variant`     | `'vertical' \| 'horizontal' \| 'livestream'` | Controls the layout arrangement of elements.                                | No       | `'vertical'` |
| `collapsible` | `boolean`                                   | If true, allows the user to collapse and expand the container.              | No       | `false`      |
| `collapsed`   | `boolean`                                   | Sets the initial collapsed state when `collapsible` is true.                | No       | `false`      |
| `required`    | `boolean`                                   |                                                                             | No       | `false`      |
| `wrapAs`      | `React.ElementType`                         | A custom React component to use as the wrapper instead of the default `View`. | No       | `undefined`  |
| `wrapperProps`| `object`                                    | Additional props to pass directly to the root wrapper component.            | No       | `{}`         |
| `className`   | `string`                                    | CSS class name for the wrapper (primarily for web).                         | No       | `undefined`  |
| `sx`          | `object`                                    | Style object for applying custom styles to the root wrapper component.      | No       | `{}`         |
| `full_space`  | `boolean`                                   | When true, the container attempts to occupy full available space.           | No       | `false`      |

## CountryCityCode

This form element provides an input field that allows users to select a country and associated city/state code. It typically opens a dedicated selection interface (modal or screen) for browsing and choosing the appropriate code.

### Props

| Name              | Type                                             | Description                                                                                              | Required | Default        |
| :---------------- | :----------------------------------------------- | :------------------------------------------------------------------------------------------------------- | :------- | :------------- |
| `label`           | `string`                                         |                                                                                                          | Yes      | `''`           |
| `fullWidth`       | `boolean`                                        |                                                                                                          | No       | `false`        |
| `margin`          | `'none' \| 'dense' \| 'normal'`                  |                                                                                                          | No       | `'normal'`     |
| `required`        | `boolean`                                        |                                                                                                          | No       | `false`        |
| `variant`         | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined'` | The visual style variant of the form field.                                                              | No       | `'standard'`   |
| `paddingBottom`   | `'none' \| 'dense' \| 'normal'`                  |                                                                                                          | No       | `'normal'`     |
| `enable_search`   | `boolean`                                        | Enables search functionality within the selection view.                                                  | No       | `false`        |
| `disable_uncheck` | `boolean`                                        | Prevents the user from unselecting the current value if set to true.                                     | No       | `false`        |
| `search_endpoint` | `string`                                         | API endpoint used for searching options if `enable_search` is true.                                      | No       | `undefined`    |
| `search_params`   | `object`                                         | Additional parameters for the search request. Values can be dynamically sourced from the form context. | No       | `undefined`    |
| `backgroundColor` | `string`                                         | Background color for the animated placeholder (used in 'standard-outlined' variant).                     | No       | `undefined`    |

## countryStatePicker

This element provides a specialized picker for selecting a country and its corresponding state or province. It typically fetches state/province options dynamically based on the selected country.

### Props

| Name              | Type                                  | Description                                                                 | Required | Default     |
| :---------------- | :------------------------------------ | :-------------------------------------------------------------------------- | :------- | :---------- |
| `label`           | `string`                              |                                                                             | Yes      | `''`        |
| `fullWidth`       | `boolean`                             |                                                                             | No       | `false`     |
| `margin`          | `'normal' \| 'dense' \| 'none'`       |                                                                             | No       | `'normal'`  |
| `required`        | `boolean`                             |                                                                             | No       | `false`     |
| `variant`         | `'standard' \| 'outlined' \| 'filled'`| The display style of the form element.                                      | No       | `'standard'`|
| `paddingBottom`   | `'normal' \| 'dense' \| 'none'`       |                                                                             | No       | `'normal'`  |
| `placeholder`     | `string`                              |                                                                             | No       | `undefined` |
| `search_endpoint` | `string`                              | API endpoint to fetch options dynamically (e.g., states based on country). | No       | `undefined` |
| `search_params`   | `object`                              | Additional parameters for the search API endpoint.                          | No       | `undefined` |
| `enable_search`   | `boolean`                             | Enables searching within the options list (if applicable).                  | No       | `false`     |
| `disable_uncheck` | `boolean`                             | Prevents unselecting the current value if the field is required.            | No       | `false`     |
| `backgroundColor` | `string`                              | Background color for the element (used in specific variants).               | No       | `undefined` |
| `disabled`        | `boolean`                             |                                                                             | No       | `false`     |

## CustomButton

A form element that renders a button which dispatches a custom Redux action when pressed.

### Props

| Name          | Type                                               | Description                                                                                                | Required | Default           |
| ------------- | -------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | -------- | ----------------- |
| `name`        | `string`                                           | The unique identifier for the form field.                                                                  | Yes      | `CustomButtonField` |
| `label`       | `string`                                           |                                                                                                            | Yes      |                   |
| `variant`     | `string`                                           | Specifies the button style. Currently supports 'link'.                                                     | Yes      | `'link'`          |
| `customAction`| `{ type: string; payload?: any; meta?: any }`      | An object defining the Redux action dispatched on press. `type` is required, `payload` and `meta` are optional. | Yes      |                   |
| `disabled`    | `boolean`                                          |                                                                                                            | No       | `false`           |

## Date

A form element that allows users to select a date, time, or both using a native modal picker.

### Props

| Name           | Type                             | Description                                                                 | Required | Default             |
| -------------- | -------------------------------- | --------------------------------------------------------------------------- | -------- | ------------------- |
| label          | string                           |                                                                             | Yes      | `'close_time'`      |
| placeholder    | string                           |                                                                             | No       |                     |
| description    | string                           |                                                                             | No       |                     |
| required       | boolean                          |                                                                             | No       | `false`             |
| disabled       | boolean                          |                                                                             | No       | `false`             |
| fullWidth      | boolean                          |                                                                             | No       | `false`             |
| margin         | `'none' \| 'normal' \| 'dense'`  |                                                                             | No       | `'normal'`          |
| variant        | `'standard' \| 'outlined' \| 'filled'` | The visual style variant of the input field.                              | No       | `'standard'`        |
| datePickerMode | `'date' \| 'time' \| 'datetime'` | Determines if the picker selects date, time, or both.                     | No       | `'datetime'`        |
| displayFormat  | string                           | The `moment.js` format string used to display the selected date/time.     | No       | `'DD/MM/YYYY - HH:mm'` |
| minDate        | string                           | The minimum selectable date (ISO string or format specified by `momentResultFormat`). | No       |                     |
| maxDate        | string                           | The maximum selectable date (ISO string or format specified by `momentResultFormat`). | No       |                     |
| time_zone_gmt  | string                           | Timezone identifier (e.g., 'Asia/Ho_Chi_Minh') for display formatting.    | No       | User's timezone     |
| timeFormat     | `12 \| 24`                       | Specifies 12 or 24-hour time format for the picker.                       | No       | `12`                |
| startOfDay     | boolean                          | If `true`, sets the selected time to the start of the day (00:00:00).     | No       | `false`             |
| endOfDay       | boolean                          | If `true`, sets the selected time to the end of the day (23:59:59).       | No       | `false`             |

## DateBasic

A form element component that provides a user interface for selecting a date, time, or datetime using a native modal picker. It integrates with Formik for form state management.

### Props

| Name               | Type                           | Description                                                                 | Required | Default        |
| :----------------- | :----------------------------- | :-------------------------------------------------------------------------- | :------- | :------------- |
| `fullWidth`        | `boolean`                      |                                                                             | No       | `false`        |
| `margin`           | `string`                       |                                                                             | No       | `normal`       |
| `paddingBottom`    | `string`                       |                                                                             | No       | `normal`       |
| `variant`          | `string`                       | The visual style variant (`standard`, `outlined`, `filled`).                | No       | `standard`     |
| `time_zone_gmt`    | `string`                       | Specifies the GMT timezone offset (e.g., "+07:00").                         | No       | `''`           |
| `label`            | `string`                       |                                                                             | No       | `'close_time'` |
| `placeholder`      | `string`                       |                                                                             | No       | `''`           |
| `required`         | `boolean`                      |                                                                             | No       | `false`        |
| `editable`         | `boolean`                      | If `false`, the text input part is not directly editable by the user.       | No       | `true`         |
| `minDate`          | `string`                       | The earliest selectable date (format defined by `momentResultFormat`).      | No       | `undefined`    |
| `maxDate`          | `string`                       | The latest selectable date (format defined by `momentResultFormat`).        | No       | `undefined`    |
| `momentResultFormat` | `string`                       | The Moment.js format string used for parsing `minDate` and `maxDate`.       | No       | `''`           |
| `datePickerMode`   | `'date' \| 'time' \| 'datetime'` | Determines the type of picker shown (`date`, `time`, or `datetime`).        | No       | `'date'`       |
| `resultFormat`     | `string`                       | The desired format for the final value submitted by the form.               | No       | `''`           |
| `valueFormat`      | `string`                       | The Moment.js format string for displaying and storing the selected value.  | No       | `'DD/MM/YYYY'` |
| `initialValue`     | `string`                       | An initial value to populate the date field with.                           | No       | `undefined`    |
| `timeFormat`       | `number`                       | Specifies the time format (e.g., `12` or `24` for 12/24 hour format).       | No       | `12`           |
| `disabled`         | `boolean`                      |                                                                             | No       | `false`        |

## Datetime

The same with element Date.

### Props

Props are configured via the `config` object passed to the component.

| Name             | Type                             | Description                                                                 | Required | Default             |
| :--------------- | :------------------------------- | :-------------------------------------------------------------------------- | :------- | :------------------ |
| `label`          | `string`                         |                                                                             | No       | `'close_time'`      |
| `description`    | `string`                         |                                                                             | No       |                     |
| `placeholder`    | `string`                         |                                                                             | No       |                     |
| `datePickerMode` | `'date' \| 'time' \| 'datetime'` | Determines if the picker selects date, time, or both.                       | No       | `'datetime'`        |
| `displayFormat`  | `string`                         | The Moment.js format string used to display the selected value.             | No       | `'DD/MM/YYYY - HH:mm'` |
| `initialValue`   | `string`                         | An initial value for the date/time field (ISO 8601 format recommended).     | No       |                     |
| `minDate`        | `string`                         | The minimum selectable date (format depends on `momentResultFormat`).       | No       |                     |
| `maxDate`        | `string`                         | The maximum selectable date (format depends on `momentResultFormat`).       | No       |                     |
| `momentResultFormat` | `string`                     | The Moment.js format string used for parsing `minDate` and `maxDate`.       | No       |                     |
| `time_zone_gmt`  | `string`                         | The timezone identifier (e.g., 'America/New_York') used for formatting.     | No       |                     |
| `timeFormat`     | `12 \| 24`                       | Specifies 12-hour or 24-hour time format for the picker.                    | No       | (Locale default)    |
| `startOfDay`     | `boolean`                        | If true, sets the selected date's time to the start of the day (00:00:00).  | No       | `false`             |
| `endOfDay`       | `boolean`                        | If true, sets the selected date's time to the end of the day (23:59:59).    | No       | `false`             |
| `required`       | `boolean`                        |                                                                             | No       | `false`             |
| `disabled`       | `boolean`                        |                                                                             | No       | `false`             |
| `fullWidth`      | `boolean`                        |                                                                             | No       | `false`             |
| `margin`         | `'none' \| 'dense' \| 'normal'`  |                                                                             | No       | `'normal'`          |
| `paddingBottom`  | `'none' \| 'dense' \| 'normal'`  |                                                                             | No       | `'normal'`          |
| `variant`        | `'standard' \| 'outlined' \| 'filled'` | The visual style of the input field.                                        | No       | `'standard'`        |

*Note: The component also accepts standard `FormFieldProps` like `name` (required) and `formik` (required), as well as top-level `disabled` and `required` props that can override the corresponding settings within `config`.*

## Description

Displays a simple text label within a form, often used for informational purposes or section descriptions.

### Props

| Name          | Type                     | Description                                      | Required | Default      |
| ------------- | ------------------------ | ------------------------------------------------ | -------- | ------------ |
| `label`       | `string`                 |                                                  | Yes      |              |
| `variant`     | `keyof typeof Variant`   | The visual style variant (e.g., 'standard').     | No       | `'standard'` |
| `fullWidth`   | `boolean`                |                                                  | No       | `false`      |
| `margin`      | `keyof typeof SizeEnum`  |                                                  | No       | `undefined`  |
| `paddingBottom`| `keyof typeof SizeEnum`  |                                                  | No       | `undefined`  |

## DynamicTypo

Displays a dynamic description text based on the value of a related form field. It looks up the description from the `config.data` array using the value of the field specified in `config.relatedField`.

### Props

| Name             | Type                                          | Description                                                              | Required | Default |
| :--------------- | :-------------------------------------------- | :----------------------------------------------------------------------- | :------- | :------ |
| `data`           | `Array<{ value: any; description: string; }>` | Array of value-description pairs.                                        | Yes      | `[]`    |
| `relatedField`   | `string`                                      | Name of the form field whose value determines the displayed description. | Yes      |         |
| `fullWidth`      | `boolean`                                     |                                                                          | No       |         |
| `margin`         | `'dense' \| 'normal' \| 'none'`               |                                                                          | No       |         |
| `required`       | `boolean`                                     |                                                                          | No       |         |
| `variant`        | `'outlined' \| 'filled' \| 'standard'`        | The visual style variant of the element.                                 | No       |         |
| `paddingBottom`  | `'dense' \| 'normal' \| 'none'`               |                                                                          | No       |         |

## Editor

The same with element Text.

### Props

| Name                  | Type                                                              | Description                                                                 | Required | Default         |
| :-------------------- | :---------------------------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :-------------- |
| `label`        | `string`                           |                                                                             | No       |                 |
| `placeholder`  | `string`                           |                                                                             | No       |                 |
| `description`  | `string`                           |                                                                             | No       |                 |
| `variant`      | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined' \| 'livestream'` | The visual style variant of the input field.                              | No       | `'standard'`    |
| `fullWidth`    | `boolean`                                                         |                                                                             | No       | `false`         |
| `margin`       | `'none' \| 'normal' \| 'dense'`                                     |                                                                             | No       | `'normal'`      |
| `multiline`    | `boolean`                                                         | If `true`, allows multiple lines of text input (textarea).                  | No       | `false`         |
| `minHeight`    | `number`                                                          |                                                                             | No       |                 |
| `maxLength`    | `number`                                                          |                                                                             | No       |                 |
| `autoFocus`    | `boolean`                                                         |                                                                             | No       | `false`         |
| `autoCorrect`  | `boolean`                                                         | Enables or disables auto-correction for the input.                          | No       | `true`          |
| `autoCapitalize`| `'none' \| 'sentences' \| 'words' \| 'characters'`                | Controls automatic capitalization behavior.                                 | No       | `'sentences'`   |
| `editable`     | `boolean`                                                         | If `false`, the text input is not editable.                                 | No       | `true`          |
| `required`     | `boolean`                                                         |                                                                             | No       | `false`         |
| `clearButtonMode`| `'never' \| 'while-editing' \| 'unless-editing' \| 'always'`      | (iOS only) When to display the clear text button.                           | No       | `'never'`       |
| `validateAction`| `string`                                                          | Name of a registered action for backend validation triggered on blur.       | No       |                 |
| `findReplace`  | `{ find: string, replace: string }`                               | Configuration to automatically generate a slug-like value based on input. | No       |                 |
| `contextualDescription` | `string`                                               | Additional descriptive text displayed near the input.                       | No       |                 |
| `hasQRScanner` | `boolean`                                                         | If `true`, displays a QR code scanner icon button.                          | No       | `false`         |
| `qrScannerParamName` | `string`                                                  | Query parameter name to extract from the scanned QR code URL.               | No       | `'invite_code'` |
| `hasCopy`      | `boolean`                                                         | If `true`, displays a copy-to-clipboard icon button.                        | No       | `false`         |
| `backgroundColor`| `string`                                                          | Sets the background color for the input wrapper.                            | No       |                 |

## Email

*Note: This element inherits most props from the base `Text` element.*

### Props

| Name                  | Type                                                         | Description                                                                                   | Required | Default         |
| :-------------------- | :----------------------------------------------------------- | :-------------------------------------------------------------------------------------------- | :------- | :-------------- |
| `label`               | `string`                                                     |                                                                                               | No       | `undefined`     |
| `placeholder`         | `string`                                                     |                                                                                               | No       | `undefined`     |
| `description`         | `string`                                                     |                                                                                               | No       | `undefined`     |
| `required`            | `boolean`                                                    |                                                                                               | No       | `false`         |
| `disabled`            | `boolean`                                                    |                                                                                               | No       | `false`         |
| `variant`             | `'standard'`, `'outlined'`, `'filled'`, `'standard-outlined'` | The visual style of the input field.                                                          | No       | `'standard'`    |
| `margin`              | `'normal'`, `'dense'`, `'none'`                              |                                                                                               | No       | `'normal'`      |
| `fullWidth`           | `boolean`                                                    |                                                                                               | No       | `false`         |
| `maxLength`           | `number`                                                     |                                                                                               | No       | `undefined`     |
| `autoFocus`           | `boolean`                                                    |                                                                                               | No       | `false`         |
| `validateAction`      | `string`                                                     | Name of a registered action for backend validation on blur.                                   | No       | `undefined`     |
| `keyboardType`        | `string`                                                     | Determines which keyboard to open (e.g., 'numeric', 'email-address'). For Email, defaults to 'email-address'. | No       | `'email-address'` |
| `autoCapitalize`      | `'none'`, `'sentences'`, `'words'`, `'characters'`           | How to automatically capitalize text. For Email, defaults to 'none'.                          | No       | `'none'`        |
| `returnKeyType`       | `string`                                                     | Determines how the return key should look.                                                    | No       | `'default'`     |
| `textContentType`     | `string`                                                     | Give the keyboard and the system information about the expected semantic meaning for the content. For Email, defaults to 'emailAddress'. | No       | `'emailAddress'` |
| `clearButtonMode`     | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | When to display the clear text button (iOS only).                                             | No       | `'never'`       |
| `...rest`             | `TextInputProps`                                             | Other standard React Native `TextInput` props are accepted.                                   | No       | `undefined`     |

## File

The `File` form element allows users to select and upload a single file, typically an image or video. It provides options to choose from the device library or capture directly using the camera. It handles file preview, upload progress (implicitly via `SinglePhotoItemView`), deletion, and file size validation.

### Props

| Name                  | Type                                                    | Description                                                                                                | Required | Default            |
| :-------------------- | :------------------------------------------------------ | :--------------------------------------------------------------------------------------------------------- | :------- | :----------------- |
| `label`               | `string`                                                |                                                                                                            | No       | `''`               |
| `description`         | `string`                                                |                                                                                                            | No       | `''`               |
| `required`            | `boolean`                                               |                                                                                                            | No       | `false`            |
| `variant`             | `string`                                                | Visual style variant ('standard', 'outlined', 'filled', 'standard-inlined', 'livestream').                 | No       | `standard-inlined` |
| `fullWidth`           | `boolean`                                               |                                                                                                            | No       | `false`            |
| `margin`              | `string`                                                |                                                                                                            | No       | `normal`           |
| `paddingBottom`       | `string`                                                |                                                                                                            | No       | `normal`           |
| `preview_url`         | `string`                                                | URL of an existing image/file to preview initially.                                                        | No       | `undefined`        |
| `max_upload_filesize` | `object`                                                | Max file sizes in bytes (e.g., `{ photo: 5242880, video: 10485760 }`). `0` means no limit.               | No       | `{ photo: 0, video: 0 }` |
| `file_type`           | `string`                                                | Type of file allowed ('photo', 'video').                                                                   | No       | `photo`            |
| `cropping`            | `boolean`                                               | Enable image cropping after selection (currently might have limitations).                                  | No       | `false`            |
| `include_exif`        | `boolean`                                               | Include EXIF data when selecting photos.                                                                   | No       | `true`             |
| `item_type`           | `string`                                                | The type identifier for the uploaded item on the backend.                                                  | No       | `unknown`          |
| `upload_url`          | `string`                                                | The API endpoint for direct file uploads.                                                                  | No       | `/file`            |
| `extraProps`          | `object`                                                | Additional props for styling or behavior.                                                                  | No       | `{}`               |

## Form

The `Form` element acts as a container for rendering other form elements. It provides layout options and handles scrolling, including keyboard awareness and integration with bottom sheets. When `scrollable` is enabled, it groups elements into `top`, `bottom`, `full_space`, and other categories for layout purposes.

### Props

| Name                  | Type                   | Description                                                                                                | Required | Default |
| :-------------------- | :--------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :------ |
| `elements`            | `Record<string, any>`  | An object containing configurations for nested form elements.                                                | Yes      | `{}`    |
| `isBottomSheet`       | `boolean`              | If true, adapts scrolling behavior for use within a bottom sheet.                                          | No       | `false` |
| `scrollable`          | `boolean`              | If true, wraps the main elements in a scrollable container with keyboard awareness.                          | No       | `false` |
| `disableContainerStyle` | `boolean`              | If true and `scrollable` is true, disables the default `flex: 1` style applied to the scroll container. | No       | `false` |

## FormBottom

Renders a styled container at the bottom of a form, typically used to group related elements like submit buttons or secondary actions. It can display an optional label and description, and renders a collection of nested form elements.

### Props

| Name        | Type                          | Description                                                                                             | Required | Default   |
| :---------- | :---------------------------- | :------------------------------------------------------------------------------------------------------ | :------- | :-------- |
| `label`     | `string`                      |                                                                                                         | No       | `undefined` |
| `description`| `string`                      |                                                                                                         | No       | `undefined` |
| `elements`  | `Record<string, FormFieldConfig>` | An object containing configurations for nested form elements to be rendered within this section. | Yes      | `{}`      |

## FormContent

The `FormContent` element acts as a container to group and render other form elements defined in its configuration. It can optionally display a label and description above the nested elements.

### Props

| Name        | Type                          | Description                                               | Required | Default   |
| :---------- | :---------------------------- | :-------------------------------------------------------- | :------- | :-------- |
| `label`     | `string`                      |                                                           | No       | `undefined` |
| `description`| `string`                      |                                                           | No       | `undefined` |
| `elements`  | `Record<string, ElementConfig>` | An object containing configurations for nested elements. | Yes      | N/A       |

## FormDescription

Displays a description text within a form, supporting simple HTML content.

### Props

| Name          | Type   | Description                                                    | Required | Default     |
| ------------- | ------ | -------------------------------------------------------------- | -------- | ----------- |
| `style`       | object | Custom styling for the description container View.             | No       | `{}`        |
| `description` | string |                                                              | No       | `null`      |
| `numberOfLines`| number | Limits the number of lines displayed for the description text. | No       | `undefined` |

## FormFooter

Renders a footer section for a form, capable of displaying a label, description, and nested form elements.

### Props

| Name        | Type                         | Description                                                              | Required | Default |
| :---------- | :--------------------------- | :----------------------------------------------------------------------- | :------- | :------ |
| `label`     | `string`                     |                                                                          | No       | `null`  |
| `description` | `string`                     |                                                                          | No       | `null`  |
| `elements`  | `Record<string, ElementConfig>` | An object containing configurations for nested form elements.          | Yes      | `{}`    |

## FormHeader

Configures the navigation header for a form screen, setting the title, back button (left), and submit button (right). This element renders `null` and uses `navigation.setOptions` to apply the header configuration.

### Props

| Name                   | Type    | Description                                      | Required | Default         |
| :--------------------- | :------ | :----------------------------------------------- | :------- | :-------------- |
| `title`                | string  | The title displayed in the header.               | No       | `schema.title`  |
| `showLeftHeader`       | boolean | Whether to show the left header button (Back).   | No       | `true`          |
| `showRightHeader`      | boolean | Whether to show the right header button (Submit).| No       | `true`          |

## FormTop

Renders a top section for a form, optionally displaying a label and description, and rendering a collection of nested form elements.

### Props

| Name        | Type                          | Description                                                              | Required | Default     |
| :---------- | :---------------------------- | :----------------------------------------------------------------------- | :------- | :---------- |
| `label`     | `string`                      |                                                                          | No       | `undefined` |
| `description`| `string`                      |                                                                          | No       | `undefined` |
| `elements`  | `Record<string, FormFieldConfig>` | Object containing configurations for nested form elements to be rendered. | Yes      | N/A         |

## FriendPicker

A form element that allows users to select one or multiple friends from a list, typically fetched via an API. It presents a user-friendly interface for friend selection within forms.

### Props

| Name              | Type                                                                              | Description                                       | Required | Default     |
| :---------------- | :-------------------------------------------------------------------------------- | :------------------------------------------------ | :------- | :---------- |
| `fullWidth`       | `boolean`                                                                         |                                                   | No       | `false`     |
| `margin`          | `'none' \| 'dense' \| 'normal'`                                                   |                                                   | No       | `'normal'`  |
| `required`        | `boolean`                                                                         |                                                   | No       | `false`     |
| `variant`         | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined' \| 'livestream'` | Sets the visual style of the element.             | No       | `'standard'`|
| `paddingBottom`   | `'none' \| 'dense' \| 'normal'`                                                   |                                                   | No       | `undefined` |
| `label`           | `string`                                                                          |                                                   | No       | `''`        |
| `suboptions`      | `SubOptionsShape`                                                                 | Additional options or configurations.             | No       | `undefined` |
| `initialValue`    | `OptionsItemShape[]`                                                              | Initial selected friend(s).                       | No       | `undefined` |
| `disable_custom`  | `boolean`                                                                         | Disables custom privacy selection.                | No       | `false`     |
| `value_type`      | `string`                                                                          | Specifies the type of value returned.             | No       | `undefined` |
| `multiple`        | `boolean`                                                                         | Allows selecting multiple friends.                | No       | `false`     |
| `options`         | `OptionsItemShape[]`                                                              | Predefined list of options.                       | No       | `[]`        |
| `enable_search`   | `boolean`                                                                         | Enables searching within the friend list.         | No       | `false`     |
| `disable_uncheck` | `boolean`                                                                         | Prevents unselecting if required.                 | No       | `false`     |
| `choice_type`     | `string`                                                                          | Type of choice mechanism.                         | No       | `undefined` |
| `placeholder`     | `string`                                                                          |                                                   | No       | `undefined` |
| `showWithoutOptions`| `boolean`                                                                         | Whether to show the field without options.        | No       | `undefined` |
| `api_endpoint`    | `string`                                                                          | API endpoint to fetch friend suggestions.         | Yes      | `undefined` |
| `disabled`        | `boolean`                                                                         |                                                   | No       | `false`     |

## GatewayButton

Renders a button specific to a payment gateway (e.g., Apple Pay, Stripe). It handles setting the selected gateway ID, passing relevant data, and triggering form submission upon click. It can display platform-specific buttons (Apple Pay/Google Pay) or a generic button based on the `variant` prop.

### Props

| Name             | Type                                                                               | Description                                                                                                | Required | Default    |
| :--------------- | :--------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :--------- |
| `label`          | `string`                                                                           |                                                                                                            | Yes      |            |
| `gateway_id`     | `string \| number`                                                                 | The unique identifier for the payment gateway this button represents.                                      | Yes      |            |
| `variant`        | `'applepay' \| 'googlepay' \| 'stripe' \| 'paypal' \| 'activitypoint'`             | The type of gateway. Determines rendering logic, platform availability (Apple/Google Pay), and behavior. | Yes      |            |
| `item`           | `any`                                                                              | Item data associated with the payment, passed to the form on submission.                                   | Yes      |            |
| `gateway_config` | `any`                                                                              | Configuration specific to the selected payment gateway, passed to the form on submission.                  | Yes      |            |
| `description`    | `string`                                                                           |                                                                                                            | No       | `''`       |
| `icon`           | `string`                                                                           | Optional icon name (from the icon set) to display on the generic button.                                   | No       |            |
| `confirmation`   | `{ title: string, message: string }`                                               | Optional configuration for a confirmation dialog shown before submission (used for `activitypoint` variant). | No       |            |
| `disabled`       | `boolean`                                                                          |                                                                                                            | No       | `false`    |
| `fullWidth`      | `boolean`                                                                          |                                                                                                            | No       | `true`     |
| `margin`         | `'none' \| 'dense' \| 'normal' \| 'small'`                                         |                                                                                                            | No       | `'none'`   |
| `size`           | `'small' \| 'medium' \| 'large'`                                                   | Size applied to the underlying form control (affects spacing/layout).                                      | No       |            |

## Hidden

A form element that stores a value in the form state without rendering any visible UI element. It's typically used to pass data that shouldn't be directly modified by the user.

### Props

| Name             | Type     | Description                                                              | Required | Default |
| :--------------- | :------- | :----------------------------------------------------------------------- | :------- | :------ |
| `value`          | `string` | The specific value to set for the hidden field.                          | No       | `null`  |
| `defaultValue`   | `string` | The default value to set if `config.value` is not provided.            | No       | `null`  |

## HtmlLink

This element renders a button styled as a link. It's primarily used for navigation or triggering specific actions within a form, often without directly manipulating form field values. While named `HtmlLink` for consistency with web counterparts, it utilizes the `LinkButtonField` component internally for mobile implementation.

### Props

| Name          | Type                                               | Description                                                                                                                               | Required | Default             |
|---------------|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|----------|---------------------|
| `label`       | `string`                                           |                                                                                                                                           | Yes      | -                   |
| `textTransform`| `'none' \| 'capitalize' \| 'uppercase' \| 'lowercase'` | Controls the text transformation (e.g., uppercase, lowercase).                                                                            | No       | -                   |
| `margin`      | `'normal'`                                         |                                                                                                                                           | Yes      | -                   |
| `link`        | `string`                                           | A URL path to navigate to when the button is pressed. Used if `action` is not provided.                                                   | No       | -                   |
| `routerName`  | `string`                                           | The name of the route to navigate to, used with `actionName`. Primarily for navigation actions like 'reset'.                              | No       | `'forgot-password'` |
| `actionName`  | `string`                                           | Specifies the type of navigation action (e.g., 'reset', 'navigate'). Used if `action` is not provided.                                     | No       | `'navigate'`        |
| `action`      | `string`                                           | A Redux action type to dispatch when the button is pressed. Takes precedence over `link` and `actionName`/`routerName`.                   | No       | -                   |
| `actionPayload`| `Record<string, any>`                              | The payload to include with the dispatched Redux action specified by `action`.                                                            | No       | `{}`                |
| `description` | `string`                                           |                                                                                                                                           | No       | -                   |

## Information

Displays HTML content fetched based on the field's value, typically representing related information (e.g., a forum post).

### Props

| Name          | Type                                     | Description                                      | Required | Default     |
|---------------|------------------------------------------|--------------------------------------------------|----------|-------------|
| `fullWidth`   | `boolean`                                |                                                  | No       | `false`     |
| `margin`      | `'none' \| 'dense' \| 'normal'`            |                                                  | No       | `undefined` |
| `paddingBottom`| `'none' \| 'dense' \| 'normal'`            |                                                  | No       | `undefined` |
| `variant`     | `'standard' \| 'outlined' \| 'filled'`   | Sets the visual style.                           | No       | `'standard'`|
| `label`       | `string`                                 |                                                  | Yes      |             |
| `required`    | `boolean`                                |                                                  | No       | `false`     |

## input

A standard text input field allowing users to enter text. It wraps the `TextField` component, providing various configurations for appearance, behavior, validation, and integration with features like QR scanning and copy-to-clipboard.

### Props

| Name                 | Type                                                     | Description                                                                      | Required | Default         |
| :------------------- | :------------------------------------------------------- | :------------------------------------------------------------------------------- | :------- | :-------------- |
| `label`              | `string`                                                 |                                                                                  | No       |                 |
| `placeholder`        | `string`                                                 |                                                                                  | No       |                 |
| `description`        | `string`                                                 |                                                                                  | No       |                 |
| `variant`            | `'standard'`, `'outlined'`, `'filled'`, `'standard-outlined'`, `'livestream'` | Visual style of the input field.                                                 | No       | `'standard'`    |
| `fullWidth`          | `boolean`                                                |                                                                                  | No       | `false`         |
| `margin`             | `'none'`, `'dense'`, `'normal'`                          |                                                                                  | No       | `'normal'`      |
| `paddingBottom`      | `'none'`, `'dense'`, `'normal'`                          |                                                                                  | No       | `'normal'`      |
| `required`           | `boolean`                                                |                                                                                  | No       | `false`         |
| `disabled`           | `boolean`                                                |                                                                                  | No       | `false`         |
| `editable`           | `boolean`                                                | If false, the text is not editable (overridden by `disabled`).                   | No       | `true`          |
| `multiline`          | `boolean`                                                | If true, the input can span multiple lines.                                      | No       | `false`         |
| `minHeight`          | `number`                                                 |                                                                                  | No       |                 |
| `maxLength`          | `number`                                                 |                                                                                  | No       |                 |
| `autoFocus`          | `boolean`                                                |                                                                                  | No       | `false`         |
| `autoCorrect`        | `boolean`                                                | Enable/disable auto-correction.                                                  | No       | `true`          |
| `autoCapitalize`     | `'none'`, `'sentences'`, `'words'`, `'characters'`       | Auto-capitalization behavior.                                                    | No       | `'sentences'`   |
| `clearButtonMode`    | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Controls when the clear button appears (iOS only).                               | No       | `'never'`       |
| `validateAction`     | `string`                                                 | Name of a Redux action for server-side validation on blur.                       | No       |                 |
| `findReplace`        | `{ find: string, replace: string }`                      | Configuration for automatically replacing parts of the input value (e.g., slugify). | No       |                 |
| `contextualDescription`| `string`                                                 | Additional description text, often used with `findReplace`.                      | No       |                 |
| `hasQRScanner`       | `boolean`                                                | If true, displays a QR code scanner icon/button.                                 | No       | `false`         |
| `qrScannerParamName` | `string`                                                 | The query parameter name to extract from the scanned QR code URL.                | No       | `'invite_code'` |
| `hasCopy`            | `boolean`                                                | If true, displays a copy-to-clipboard icon/button.                               | No       | `false`         |
| `backgroundColor`    | `string`                                                 | Background color for the input container.                                        | No       |                 |

## InviteFriendPicker

A form element that allows users to select one or multiple friends to invite, typically fetching suggestions from an API endpoint. It opens a dedicated selection screen.

### Props

| Name            | Type                      | Description                                                      | Required | Default      |
| --------------- | ------------------------- | ---------------------------------------------------------------- | -------- | ------------ |
| `label`         | `string`                  |                                                                  | Yes      | `''`         |
| `api_endpoint`  | `string`                  | API endpoint URL to fetch friend suggestions.                    | Yes      | `''`         |
| `fullWidth`     | `boolean`                 |                                                                  | No       | `false`      |
| `margin`        | `'none' \| 'dense' \| 'normal'` |                                                                  | No       | `'normal'`   |
| `required`      | `boolean`                 |                                                                  | No       | `false`      |
| `variant`       | `'standard' \| 'outlined' \| 'filled'` | The display style variant of the form control.                 | No       | `'standard'` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` |                                                                  | No       | `'normal'`   |
| `suboptions`    | `SubOptionsShape`         | Configuration for sub-options within the picker.                 | No       | `undefined`  |
| `disable_custom`| `boolean`                 | If `true`, disables the custom privacy/selection option.         | No       | `false`      |
| `multiple`      | `boolean`                 | If `true`, allows selecting multiple friends.                    | No       | `false`      |
| `enable_search` | `boolean`                 | If `true`, enables search functionality within the picker screen. | No       | `false`      |
| `disable_uncheck`| `boolean`                 | If `true`, prevents users from unselecting chosen options.       | No       | `false`      |
| `choice_type`   | `string`                  | Specifies the type of choice (internal use).                     | No       | `''`         |
| `placeholder`   | `string`                  |                                                                  | No       | `''`         |
| `api_params`    | `Record<string, any>`     | Additional parameters sent with the API request.                 | No       | `{ q: ':q' }`|

## LinkButton

This form element renders a button styled as a link. It can be configured to navigate to a specific route/link or dispatch a Redux action upon being pressed. It's often used for actions like navigating to a "Forgot Password" screen or triggering secondary form actions.

### Props

| Name            | Type                                                    | Description                                                                                                | Required | Default           |
| --------------- | ------------------------------------------------------- | ---------------------------------------------------------------------------------------------------------- | -------- | ----------------- |
| `label`         | `string`                                                |                                                                                                            | Yes      |                   |
| `description`   | `string`                                                |                                                                                                            | No       |                   |
| `link`          | `string`                                                | A URL path (relative) to navigate to when pressed. Takes precedence over `actionName`/`routerName` if `action` is not set. | No       |                   |
| `action`        | `string`                                                | The type string of a Redux action to dispatch when pressed. Takes precedence over `link` and `actionName`/`routerName`. | No       |                   |
| `actionPayload` | `Record<string, any>`                                   | The payload object to send with the dispatched Redux `action`.                                             | No       | `{}`              |
| `actionName`    | `'navigate' \| 'reset'`                                 | Specifies the navigation action type. Used if `action` and `link` are not provided.                        | No       | `'navigate'`      |
| `routerName`    | `string`                                                | The name of the route to navigate to. Used with `actionName`.                                              | No       | `'forgot-password'` |
| `textTransform` | `'none' \| 'capitalize' \| 'uppercase' \| 'lowercase'` | CSS text-transform property for the button label.                                                          | No       | `'none'`          |
| `margin`        | `'normal'`                                              |                                                                                                            | No       | `'normal'`        |

## Location

A form field that allows users to select a geographical location using a native location picker interface. Clicking the field opens the picker, and the selected location's address is displayed.

### Props

| Name          | Type                                                                 | Description                                                                                                | Required | Default     |
| :------------ | :------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :---------- |
| `label`       | `string`                                                             |                                                                                                            | Yes      |             |
| `placeholder` | `string`                                                             |                                                                                                            | No       | `''`        |
| `variant`     | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined' \| 'livestream'` | Controls the visual style of the component.                                                                | No       | `'standard'`|
| `fullWidth`   | `boolean`                                                            |                                                                                                            | No       | `false`     |
| `margin`      | `'none' \| 'dense' \| 'normal'`                                        |                                                                                                            | No       | `'normal'`  |
| `paddingBottom`| `'none' \| 'dense' \| 'normal'`                                        |                                                                                                            | No       | `'normal'`  |
| `required`    | `boolean`                                                            |                                                                                                            | No       | `false`     |
| `disabled`    | `boolean`                                                            |                                                                                                            | No       | `false`     |
| `types`       | `PlaceType[]`                                                        | Filters the types of places returned by the location picker (e.g., 'address', 'geocode', 'establishment'). | No       | `undefined` |
| `inline`      | `boolean`                                                            | Controls if the label is displayed inline with the input.                                                  | No       | `false`     |

## MembershipQuestion

The `MembershipQuestion` form element allows users to define a question with different answer formats (Checkbox, Multiple Choice, or Written Answer) typically used for group membership applications. It includes fields for the question text, selecting the answer type, and managing answer options if applicable.

### Props

| Name                 | Type                                                       | Description                                                                      | Required | Default     |
| :------------------- | :--------------------------------------------------------- | :------------------------------------------------------------------------------- | :------- | :---------- |
| `label`              | string                                                     |                                                                                  | No       | `undefined` |
| `description`        | string                                                     |                                                                                  | No       | `undefined` |
| `required`           | boolean                                                    |                                                                                  | No       | `false`     |
| `multiline`          | boolean                                                    | Allows the question input field to accept multiple lines.                        | No       | `false`     |
| `clearButtonMode`    | 'never' \| 'while-editing' \| 'unless-editing' \| 'always' | Determines when the clear button appears on the text input (iOS only).           | No       | `undefined` |
| `disabled`           | boolean                                                    |                                                                                  | No       | `false`     |
| `maxLength`          | number                                                     |                                                                                  | No       | `5`         |
| `editable`           | boolean                                                    | Determines if the question text input can be edited.                             | No       | `true`      |
| `minHeight`          | number                                                     |                                                                                  | No       | `undefined` |
| `paddingBottom`      | string \| number                                           |                                                                                  | No       | `undefined` |
| `margin`             | string                                                     |                                                                                  | No       | `undefined` |
| `fullWidth`          | boolean                                                    |                                                                                  | No       | `false`     |

## MentionInput

The `MentionInput` element provides a text input field specifically designed for composing messages that can include user mentions (@username) and hashtags (#tag). It integrates with Formik for state management and validation.

### Props

| Name             | Type                                                                 | Description                                                                 | Required | Default            |
| :--------------- | :------------------------------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------------- |
| `label`          | `string`                                                             |                                                                             | Yes      | `''`               |
| `required`       | `boolean`                                                            |                                                                             | Yes      | `false`            |
| `variant`        | `'standard' \| 'outlined' \| 'filled' \| 'standard-inlined'`         | The visual style variant of the input.                                      | Yes      | `'standard-inlined'` |
| `margin`         | `'none' \| 'dense' \| 'normal'`                                      |                                                                             | Yes      | `'normal'`         |
| `fullWidth`      | `boolean`                                                            |                                                                             | No       | `false`            |
| `paddingBottom`  | `'none' \| 'dense' \| 'normal'`                                      |                                                                             | No       | `'none'`           |
| `editable`       | `boolean`                                                            | If false, the text content cannot be modified by the user.                  | No       | `true`             |
| `testId`         | `string`                                                             | A unique identifier used for testing purposes.                              | No       | `''`               |
| `meta`           | `MetaShape`                                                          | Additional metadata associated with the field.                              | No       | `{}`               |
| `inputWrapperStyle`| `ViewStyle`                                                        | Custom styles applied to the input's wrapping element.                      | No       | `{}`               |
| `containerStyle` | `ViewStyle`                                                        | Custom styles applied to the main container element.                        | No       | `{}`               |
| `styleLabel`     | `ViewStyle`                                                        | Custom styles applied to the label element.                                 | No       | `{}`               |

## MultiChoice

The `MultiChoice` form element allows users to select one or multiple options from a predefined list, typically presented using checkboxes when multiple selections are allowed. It is functionally equivalent to the `Select` element but configured for multiple selections.

### Props

| Name               | Type                               | Description                                                                 | Required | Default      |
| :----------------- | :--------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------- |
| `label`            | `string`                           |                                                                             | Yes      |              |
| `description`      | `string`                           |                                                                             | No       |              |
| `options`          | `OptionsItemShape[]`               | An array of available options to select from.                               | Yes      | `[]`         |
| `multiple`         | `boolean`                          | If true, allows selecting multiple options. Defaults to `true` for MultiChoice. | No       | `true`       |
| `required`         | `boolean`                          |                                                                             | No       | `false`      |
| `disabled`         | `boolean`                          |                                                                             | No       | `false`      |
| `variant`          | `'standard', 'outlined', 'filled'` | The visual style of the component.                                          | No       | `'standard'` |
| `margin`           | `'normal', 'dense', 'none'`        |                                                                             | No       | `'normal'`   |
| `fullWidth`        | `boolean`                          |                                                                             | No       | `false`      |
| `placeholder`      | `string`                           |                                                                             | No       | `'select'`   |
| `enable_search`    | `boolean`                          | If true, enables a search input within the option selector modal.           | No       | `false`      |
| `disableClearable` | `boolean`                          | If true, prevents the user from clearing the selection (requires a value).  | No       | `false`      |
| `value_type`       | `string`                           | Specifies the expected data type of the value ('array' or single value).    | No       | `'array'`    |
| `suboptions`       | `SubOptionsShape`                  | Defines sub-options, often used for dependent selections.                   | No       | `undefined`  |
| `useSectionList`   | `boolean`                          | If true, uses a SectionList for displaying options (for grouped options).   | No       | `false`      |
| `showWithoutOptions`| `boolean`                          | If true, renders the component even if no options are provided.             | No       | `false`      |

*Note: `OptionsItemShape` typically has `{ label: string, value: string | number }` structure. `SubOptionsShape` structure depends on implementation.*

## MultiFile

Allows users to select and upload multiple files (photos, videos, or other types based on configuration). This element is an alias for the `Attachment` element but typically used when multiple file selection is intended.

### Props

| Name                  | Type                                       | Description                                                                 | Required | Default            |
| :-------------------- | :----------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------------- |
| `label`               | `string`                                   |                                                                             | Yes      | -                  |
| `description`         | `string`                                   |                                                                             | No       | -                  |
| `multiple`            | `boolean`                                  | Allow selecting multiple files. Set to `true` for multi-file selection.     | No       | `false`            |
| `file_type`           | `string`                                   | The type of file allowed ('photo', 'video', 'attachment', etc.).            | No       | `'photo'`          |
| `item_type`           | `string`                                   | The resource type associated with the uploaded item (e.g., 'photo', 'blog'). | No       | `'unknown'`        |
| `max_files`           | `number`                                   | Maximum number of files allowed.                                            | No       | `10`               |
| `min_files`           | `number`                                   | Minimum number of files required.                                           | No       | `1`                |
| `max_upload_filesize` | `object` (`{ photo: number, video: number }`) | Maximum upload size per file type in bytes.                                 | No       | -                  |
| `isVideoUploadAllowed`| `boolean`                                  | Explicitly allow video uploads alongside photos.                            | No       | `false`            |
| `cropping`            | `boolean`                                  | Enable image cropping after selection.                                      | No       | `false`            |
| `include_exif`        | `boolean`                                  | Include EXIF data with uploaded images.                                     | No       | `false`            |
| `maxFilesDescription` | `string`                                   | Custom description related to the maximum file limit.                       | No       | -                  |
| `current_files`       | `array`                                    | Array of pre-existing file objects (used for editing).                      | No       | `[]`               |
| `fullWidth`           | `boolean`                                  |                                                                             | No       | `false`            |
| `margin`              | `'normal' \| 'dense' \| 'none'`            |                                                                             | No       | `'normal'`         |
| `variant`             | `string`                                   | The display variant of the form control.                                    | No       | `'standard-inlined'` |
| `required`            | `boolean`                                  |                                                                             | No       | `false`            |
| `disabled`            | `boolean`                                  |                                                                             | No       | `false`            |
| `name`                | `string`                                   | The name of the field in the form state.                                    | Yes      | -                  |
| `paddingBottom`       | `string`                                   |                                                                             | No       | -                  |

## NumberCode

A form input element designed for entering numerical codes (like One-Time Passwords) digit by digit into separate input boxes.

### Props

| Name                  | Type                                | Description                                                    | Required | Default      |
| :-------------------- | :---------------------------------- | :------------------------------------------------------------- | :------- | :----------- |
| `label`               | `string`                            |                                                                | No       | `undefined`  |
| `editable`            | `boolean`                           | Determines if the input fields are editable.                   | No       | `true`       |
| `variant`             | `'standard' \| 'outlined' \| 'filled'` | The visual style variant of the form control.                  | No       | `'standard'` |
| `paddingBottom`       | `'dense' \| 'normal' \| 'none'`     |                                                                | No       | `'dense'`    |
| `margin`              | `'dense' \| 'normal' \| 'none'`     |                                                                | No       | `undefined`  |
| `required`            | `boolean`                           |                                                                | No       | `false`      |
| `fullWidth`           | `boolean`                           |                                                                | No       | `false`      |
| `clearInputs`         | `boolean`                           | Controls input clearing behavior on press.                     | No       | `false`      |
| `isAutoFillSupported` | `boolean`                           | Enables native OTP autofill support if available.              | No       | `false`      |
| `isAutoFocus`         | `boolean`                           |                                                                | No       | `false`      |
| `codeLength`          | `number`                            | The number of digits/input boxes for the code.                 | No       | `6`          |
| `keyboardType`        | `TextInputProps['keyboardType']`    | Specifies the type of keyboard to display (e.g., 'numeric'). | No       | `'numeric'`  |

## Password

The `Password` element provides a secure text input field specifically designed for entering passwords. It includes a toggle button to show or hide the entered password for user convenience. It integrates with Formik for form state management.

### Props

The component accepts standard `FormFieldProps` along with a `config` object for specific customizations.

| Name             | Type                                                              | Description                                                                 | Required | Default      |
| :--------------- | :---------------------------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------- |
| `label`          | `string`                                                          |                                                                             | No       | `''`         |
| `placeholder`    | `string`                                                          |                                                                             | No       | `''`         |
| `required`       | `boolean`                                                         |                                                                             | No       | `false`      |
| `disabled`       | `boolean`                                                         |                                                                             | No       | `false`      |
| `variant`        | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined'` | Defines the visual style of the input field (e.g., border, background).     | No       | `'standard'` |
| `margin`         | `'none' \| 'dense' \| 'normal'`                                   |                                                                             | No       | `'normal'`   |
| `fullWidth`      | `boolean`                                                         |                                                                             | No       | `false`      |
| `editable`       | `boolean`                                                         | If `false`, the text content cannot be modified by the user.                | No       | `true`       |
| `returnKeyType`  | `ReturnKeyTypeOptions`                                            | Specifies the appearance of the keyboard's return key.                      | No       | `'next'`     |
| `inputWapperStyle` | `ViewStyle`                                                       | Custom styles applied to the wrapper view containing the `TextInput`.       | No       | `undefined`  |
| `containerStyle` | `ViewStyle`                                                       | Custom styles applied to the outermost container of the component.          | No       | `undefined`  |
| `styleLabel`     | `ViewStyle`                                                       | Custom styles applied specifically to the label text component.             | No       | `undefined`  |
| *Other*          | `TextInputProps`                                                  | Accepts other standard React Native `TextInput` props.                      | No       | `undefined`  |

## PointConversionAmountReceived

Displays a calculated monetary amount based on a value from another form field, an exchange rate, and a fee percentage. The result is formatted according to a specified currency pattern.

### Props

| Name                | Type     | Description                                                                          | Required | Default |
| :------------------ | :------- | :----------------------------------------------------------------------------------- | :------- | :------ |
| `label`             | `string` |                                                                                      | Yes      |         |
| `exchangeRate`      | `number` | The numerical exchange rate used for conversion.                                     | Yes      |         |
| `exchangeRatePattern`| `object` | An object defining the currency formatting rules (e.g., separators, precision). | Yes      |         |
| `feePercentage`     | `number` | The fee percentage to be deducted (e.g., 0.05 for 5%).                               | Yes      |         |
| `relatedField`      | `string` | The name of the form field providing the base value for the calculation.             | Yes      |         |

## PollAnswer

A form element for managing a list of poll answers. Allows users to add, edit, and delete answer options, enforcing minimum/maximum answer counts and character limits per answer.

### Props

| Name         | Type    | Description                                       | Required | Default     |
| :----------- | :------ | :------------------------------------------------ | :------- | :---------- |
| `minAnswers` | number  | Minimum number of answers required.             | Yes      | *Varies*    |
| `maxAnswers` | number  | Maximum number of answers allowed (0=unlimited). | Yes      | *Varies*    |
| `maxLength`  | number  |                                                   | No       | `undefined` |
| `disabled`   | boolean |                                                   | No       | `false`     |
| `variant`    | string  | Visual style variant ('standard', 'standard-outlined'). | No       | `'standard'`|
| `fullWidth`  | boolean |                                                   | No       | `false`     |

## PollCloseTime

This element renders a date and time picker input field, specifically configured for selecting the closing time of a poll. It utilizes the underlying `DatePickerField` component.

### Props

| Name          | Type                               | Description                                                                 | Required | Default             |
|---------------|------------------------------------|-----------------------------------------------------------------------------|----------|---------------------|
| `label`       | `string`                           |                                                                             | No       | `'close_time'`      |
| `placeholder` | `string`                           |                                                                             | No       |                     |
| `description` | `string`                           |                                                                             | No       |                     |
| `required`    | `boolean`                          |                                                                             | No       | `false`             |
| `disabled`    | `boolean`                          |                                                                             | No       | `false`             |
| `fullWidth`   | `boolean`                          |                                                                             | No       | `false`             |
| `margin`      | `'dense' \| 'normal' \| 'none'`    |                                                                             | No       | `'normal'`          |
| `variant`     | `'standard' \| 'outlined' \| 'filled'` | Defines the visual style of the input field.                             | No       | `'standard'`        |
| `datePickerMode` | `'date' \| 'time' \| 'datetime'` | Determines the type of picker displayed (date, time, or both).          | No       | `'datetime'`        |
| `displayFormat` | `string`                           | The format used to display the selected date and time in the input field. | No       | `'DD/MM/YYYY - HH:mm'` |
| `minDate`     | `string`                           | The earliest selectable date/time (ISO 8601 format string).                 | No       |                     |
| `maxDate`     | `string`                           | The latest selectable date/time (ISO 8601 format string).                   | No       |                     |
| `time_zone_gmt` | `string`                           | Timezone identifier (e.g., 'America/New_York') for calculations.          | No       | User's setting    |
| `timeFormat`  | `12 \| 24`                         | Specifies whether to use 12-hour or 24-hour format in the time picker.    | No       | User's setting    |
| `startOfDay`  | `boolean`                          | If `true`, sets the selected time to the beginning of the day (00:00:00).   | No       | `false`             |
| `endOfDay`    | `boolean`                          | If `true`, sets the selected time to the end of the day (23:59:59).         | No       | `false`             |

## Price

Renders a set of price input fields, often used for different currencies or price types. The actual input fields are defined by the `options` prop. This component conditionally renders different implementations based on the API version, but this documentation focuses on the behavior for API version 5.1.8 and later.

### Props

| Name          | Type                                                                                                | Description                                                                                                                               | Required | Default      |
|---------------|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|----------|--------------|
| `label`       | `string`                                                                                            |                                                                                                                                           | Yes      | -            |
| `description` | `string`                                                                                            |                                                                                                                                           | No       | -            |
| `variant`     | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined'`                                     | The visual style of the field.                                                                                                            | No       | `'standard'` |
| `options`     | `Array<{ key: string, name: string, required?: boolean, requiredWhen?: object, ... }>`             | Defines the individual price inputs (e.g., currencies). Each object requires `key` (label/value key) and `name`. Can include `required`. | Yes      | `[]`         |
| `maxLength`   | `number`                                                                                            |                                                                                                                                           | No       | -            |
| `required`    | `boolean`                                                                                           |                                                                                                                                           | No       | `false`      |
| `disabled`    | `boolean`                                                                                           |                                                                                                                                           | No       | `false`      |
| `fullWidth`   | `boolean`                                                                                           |                                                                                                                                           | No       | `false`      |
| `margin`      | `'normal' \| 'dense' \| 'none'`                                                                     |                                                                                                                                           | No       | -            |
| `paddingBottom`| `string \| number`                                                                                  |                                                                                                                                           | No       | -            |
| `findReplace` | `{ find: string \| RegExp, replace: string }`                                                       | Defines rules for replacing characters in the input value.                                                                                | No       | -            |

*Note: The component also accepts other standard `FormFieldProps` like `formik` which are not detailed here.*

## Privacy

This element provides a user interface for selecting privacy settings, typically used for controlling who can see a piece of content (e.g., a post). It displays the currently selected privacy option (with an icon and label) and opens a dedicated selector view (`SelectPrivacyView`) when tapped.

### Props

| Name             | Type                                  | Description                                                                 | Required | Default            |
| :--------------- | :------------------------------------ | :-------------------------------------------------------------------------- | :------- | :----------------- |
| `label`          | `string`                              |                                                                             | Yes      |                    |
| `options`        | `PrivacyOptionItemShape[]`            | An array of predefined privacy options available for selection.             | Yes      | `[]`               |
| `name`           | `string`                              | The unique identifier for the field within the form.                        | Yes      |                    |
| `fullWidth`      | `boolean`                             |                                                                             | No       | `false`            |
| `margin`         | `'dense' \| 'normal' \| 'none'`       |                                                                             | No       | `'normal'`         |
| `required`       | `boolean`                             |                                                                             | No       | `false`            |
| `variant`        | `'standard' \| 'outlined' \| 'filled' \| 'standard-inlined' \| 'livestream'` | The visual style variant of the component.                                  | No       | `'standard-inlined'` |
| `suboptions`     | `SubOptionsShape`                     | Additional options, often used for custom privacy lists or friend lists.    | No       | `[]`               |
| `disable_custom` | `boolean`                             | If `true`, prevents users from selecting custom privacy options.            | No       | `false`            |
| `multiple`       | `boolean`                             | If `true`, allows selecting multiple privacy options (currently single).    | No       | `false`            |
| `paddingBottom`  | `'dense' \| 'normal' \| 'none'`       |                                                                             | No       | `undefined`        |
| `description`    | `string`                              |                                                                             | No       | `undefined`        |
| `disabled`       | `boolean`                             |                                                                             | No       | `false`            |

## Progress

Renders a progress bar indicating the completion status, typically used within multi-step forms. It calculates progress based on a related field (representing the current step/value) and the total number of steps/value (expected in the form context).

### Props

| Name                | Type                                | Description                                                                                             | Required | Default      |
| :------------------ | :---------------------------------- | :------------------------------------------------------------------------------------------------------ | :------- | :----------- |
| `margin`            | `'none' \| 'dense' \| 'normal'`   |                                                                                                         | No       | `'normal'`   |
| `variant`           | `'standard' \| 'outlined' \| 'filled'` | The display variant of the form control.                                                              | No       | `'standard'` |
| `paddingTop`        | `'none' \| 'dense' \| 'normal'`   | Sets the top inner padding of the form control.                                                         | No       | `undefined`  |
| `paddingBottom`     | `'none' \| 'dense' \| 'normal'`   |                                                                                                         | No       | `undefined`  |
| `paddingRight`      | `'none' \| 'dense' \| 'normal'`   | Sets the right inner padding of the form control.                                                       | No       | `undefined`  |
| `paddingLeft`       | `'none' \| 'dense' \| 'normal'`   | Sets the left inner padding of the form control.                                                        | No       | `undefined`  |
| `relatedField`      | `string`                            | The name of the form field holding the current value (e.g., current step) for progress calculation. | Yes      |              |

## question

This element renders a standard text input field. It is an alias for the `Text` element (`form.element.Text`).

### Props

| Name                  | Type                                                     | Description                                                                 | Required | Default         |
| --------------------- | -------------------------------------------------------- | --------------------------------------------------------------------------- | -------- | --------------- |
| `label`               | `string`                                                 |                                                                             | No       |                 |
| `placeholder`         | `string`                                                 |                                                                             | No       |                 |
| `description`         | `string`                                                 |                                                                             | No       |                 |
| `contextualDescription`| `string`                                                 | Additional description shown below the input, often used for dynamic info. | No       |                 |
| `variant`             | `'standard'`, `'outlined'`, `'filled'`, `'livestream'` etc. | The visual style variant of the input field.                                | No       | `'standard'`    |
| `fullWidth`           | `boolean`                                                |                                                                             | No       | `false`         |
| `margin`              | `'normal'`, `'dense'`, `'none'` etc.                     |                                                                             | No       | `'normal'`      |
| `paddingBottom`       | `'normal'`, `'dense'`, `'none'` etc.                     |                                                                             | No       |                 |
| `required`            | `boolean`                                                |                                                                             | No       | `false`         |
| `disabled`            | `boolean`                                                |                                                                             | No       | `false`         |
| `editable`            | `boolean`                                                | If `false`, the text field value cannot be changed.                         | No       | `true`          |
| `multiline`           | `boolean`                                                | If `true`, allows multiple lines of text input.                             | No       | `false`         |
| `minHeight`           | `number`                                                 |                                                                             | No       |                 |
| `maxLength`           | `number`                                                 |                                                                             | No       |                 |
| `autoCorrect`         | `boolean`                                                | Controls whether autocorrection should be enabled.                          | No       | `true`          |
| `autoCapitalize`      | `'none'`, `'sentences'`, `'words'`, `'characters'`       | Controls how text input is automatically capitalized.                       | No       | `'sentences'`   |
| `autoFocus`           | `boolean`                                                |                                                                             | No       | `false`         |
| `keyboardType`        | `string`                                                 | Specifies the type of keyboard to display (e.g., 'numeric', 'email-address'). | No       | `'default'`     |
| `returnKeyType`       | `string`                                                 | Specifies the appearance of the return key (e.g., 'done', 'next').          | No       | `'done'`        |
| `secureTextEntry`     | `boolean`                                                | If `true`, masks the text entered (for passwords).                          | No       | `false`         |
| `clearButtonMode`     | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Controls when the standard clear button appears in the text field (iOS only). | No       | `'never'`       |
| `validateAction`      | `string`                                                 | Name of a resource action used for asynchronous backend validation on blur. | No       |                 |
| `findReplace`         | `{ find: string, replace: string }`                      | Configuration to display a transformed version of the input (e.g., slug).   | No       |                 |
| `hasQRScanner`        | `boolean`                                                | If `true`, displays a QR code scanner icon button.                          | No       | `false`         |
| `qrScannerParamName`  | `string`                                                 | The URL query parameter name to extract when using the QR scanner.          | No       | `'invite_code'` |
| `hasCopy`             | `boolean`                                                | If `true`, displays a copy-to-clipboard icon button.                        | No       | `false`         |
| `backgroundColor`     | `string`                                                 | Sets a custom background color for the input field.                         | No       |                 |

*Note: This component inherits standard `TextInput` props. Only the most common and element-specific configuration props are listed here.*

## QuizQuestion

A form element for creating and managing a list of quiz questions, each with multiple answers and a designated correct answer. Users can add/remove questions and answers within specified limits.

### Props

| Name              | Type                                    | Description                                                                 | Required | Default     |
| :---------------- | :-------------------------------------- | :-------------------------------------------------------------------------- | :------- | :---------- |
| `label`           | `string`                                |                                                                             | Yes      |             |
| `fullWidth`       | `boolean`                               |                                                                             | No       | `true`      |
| `margin`          | `'normal'`, `'dense'`, `'none'`         |                                                                             | No       | `'normal'`  |
| `required`        | `boolean`                               |                                                                             | No       | `false`     |
| `variant`         | `'standard'`, `'outlined'`, `'filled'`  | The display style variant of the form control.                              | No       | `'standard'`|
| `paddingBottom`   | `'normal'`, `'dense'`, `'none'`         |                                                                             | No       | `'normal'`  |
| `minQuestions`    | `number`                                | The minimum number of questions required.                                   | No       | `1`         |
| `maxQuestions`    | `number`                                | The maximum number of questions allowed.                                    | No       | `10`        |
| `minAnswers`      | `number`                                | The minimum number of answers required per question.                        | No       | `2`         |
| `maxAnswers`      | `number`                                | The maximum number of answers allowed per question.                         | No       | `20`        |
| `defaultAnswers`  | `number`                                | The default number of answer fields to show when adding a new question.     | No       | `2`         |
| `disabled`        | `boolean`                               |                                                                             | No       | `false`     |
| `maxLength`       | `number`                                |                                                                             | No       | `undefined` |
| `maxAnswerLength` | `number`                                | The maximum character length allowed for each answer text.                  | No       | `undefined` |

## RadioGroup

A form element that displays a group of radio buttons, allowing the user to select a single option.

### Props

| Name                | Type                                                                 | Description                                                                                                | Required | Default |
| :------------------ | :------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :------ |
| `label`             | `string`                                                             |                                                                                                            | Yes      |         |
| `options`           | `Array<{label: string, value: any, description?: string}>`           | An array of objects defining each radio button. Each object needs `label` and `value`. `description` is optional. | Yes      | `[]`    |
| `description`       | `string`                                                             |                                                                                                            | No       | `''`    |
| `required`          | `boolean`                                                            |                                                                                                            | No       | `false` |
| `initialValue`      | `string`                                                             | The initial value/selection for the radio group.                                                           | No       | `''`    |
| `variant`           | `'outlined' \| 'filled' \| 'standard' \| 'horizontal' \| 'vertical'` | The visual style variant.                                                                                  | No       |         |
| `order`             | `number`                                                             | Optional number to prefix the label for ordering.                                                          | No       |         |

## RadioLabelGroup

Renders a group of radio buttons, visually styled using circular icons, allowing the user to select only one option from a list. This element is typically used for membership questions or similar single-choice scenarios within a form.

### Props

| Name              | Type                                                                 | Description                                                                                                | Required | Default     |
| :---------------- | :------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :---------- |
| `label`           | `string`                                                             |                                                                                                            | Yes      |             |
| `options`         | `Array<{ value: string, label?: string, disable?: boolean }>`        | An array of objects defining each radio option. `value` is required, `label` and `disable` are optional. | Yes      | `[]`        |
| `variant`         | `'standard' \| 'outlined' \| 'filled' \| string`                     | The visual style variant of the form control.                                                              | No       | `'standard'`|
| `margin`          | `'normal' \| 'dense' \| 'none' \| string`                            |                                                                                                            | No       | `'normal'`  |
| `fullWidth`       | `boolean`                                                            |                                                                                                            | No       | `false`     |
| `disabled`        | `boolean`                                                            |                                                                                                            | No       | `false`     |
| `required`        | `boolean`                                                            |                                                                                                            | No       | `false`     |
| `hasFormOrder`    | `boolean`                                                            | If `true`, prepends the `order` number to the `label`.                                                     | No       | `false`     |
| `order`           | `number`                                                             | The numerical order to display before the label when `hasFormOrder` is `true`.                             | No       |             |
| `paddingBottom`   | `string`                                                             |                                                                                                            | No       |             |

## Range

A form element that renders a dual-handle slider, allowing users to select a range of values. It uses two separate field names (defined in `min.name` and `max.name` props) to store the selected minimum and maximum values in the form state.

### Props

| Name          | Type                                                     | Description                                                                                                | Required | Default     |
|---------------|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------|----------|-------------|
| `label`       | `string`                                                 |                                                                                                            | No       |             |
| `description` | `string`                                                 |                                                                                                            | No       |             |
| `required`    | `boolean`                                                |                                                                                                            | No       | `false`     |
| `fullWidth`   | `boolean`                                                |                                                                                                            | No       | `false`     |
| `margin`      | `'none' \| 'dense' \| 'normal'`                        |                                                                                                            | No       | `'normal'`  |
| `paddingBottom`| `'none' \| 'dense' \| 'normal'`                         |                                                                                                            | No       |             |
| `variant`     | `'standard' \| 'outlined' \| 'filled'`                 | The visual style variant of the form control.                                                              | No       | `'standard'`|
| `step`        | `number`                                                 | The granularity that the slider can step through values.                                                   | Yes      |             |
| `min`         | `object { label: string, name: string, value: number }`  | Config for the minimum value handle. `name` is the formik field name, `value` is the slider minimum limit. | Yes      |             |
| `max`         | `object { label: string, name: string, value: number }`  | Config for the maximum value handle. `name` is the formik field name, `value` is the slider maximum limit. | Yes      |             |

## ResetSearch

This element renders a button used within a search or filter form. When clicked, it resets the values of specified form fields (`targetFields`) back to their initial state as defined in the form's `initialValues`. The button is automatically hidden if the target fields currently hold their default values.

### Props

| Name           | Type     | Description                                                                 | Required | Default                           |
| -------------- | -------- | --------------------------------------------------------------------------- | -------- | --------------------------------- |
| `targetFields` | `string[]` | An array of field names within the form that this component should reset. | No       | `['sort', 'when', 'category_id']` |
| `label`        | `string` |                                                                             | No       | `'reset'`                         |
| `title`        | `string` | A title associated with the element (specific usage may vary).              | No       | `'filter'`                        |
| `align`        | `string` | Alignment setting (specific usage may vary).                                | No       | `'right'`                         |
| `variant`      | `string` | Controls the visual style or variant of the form control wrapper.           | No       | `'standard'`                      |

## Row

Renders child form elements horizontally in a row, allowing control over their alignment.

### Props

| Name           | Type                                                                                   | Description                                                    | Required | Default         |
| -------------- | -------------------------------------------------------------------------------------- | -------------------------------------------------------------- | -------- | --------------- |
| `elements`     | `Record<string, FormElementConfig>`                                                    | Configuration for child form elements to render within the row | Yes      |                 |
| `justifyContent` | `'space-between' \| 'flex-start' \| 'flex-end' \| 'center' \| 'space-around' \| 'space-evenly'` | Specifies the alignment of child elements along the main axis. | No       | `'space-between'` |
| `style`        | `ViewStyle`                                                                            | Custom styles applied to the row container.                    | No       |                 |

## SearchBox

A form element intended for search input fields. Currently, this component displays a "Coming Soon" placeholder, indicating the feature is under development.

### Props

| Name             | Type      | Description                                                     | Required | Default    |
| :--------------- | :-------- | :-------------------------------------------------------------- | :------- | :--------- |
| `placeholder`      | `string`  |                                                                 | No       |            |
| `size`             | `string`  | Defines the size of the input field (e.g., 'small', 'medium').  | No       |            |
| `margin`           | `string`  |                                                                           | No       | `'normal'` |
| `fullWidth`        | `boolean` |                                                                           | No       | `true`     |
| `className`        | `string`  | An optional CSS class name to apply to the component for styling. | No       |            |

## Select

The `Select` form element provides a dropdown or list interface for users to choose one or multiple options from a predefined set. It supports various configurations like search, multiple selections, and different visual styles.

### Props

| Name                 | Type                                                                                             | Description                                                                 | Required | Default     |
| :------------------- | :----------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :---------- |
| `label`              | `string`                                                                                         |                                                                             | Yes      |             |
| `options`            | `OptionsItemShape[]`                                                                             | An array of available options for the select field.                         | Yes      | `[]`        |
| `fullWidth`          | `boolean`                                                                                        |                                                                             | No       | `false`     |
| `margin`             | `'none' \| 'dense' \| 'normal'`                                                                  |                                                                             | No       | `'normal'`  |
| `required`           | `boolean`                                                                                        |                                                                             | No       | `false`     |
| `variant`            | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined' \| 'livestream'`                    | The visual style variant of the select field.                               | No       | `'standard'`|
| `paddingBottom`      | `'none' \| 'dense' \| 'normal'`                                                                  |                                                                             | No       | `'normal'`  |
| `suboptions`         | `SubOptionsShape`                                                                                | Additional options grouped under main options (e.g., for dependent selects). | No       | `undefined` |
| `multiple`           | `boolean`                                                                                        | If `true`, allows selecting multiple options.                               | No       | `false`     |
| `disable_custom`     | `boolean`                                                                                        | If `true`, disables the ability to add custom options (if applicable).      | No       | `false`     |
| `value_type`         | `string`                                                                                         | Specifies the type of value to store (e.g., 'array').                       | No       | `undefined` |
| `enable_search`      | `boolean`                                                                                        | If `true`, enables a search input within the options list.                  | No       | `false`     |
| `disableClearable`   | `boolean`                                                                                        | If `true`, prevents the user from clearing the selected value.              | No       | `false`     |
| `choice_type`        | `string`                                                                                         | Specifies the type of choice control (e.g., 'radio', 'checkbox').           | No       | `undefined` |
| `placeholder`        | `string`                                                                                         |                                                                             | No       | `'select'`  |
| `showWithoutOptions` | `boolean`                                                                                        | If `true`, renders the field even if the `options` array is empty.          | No       | `false`     |
| `useSectionList`     | `boolean`                                                                                        | If `true`, uses a SectionList to display options (requires specific data structure). | No       | `false`     |
| `disabled`           | `boolean`                                                                                        |                                                                             | No       | `false`     |
| `description`        | `string`                                                                                         |                                                                             | No       | `undefined` |
| `resetValue`         | `boolean`                                                                                        | If `true`, indicates the value should be reset under certain conditions.    | No       | `false`     |

## SelectSubForm

This element renders a touchable area displaying an icon and the label of the currently selected option. Tapping it opens a bottom sheet containing a sub-form where the user can select one or multiple options from a predefined list (`options` and `suboptions`).

### Props

The component accepts standard `FormFieldProps` (`name`, `disabled`, `formik`) and a `config` object with the following properties:

| Name               | Type                                | Description                                                                                                | Required | Default      |
| :----------------- | :---------------------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :----------- |
| `fullWidth`        | `boolean`                           |                                                                                                            | No       | `false`      |
| `margin`           | `'dense' \| 'normal' \| 'none'`     |                                                                                                            | No       | `'normal'`   |
| `required`         | `boolean`                           |                                                                                                            | No       | `false`      |
| `variant`          | `'standard' \| 'outlined' \| ...` | Visual style variant of the control.                                                                       | No       | `'standard'` |
| `paddingBottom`    | `'dense' \| 'normal' \| 'none'`     |                                                                                                            | No       | `undefined`  |
| `label`            | `string`                            |                                                                                                            | No       | `''`         |
| `options`          | `OptionsItemShape[]`                | An array of primary options to be displayed in the sub-form.                                               | Yes      | `[]`         |
| `suboptions`       | `SubOptionsShape`                   | An object containing secondary options, often dependent on the primary selection.                          | No       | `undefined`  |
| `initialValue`     | `any`                               | The initial value of the form field.                                                                       | No       | `undefined`  |
| `disable_custom`   | `boolean`                           | If true, disables the ability to add custom options in the sub-form.                                       | No       | `false`      |
| `value_type`       | `string`                            | Specifies the data type of the value (e.g., 'string', 'number').                                           | No       | `undefined`  |
| `multiple`         | `boolean`                           | If true, allows multiple options to be selected in the sub-form.                                           | No       | `false`      |
| `enable_search`    | `boolean`                           | If true, enables a search input within the sub-form.                                                       | No       | `false`      |
| `disable_uncheck`  | `boolean`                           | If true, prevents users from deselecting an already selected option.                                       | No       | `false`      |
| `choice_type`      | `string`                            | Defines the selection mechanism in the sub-form (e.g., 'radio', 'checkbox').                               | No       | `undefined`  |
| `placeholder`      | `string`                            |                                                                                                            | No       | `undefined`  |
| `showWithoutOptions`| `boolean`                           | If true, the element is rendered even when no `options` are provided.                                      | No       | `false`      |
| `useSectionList`   | `boolean`                           | If true, the sub-form uses a `SectionList` for displaying options, suitable for grouped data.              | No       | `false`      |
| `icon`             | `string`                            | The name of the Lineficon icon to display next to the selected value.                                      | Yes      | `''`         |

## SFAutocomplete

The `SFAutocomplete` element provides an autocomplete input field, allowing users to search and select one or multiple options from a predefined list or dynamically fetched data source. It opens a bottom sheet for option selection.

### Props

| Name              | Type                     | Description                                                                          | Required | Default    |
| :---------------- | :----------------------- | :----------------------------------------------------------------------------------- | :------- | :--------- |
| `fullWidth`       | `boolean`                |                                                                                      | No       | `false`    |
| `margin`          | `normal`, `dense`, `none` |                                                                                      | No       | `normal`   |
| `required`        | `boolean`                |                                                                                      | No       | `false`    |
| `variant`         | `standard`, `outlined`   | Visual style variant.                                                                | No       | `standard` |
| `paddingBottom`   | `normal`, `dense`, `none` |                                                                                      | No       | `normal`   |
| `label`           | `string`                 |                                                                                      | No       | `''`       |
| `multiple`        | `boolean`                | Allow multiple selections.                                                           | No       | `false`    |
| `disable_uncheck` | `boolean`                | Prevent unselecting the current value (makes selection required if a value exists). | No       | `false`    |
| `search_endpoint` | `string`                 | API endpoint URL to fetch options dynamically.                                       | No       | `undefined`|
| `search_params`   | `object`                 | Additional parameters for the search API endpoint.                                   | No       | `{}`       |
| `valueKey`        | `string`                 | Key to use for the option's value.                                                   | No       | `'id'`     |
| `labelKey`        | `string`                 | Key to use for the option's display label.                                           | No       | `'name'`   |
| `useOptionContext`| `boolean`                | Whether to use a shared option context for managing selected options.                | No       | `false`    |
| `option_default`  | `Array<any>`             | Default options to use if `useOptionContext` is true and no context value exists.    | No       | `[]`       |
| `canLoadMore`     | `boolean`                | Whether more options can be loaded (pagination) from the search endpoint.            | No       | `false`    |
| `placeholder`     | `string`                 |                                                                                      | No       | `undefined`|
| `options`         | `OptionsItemShape[]`     | Predefined options list (used if `search_endpoint` is not provided).                 | No       | `[]`       |

## SFDate

A form element that allows users to select a date, time, or both using a native modal picker. It displays the selected value in a specified format.

### Props

| Name               | Type                         | Description                                                                              | Required | Default             |
|--------------------|------------------------------|------------------------------------------------------------------------------------------|----------|---------------------|
| `fullWidth`        | `boolean`                    |                                                                                          | No       | `false`             |
| `margin`           | `'none' \| 'dense' \| 'normal'` |                                                                                          | No       | `'normal'`          |
| `paddingBottom`    | `'none' \| 'dense' \| 'normal'` |                                                                                          | No       | `'none'`            |
| `variant`          | `'standard' \| 'outlined' \| 'filled'` | The visual style variant of the input field.                                             | No       | `'standard'`        |
| `time_zone_gmt`    | `string`                     | The GMT timezone string (e.g., 'Asia/Ho_Chi_Minh') for date calculations.                | No       | `undefined`         |
| `label`            | `string`                     |                                                                                          | No       | `'close_time'`      |
| `placeholder`      | `string`                     |                                                                                          | No       | `undefined`         |
| `required`         | `boolean`                    |                                                                                          | No       | `false`             |
| `editable`         | `boolean`                    | If `false`, the text input part is not directly editable (picker still works).           | No       | `true`              |
| `minDate`          | `string`                     | The minimum selectable date/time (ISO 8601 format or format specified by `momentResultFormat`). | No       | `undefined`         |
| `maxDate`          | `string`                     | The maximum selectable date/time (ISO 8601 format or format specified by `momentResultFormat`). | No       | `undefined`         |
| `momentResultFormat`| `string`                     | The Moment.js format string used for parsing `minDate` and `maxDate`.                    | No       | `undefined`         |
| `datePickerMode`   | `'date' \| 'time' \| 'datetime'` | Determines if the picker allows selecting date, time, or both.                           | No       | `'datetime'`        |
| `displayFormat`    | `string`                     | The Moment.js format string for displaying the selected value in the input field.        | No       | `'DD/MM/YYYY - HH:mm'`|
| `initialValue`     | `string`                     | The initial value for the date picker (ISO 8601 format).                                 | No       | `undefined`         |
| `timeFormat`       | `12 \| 24`                   | Specifies 12 or 24-hour time format for the time picker.                                 | No       | `12`                |
| `startOfDay`       | `boolean`                    | If true, sets the selected date's time to the start of the day (00:00:00).               | No       | `false`             |
| `endOfDay`         | `boolean`                    | If true, sets the selected date's time to the end of the day (23:59:59).                 | No       | `false`             |

## SFDatetime

A form input element that allows users to select a date, time, or both using a native modal picker. It displays the selected value in a formatted text input. This element is an alias for `SFDate` but typically configured with `datePickerMode: 'datetime'`.

### Props

| Name             | Type                      | Description                                                                                             | Required | Default                  |
| :--------------- | :------------------------ | :------------------------------------------------------------------------------------------------------ | :------- | :----------------------- |
| `label`          | `string`                  |                                                                                                         | Yes      | `'close_time'`           |
| `placeholder`    | `string`                  |                                                                                                         | Yes      | -                        |
| `datePickerMode` | `'date'\|'time'\|'datetime'` | Determines if the picker selects date, time, or both.                                           | Yes      | `'datetime'`             |
| `displayFormat`  | `string`                  | Moment.js format for displaying the selected date/time in the input.                                    | Yes      | `'DD/MM/YYYY - HH:mm'`   |
| `required`       | `boolean`                 |                                                                                                         | Yes      | `false`                  |
| `disabled`       | `boolean`                 |                                                                                                         | No       | `false`                  |
| `variant`        | `'standard'\|'outlined'\|...` | The visual style variant of the input.                                                                  | Yes      | `'standard'`             |
| `fullWidth`      | `boolean`                 |                                                                                                         | No       | `false`                  |
| `margin`         | `'none'\|'dense'\|'normal'` |                                                                                                         | Yes      | `'normal'` (assumed)     |
| `minDate`        | `string`                  | Minimum selectable date (ISO 8601 format).                                                              | No       | -                        |
| `maxDate`        | `string`                  | Maximum selectable date (ISO 8601 format).                                                              | No       | -                        |
| `time_zone_gmt`  | `string`                  | IANA time zone name (e.g., 'Asia/Saigon') for date calculations. Defaults to device timezone if omitted. | Yes      | Device Timezone          |
| `timeFormat`     | `12 \| 24`                | Use 12-hour or 24-hour format in the time picker.                                                       | No       | System Default           |
| `startOfDay`     | `boolean`                 | Set selected date's value to the start of the day (00:00:00).                                           | No       | `false`                  |
| `endOfDay`       | `boolean`                 | Set selected date's value to the end of the day (23:59:59).                                             | No       | `false`                  |
| `editable`       | `boolean`                 | If false, prevents direct text input, forcing picker use.                                               | No       | `true`                   |

*Note: `required` status is based on the TypeScript `Config` type definition. Default values are inferred from code logic where possible.*

## SFFilterButton

This form element renders a button, typically represented by an icon. When pressed, it opens a bottom sheet containing a sub-form (`ui.SubFormBuilder`) based on the main form's schema. This allows users to configure and apply filter criteria, which are then reflected in the main form's values upon submission of the sub-form.

### Props

| Name               | Type                   | Description                                                                 | Required | Default      |
| :----------------- | :--------------------- | :-------------------------------------------------------------------------- | :------- | :----------- |
| `fullWidth`        | `boolean`              |                                                                             | No       | `false`      |
| `variant`          | `keyof typeof Variant` | Specifies the visual style variant (e.g., 'standard', 'outlined').          | No       | `'standard'` |
| `margin`           | `keyof typeof SizeEnum`  |                                                                             | No       | `undefined`  |
| `required`         | `boolean`              |                                                                             | No       | `false`      |
| `paddingBottom`    | `keyof typeof SizeEnum`  |                                                                             | No       | `undefined`  |
| `label`            | `string`               |                                                                             | No       | `''`         |
| `suboptions`       | `SubOptionsShape`      | Configuration for sub-options within the filter form.                       | No       | `undefined`  |
| `initialValue`     | `OptionsItemShape[]`   | Default selected values for the filter options.                             | No       | `undefined`  |
| `disable_custom`   | `boolean`              | If `true`, disables custom value input in the filter form.                  | No       | `false`      |
| `value_type`       | `string`               | Specifies the expected data type of the filter value.                       | No       | `undefined`  |
| `multiple`         | `boolean`              | If `true`, allows multiple selections in the filter form.                   | No       | `false`      |
| `options`          | `OptionsItemShape[]`   | The list of available options to display in the filter form.                | No       | `[]`         |
| `enable_search`    | `boolean`              | If `true`, enables a search input within the filter form options.           | No       | `false`      |
| `disable_uncheck`  | `boolean`              | If `true`, prevents users from unselecting an already selected option.      | No       | `false`      |
| `choice_type`      | `string`               | Defines the selection mechanism (e.g., 'radio', 'checkbox').                | No       | `undefined`  |
| `placeholder`      | `string`               |                                                                             | No       | `''`         |
| `showWithoutOptions`| `boolean`              | If `true`, the button is shown even when there are no `config.options`.     | No       | `false`      |
| `useSectionList`   | `boolean`              | If `true`, uses a `SectionList` component to render options in the filter form. | No       | `false`      |

## SFFilterForm

Renders a button that opens a bottom sheet containing a sub-form, typically used for applying filters within a larger form. Pressing the button navigates to a dedicated screen (`FORM_BOTTOM_SHEET`) where the filter options, defined by the `options` and `suboptions` props, are presented.

### Props

| Name               | Type                  | Description                                                                 | Required   | Default     |
| :----------------- | :-------------------- | :-------------------------------------------------------------------------- | :--------- | :---------- |
| `fullWidth`        | `boolean`             |                                                                             | No         | `false`     |
| `margin`           | `normal` \| `dense` \| `none` |                                                                             | No         | `normal`    |
| `variant`          | `standard` \| `outlined` \| `filled` | The visual style variant of the control.                                  | No         | `standard`  |
| `paddingBottom`    | `normal` \| `dense` \| `none` |                                                                             | No         | `normal`    |
| `label`            | `string`              |                                                                             | No         | `undefined` |
| `suboptions`       | `SubOptionsShape`     | Configuration for the sub-form displayed in the bottom sheet.             | Yes        | `undefined` |
| `initialValue`     | `OptionsItemShape[]`  | Initial values for the filter options within the sub-form.                | No         | `undefined` |
| `disable_custom`   | `boolean`             | Disables custom options in the sub-form.                                  | No         | `false`     |
| `value_type`       | `string`              | Specifies the expected data type of the selected value(s) in the sub-form. | No         | `undefined` |
| `multiple`         | `boolean`             | Allows multiple selections in the sub-form.                               | No         | `false`     |
| `options`          | `OptionsItemShape[]`  | The list of options to display within the sub-form.                       | Yes        | `[]`        |
| `enable_search`    | `boolean`             | Enables a search input within the sub-form.                               | No         | `false`     |
| `disable_uncheck`  | `boolean`             | Prevents unselecting options once selected in the sub-form.               | No         | `false`     |
| `choice_type`      | `string`              | Specifies the type of choice input used in the sub-form (e.g., 'checkbox'). | No         | `undefined` |
| `placeholder`      | `string`              |                                                                             | No         | `undefined` |
| `showWithoutOptions`| `boolean`             | Determines if the filter button should be shown even when no options exist. | No         | `false`     |
| `useSectionList`   | `boolean`             | Uses a `SectionList` for displaying options in the sub-form if true.      | No         | `false`     |

## SFFilterPrice

The `SFFilterPrice` element provides a form input for selecting a price range (minimum and maximum). It displays the selected range and opens a bottom sheet for users to enter or modify the 'from' and 'to' price values.

### Props

| Name                 | Type                     | Description                                                          | Required | Default        |
| :------------------- | :----------------------- | :------------------------------------------------------------------- | :------- | :------------- |
| `label`              | `string`                 |                                                                      | Yes      | -              |
| `fromFieldName`      | `string`                 | The formik field name for the minimum price value.                   | No       | `'price_from'` |
| `toFieldName`        | `string`                 | The formik field name for the maximum price value.                   | No       | `'price_to'`   |
| `fromFieldLabel`     | `string`                 | Label for the minimum price input in the bottom sheet.               | No       | -              |
| `toFieldLabel`       | `string`                 | Label for the maximum price input in the bottom sheet.               | No       | -              |
| `fromFieldPlaceholder` | `string`                 | Placeholder text for the minimum price input in the bottom sheet.    | No       | -              |
| `toFieldPlaceholder` | `string`                 | Placeholder text for the maximum price input in the bottom sheet.    | No       | -              |
| `variant`            | `string`                 | Specifies the visual style ('standard', 'standard-outlined', etc.).  | No       | `'standard'`   |
| `fullWidth`          | `boolean`                |                                                                      | No       | `false`        |
| `margin`             | `string`                 |                                                                      | No       | -              |
| `paddingBottom`      | `string`                 |                                                                      | No       | -              |
| `required`           | `boolean`                |                                                                      | No       | `false`        |
| `enable_search`      | `boolean`                | Configuration passed to the bottom sheet component (FilterPriceField). | No       | `false`        |
| `findReplace`        | `any`                    | Configuration passed to the bottom sheet component (FilterPriceField). | No       | -              |

## SFScrollView

A form element that renders its child elements within a horizontal ScrollView. It allows users to scroll horizontally through a set of form inputs or components.

### Props

| Name          | Type                                | Description                                                                          | Required | Default         |
| ------------- | ----------------------------------- | ------------------------------------------------------------------------------------ | -------- | --------------- |
| `elements`      | `Record<string, ElementConfig>` | Defines the child form elements to render within the scroll view.                  | Yes      | N/A             |
| `paddingBottom` | `string`                            |                                                                             | No       | `paddingBase` |

## SFSearchBox

The `SFSearchBox` component renders a search input field integrated directly into the screen's header navigation bar. It automatically handles focus, clearing, and debounced value updates for form submission.

### Props

The component accepts standard `FormFieldProps` (`name`, `config`, `disabled`, `formik`). The primary configuration is done via the `config` object:

| Name             | Type                                                          | Description                                       | Required | Default         |
| :--------------- | :------------------------------------------------------------ | :------------------------------------------------ | :------- | :-------------- |
| `placeholder`    | `string`                                                      |                                                   | No       | `undefined`     |
| `clearButtonMode`| `'never' \| 'while-editing' \| 'unless-editing' \| 'always'`  | How the clear button behaves (iOS only).          | No       | `undefined`     |
| `editable`       | `boolean`                                                     | If the input is editable.                         | No       | `true`          |
| `required`       | `boolean`                                                     |                                                   | No       | `false`         |
| `variant`        | `keyof typeof Variant`                                        | Visual style variant.                             | No       | `undefined`     |
| `multipleline`   | `boolean`                                                     | If the input allows multiple lines.               | No       | `false`         |
| `showSearchIcon` | `boolean`                                                     | Whether to show the search icon.                  | No       | `true`          |
| `fullWidth`      | `boolean`                                                     |                                                   | No       | `false`         |
| `margin`         | `keyof typeof SizeEnum`                                       |                                                   | No       | `undefined`     |
| `paddingBottom`  | `keyof typeof SizeEnum`                                       |                                                   | No       | `undefined`     |
| `minHeight`      | `number`                                                      |                                                   | No       | `undefined`     |
| `maxLength`      | `number`                                                      |                                                   | No       | `undefined`     |
| `autoCorrect`    | `boolean`                                                     | Enable/disable auto-correction.                   | No       | `false`         |
| `autoCapitalize` | `'none' \| 'sentences' \| 'words' \| 'characters'`            | Auto-capitalization behavior.                     | No       | `'none'`        |
| `autoFocus`      | `boolean`                                                     |                                                   | No       | `true` if empty |
| `description`    | `string`                                                      |                                                      | No       | `undefined`     |

## SFSelect

The `SFSelect` element provides a dropdown-like selection interface, typically opening a bottom sheet for users to choose one or multiple options from a list. It supports features like search, sections, and conditional options based on other fields.

### Props

| Name                 | Type                               | Description                                                                 | Required | Default     |
| :------------------- | :--------------------------------- | :-------------------------------------------------------------------------- | :------- | :---------- |
| `label`              | `string`                           |                                                                             | Yes      | `undefined` |
| `options`            | `OptionsItemShape[]`               | The list of selectable options.                                             | Yes      | `[]`        |
| `fullWidth`          | `boolean`                          |                                                                             | No       | `false`     |
| `margin`             | `'dense' \| 'normal' \| 'none'`    |                                                                             | No       | `'normal'`  |
| `required`           | `boolean`                          |                                                                             | No       | `false`     |
| `variant`            | `'standard' \| 'outlined' \| etc.` | Visual style variant.                                                       | No       | `'standard'`|
| `paddingBottom`      | `'dense' \| 'normal' \| 'none'`    |                                                                             | No       | `'normal'`  |
| `suboptions`         | `SubOptionsShape`                  | Additional options grouped under main options.                              | No       | `undefined` |
| `initialValue`       | `OptionsItemShape[]`               | Initial selected value(s).                                                  | No       | `undefined` |
| `disable_custom`     | `boolean`                          | Disables custom privacy options if applicable.                              | No       | `false`     |
| `value_type`         | `string`                           | Specifies the type of value expected (e.g., 'string', 'number').            | No       | `undefined` |
| `multiple`           | `boolean`                          | Allows multiple selections if true.                                         | No       | `false`     |
| `enable_search`      | `boolean`                          | Enables searching within the options list in the bottom sheet.              | No       | `false`     |
| `disableClearable`   | `boolean`                          | Prevents clearing/unselecting the chosen option(s).                         | No       | `false`     |
| `choice_type`        | `string`                           | Type of choice mechanism (used internally, e.g., 'radio', 'checkbox').      | No       | `undefined` |
| `placeholder`        | `string`                           |                                                                             | No       | `undefined` |
| `showWithoutOptions` | `boolean`                          | Renders the component even if no `options` are provided.                    | No       | `false`     |
| `useSectionList`     | `boolean`                          | Uses a SectionList for displaying options in the bottom sheet if true.      | No       | `false`     |
| `autoSubmit`         | `boolean`                          | Submits the form automatically on value change.                             | No       | `false`     |
| `relatedFieldName`   | `string`                           | Name of a related form field for conditional logic (e.g., filtering options). | No       | `undefined` |
| `optionRelatedMapping`| `Record<string, OptionsItemShape[]>`| Mapping object for options based on the `relatedFieldName`'s value.         | No       | `undefined` |
| `resetValue`         | `boolean`                          | Resets the value under certain conditions (used internally).                | No       | `false`     |

## SFSwitch

A form element that renders a switch (toggle) control. It allows users to select between two states, typically representing on/off or true/false.

### Props

| Name           | Type                               | Description                                                                 | Required | Default           |
| -------------- | ---------------------------------- | --------------------------------------------------------------------------- | -------- | ----------------- |
| `label`          | string                             |                                                                             | Yes      |                   |
| `fullWidth`      | boolean                            |                                                                             | No       | `false`           |
| `margin`         | 'dense' \| 'normal' \| 'none'      |                                                                             | No       | `normal`          |
| `required`       | boolean                            |                                                                             | No       | `false`           |
| `variant`        | 'standard' \| 'outlined' \| 'filled' \| 'standard-inlined' | The visual style of the form control. (Note: Hardcoded to 'standard-inlined' in the component implementation) | No       | `'standard-inlined'` |
| `paddingBottom`  | 'dense' \| 'normal' \| 'none'      |                                                                             | No       | `normal`          |
| `checkedValue`   | boolean \| number                  | The value assigned to the field when the switch is checked (on).            | No       | `1`               |
| `uncheckedValue` | boolean \| number                  | The value assigned to the field when the switch is unchecked (off).         | No       | `0`               |
| `description`    | string                             |                                                                             | No       | `''`              |

## SFTabSelect

A form element that renders a horizontal list of tabs, allowing the user to select one option. The selected value is stored in the form state.

### Props

Props are passed via the `config` object within the form definition.

| Name      | Type                                                               | Description                                                                                                                               | Required | Default   |
| :-------- | :----------------------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------- | :------- | :-------- |
| `options` | `Array<{ label: string, value: any, showWhen?: Record<string, any> }>` | An array of objects defining the tabs. Each object should have a `label` (display text) and a `value`. Can include `showWhen` conditions. | Yes      | `[]`      |
| `bounces` | `boolean`                                                          | Determines if the horizontal tab list bounces when scrolled to the end.                                                                   | No       | `false`   |

## SFText

The `SFText` element renders a standard text input field within a form. It supports various configurations like multiline input, validation, QR code scanning, and copy-to-clipboard functionality.

### Props

| Name                 | Type                                                     | Description                                                                 | Required | Default         |
| -------------------- | -------------------------------------------------------- | --------------------------------------------------------------------------- | -------- | --------------- |
| `label`              | `string`                                                 |                                                                             | No       | `undefined`     |
| `placeholder`        | `string`                                                 |                                                                             | No       | `undefined`     |
| `description`        | `string`                                                 |                                                                             | No       | `undefined`     |
| `contextualDescription` | `string`                                              | Additional description text.                                                | No       | `undefined`     |
| `variant`            | `'standard'`, `'outlined'`, `'filled'`, `'standard-outlined'`, `'livestream'` | Visual style of the input.                                                  | No       | `'standard'`    |
| `fullWidth`          | `boolean`                                                |                                                                             | No       | `false`         |
| `margin`             | `'none'`, `'dense'`, `'normal'`                          |                                                                             | No       | `'normal'`      |
| `paddingBottom`      | `'none'`, `'dense'`, `'normal'`                          |                                                                             | No       | `'normal'`      |
| `required`           | `boolean`                                                |                                                                             | No       | `false`         |
| `disabled`           | `boolean`                                                |                                                                             | No       | `false`         |
| `editable`           | `boolean`                                                | If `false`, the text is not editable.                                       | No       | `true`          |
| `multiline`          | `boolean`                                                | Allows multiple lines of text input.                                        | No       | `false`         |
| `minHeight`          | `number`                                                 |                                                                             | No       | `undefined`     |
| `maxLength`          | `number`                                                 |                                                                             | No       | `undefined`     |
| `autoCorrect`        | `boolean`                                                | Enables auto-correction.                                                    | No       | `true`          |
| `autoCapitalize`     | `'none'`, `'sentences'`, `'words'`, `'characters'`       | Controls automatic capitalization.                                          | No       | `'sentences'`   |
| `autoFocus`          | `boolean`                                                |                                                                             | No       | `false`         |
| `clearButtonMode`    | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Controls the visibility of the clear button (iOS only).                     | No       | `'never'`       |
| `validateAction`     | `string`                                                 | Action name for backend validation on blur.                                 | No       | `undefined`     |
| `findReplace`        | `{ find: string, replace: string }`                      | Defines find/replace rules for generating a slug displayed below the input. | No       | `undefined`     |
| `hasQRScanner`       | `boolean`                                                | Adds a QR code scanner icon/button.                                         | No       | `false`         |
| `qrScannerParamName` | `string`                                                 | Query parameter name to extract from the scanned QR code URL.               | No       | `'invite_code'` |
| `hasCopy`            | `boolean`                                                | Adds a copy-to-clipboard icon/button.                                       | No       | `false`         |
| `backgroundColor`    | `string`                                                 | Sets the background color of the input.                                     | No       | `undefined`     |
| `order`              | `number`                                                 | Order of the element in the form.                                           | No       | `undefined`     |

## SimpleFriendPicker

A form element that allows users to select one or multiple friends from a searchable list. It displays selected friends as chips and provides an interface to browse and search all available friends fetched via API.

### Props

| Name             | Type                                  | Description                                       | Required | Default                          |
| :--------------- | :------------------------------------ | :------------------------------------------------ | :------- | :------------------------------- |
| `fullWidth`      | `boolean`                             |                                                   | No       | `false`                          |
| `margin`         | `'none' \| 'dense' \| 'normal'`       |                                                   | No       | `'normal'`                       |
| `required`       | `boolean`                             |                                                   | No       | `false`                          |
| `variant`        | `'standard' \| 'outlined' \| 'filled'` | The visual style variant of the input field.      | No       | `'standard'`                     |
| `paddingBottom`  | `'none' \| 'dense' \| 'normal'`       |                                                   | No       | `undefined`                      |
| `label`          | `string`                              |                                                   | No       | `''`                             |
| `initialValue`   | `OptionsItemShape[]`                  | An array of initially selected friend objects.    | No       | `[]`                             |
| `multiple`       | `boolean`                             | If `true`, allows selecting multiple friends.     | No       | `false`                          |
| `placeholder`    | `string`                              |                                                   | No       | `'Search friends by their name'` |
| `onFocus`        | `(event: any) => void`                | Callback function triggered when the input focuses. | No       | `undefined`                      |

## SingleUpdateInputField

A form element that currently renders a 'Coming Soon' placeholder. It is intended for scenarios requiring a single update input field, but the specific functionality is not yet implemented.

### Props

| Name       | Type                               | Description                                                                 | Required | Default |
| :--------- | :--------------------------------- | :-------------------------------------------------------------------------- | :------- | :------ |
| `name`     | `string`                           | The unique identifier for the form field within the form.                   | Yes      |         |
| `config`   | `object`                           | An object containing configuration properties specific to the form element. | Yes      | `{}`    |
| `disabled` | `boolean`                          |                                                                             | No       | `false` |
| `formik`   | `FormikContextType<any>`           | The Formik context object, providing access to form state and helpers.      | Yes      |         |

## SingleVideoFile

This form element allows users to select a single video, either by uploading a file directly or by providing a URL (depending on the `file_type` configuration). It displays a preview of the selected video and handles file size validation.

### Props

| Name                  | Type                                          | Description                                                                                                | Required | Default        |
| :-------------------- | :-------------------------------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :------------- |
| `label`               | `string`                                      |                                                                                                            | No       | -              |
| `required`            | `boolean`                                     |                                                                                                            | No       | `false`        |
| `fullWidth`           | `boolean`                                     |                                                                                                            | No       | `false`        |
| `margin`              | `'normal' \| 'dense' \| 'none'`               |                                                                                                            | No       | `'normal'`     |
| `paddingBottom`       | `'normal' \| 'dense' \| 'none'`               |                                                                                                            | No       | `'normal'`     |
| `variant`             | `'standard' \| 'outlined' \| 'filled'`        | The visual style variant of the form control.                                                              | No       | `'standard'`   |
| `item_type`           | `string`                                      | Specifies the type of item being uploaded (e.g., 'video').                                                 | Yes      | -              |
| `upload_url`          | `string`                                      | The endpoint URL for uploading the file.                                                                   | Yes      | -              |
| `max_upload_filesize` | `number \| { video: number, photo: number }` | Maximum allowed file size in bytes. Can be an object with different limits for video/photo.                | Yes      | -              |
| `file_type`           | `'video' \| 'link'`                           | Specifies whether to handle a direct video upload ('video') or a video URL ('link').                       | Yes      | -              |
| `allow_upload`        | `boolean`                                     | Controls if direct video upload is allowed (used when `file_type` is not 'link').                          | No       | `true` (implied) |
| `storage_id`          | `number \| null`                              | Optional ID for a specific storage service.                                                                | No       | `null`         |
| `fetchEndpoint`       | `string`                                      | Optional endpoint for fetching video details when `file_type` is 'link'.                                   | No       | -              |
| `extraProps`          | `object`                                      | Additional props, often containing context like `module_name` and `resource_name` for validation URLs. | No       | `{}`           |

## Slider

A form element that allows users to select a value from a specified range by sliding a handle along a track.

### Props

| Name           | Type                               | Description                                                               | Required | Default           |
| :------------- | :--------------------------------- | :------------------------------------------------------------------------ | :------- | :---------------- |
| `label`        | `string`                           |                                                                           | Yes      |                   |
| `fullWidth`    | `boolean`                          |                                                                           | No       | `false`           |
| `margin`       | `'none' \| 'dense' \| 'normal'`    |                                                                           | No       | `'normal'`        |
| `required`     | `boolean`                          |                                                                           | No       | `false`           |
| `paddingBottom`| `'none' \| 'dense' \| 'normal'`    |                                                                           | No       | `undefined`       |
| `minimumValue` | `number`                           | The minimum value of the slider.                                          | No       | `undefined`       |
| `maximumValue` | `number`                           | The maximum value of the slider.                                          | No       | `undefined`       |
| `step`         | `number`                           | The granularity with which the slider can step through values.            | No       | `undefined`       |
| `variant`      | `keyof typeof Variant`             | The visual style variant of the form control. (Currently fixed internally) | No       | `'standard-inlined'` |
| `inline`       | `boolean`                          | (Part of Config type, but not directly used in this component's logic)    | No       | `false`           |
| `meta`         | `MetaShape`                        | Additional metadata for the field.                                        | No       | `undefined`       |

## SocialButtons

This element renders a container for multiple social login buttons. It dynamically adjusts the layout based on the number of buttons: displaying them in a row if there are more than two, and stacked vertically otherwise. It also handles platform-specific visibility, hiding the Apple login button on Android devices.

### Props

| Name        | Type                     | Description                                                                 | Required | Default |
| :---------- | :----------------------- | :-------------------------------------------------------------------------- | :------- | :------ |
| `elements`  | `Record<string, any>`    | Configuration objects for each individual social button element.            | Yes      |         |
| `totalButton`| `number`                 | The total count of configured social buttons, used to determine layout. | Yes      |         |

## SpamQuestion

This element renders a text input field, often accompanied by an image, designed to present a question to the user to prevent spam submissions. It integrates with Formik for state management.

### Props

| Name                 | Type                                                              | Description                                                                 | Required | Default            |
| :------------------- | :---------------------------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------------- |
| `label`              | `string`                                                          |                                                                             | No       |                    |
| `placeholder`        | `string`                                                          |                                                                             | No       |                    |
| `required`           | `boolean`                                                         |                                                                             | No       | `false`            |
| `disabled`           | `boolean`                                                         |                                                                             | No       | `false`            |
| `fullWidth`          | `boolean`                                                         |                                                                             | No       | `false`            |
| `margin`             | `'none' \| 'dense' \| 'normal'`                                   |                                                                             | No       | `undefined`        |
| `variant`            | `'standard' \| 'outlined' \| 'filled' \| 'standard-inlined'`      | Defines the visual style of the input field.                                | No       | `'standard-inlined'` |
| `imageUri`           | `string`                                                          | The URI for the image associated with the spam question.                    | Yes      |                    |
| `editable`           | `boolean`                                                         | Determines if the text input field can be edited by the user.               | No       | `true`             |
| `clearButtonMode`    | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | Controls when the clear text button appears in the input field (iOS only). | No       | `undefined`        |
| `paddingBottom`      | `'none' \| 'dense' \| 'normal'`                                   |                                                                             | No       | `undefined`        |

## SponsorCalculatorCost

This form element provides a numeric input field that calculates and displays a total cost based on the entered value, an initial unit count, and a price per unit. It's typically used for scenarios like calculating sponsorship costs based on impressions or days.

### Props

| Name                  | Type                                                          | Description                                                                 | Required | Default        |
| :-------------------- | :------------------------------------------------------------ | :-------------------------------------------------------------------------- | :------- | :------------- |
| `label`               | `string`                                                      |                                                                             | No       |                |
| `description`         | `string`                                                      |                                                                             | No       |                |
| `placeholder`         | `string`                                                      |                                                                             | No       |                |
| `required`            | `boolean`                                                     |                                                                             | No       | `false`        |
| `disabled`            | `boolean`                                                     |                                                                             | No       | `false`        |
| `variant`             | `'standard' \| 'outlined' \| 'filled' \| 'livestream' \| 'standard-outlined'` | The visual style variant of the input field.                              | No       | `'standard'`   |
| `margin`              | `'none' \| 'dense' \| 'normal'`                               |                                                                             | No       | `'normal'`     |
| `fullWidth`           | `boolean`                                                     |                                                                             | No       | `false`        |
| `maxLength`           | `number`                                                      |                                                                             | No       |                |
| `initialUnit`         | `number`                                                      | The base unit used for the cost calculation (e.g., number of impressions).  | Yes      |                |
| `initialPrice`        | `number`                                                      | The price per `initialUnit`.                                                | Yes      |                |
| `pricePattern`        | `object`                                                      | An object defining the currency format (`symbol`, `currency_code`, etc.). | Yes      |                |
| `totalNameLabel`      | `string`                                                      | The translation key for the label prefix before the calculated total cost.  | No       | `'total_cost'` |

## StepButton

A button element designed for multi-step forms, allowing navigation between steps (previous/next) or form submission. It interacts with a form field (specified by `currentStepName` or defaulting to `_current_step`) to manage the active step.

### Props

| Name                 | Type                             | Description                                                                                   | Required | Default                     |
| :------------------- | :------------------------------- | :-------------------------------------------------------------------------------------------- | :------- | :-------------------------- |
| `label`              | `string`                         |                                                                                               | Yes      | `''`                        |
| `actionType`         | `'previous' \| 'next' \| 'submit'` | Determines the button's behavior (navigate previous, next, or submit).                        | Yes      | `undefined`                 |
| `fullWidth`          | `boolean`                        |                                                                                               | No       | `false`                     |
| `margin`             | `'small' \| 'medium' \| 'large' \| 'none'` |                                                                                               | No       | `undefined`                 |
| `variant`            | `'standard' \| 'outlined' \| 'filled'` | The visual style variant of the surrounding form control.                                     | No       | `'standard'`                |
| `paddingBottom`      | `'small' \| 'medium' \| 'large' \| 'none'` |                                                                                               | No       | `undefined`                 |
| `currentStepName`    | `string`                         | The name of the form field tracking the current step index.                                   | No       | `FormStepVariable.CURRENT_KEY` |
| `style`              | `ViewStyle`                      | Custom styling applied to the surrounding form control.                                       | No       | `undefined`                 |

## Submit

A button element used to trigger form submission. It integrates with Formik to handle the submit action and can be configured with various visual styles and behaviors.

### Props

| Name                 | Type                                                              | Description                                                                                   | Required | Default      |
| :------------------- | :---------------------------------------------------------------- | :-------------------------------------------------------------------------------------------- | :------- | :----------- |
| `label`              | `string`                                                          |                                                                                               | Yes      |              |
| `icon`               | `string`                                                          | Name of the icon to display on the button.                                                    | No       |              |
| `fullWidth`          | `boolean`                                                         |                                                                                               | No       | `false`      |
| `margin`             | `'none' \| 'dense' \| 'normal'`                                   |                                                                                               | No       | `'normal'`   |
| `paddingBottom`      | `'none' \| 'dense' \| 'normal'`                                   |                                                                                               | No       | `'normal'`   |
| `variant`            | `'standard' \| 'outlined' \| 'contained'`                         | The visual style variant of the button's container.                                           | No       | `'standard'` |
| `color`              | `'primary' \| 'secondary' \| 'error' \| 'warning' \| 'info' \| 'success' \| 'inherit' \| string` | The color of the button. Defaults to 'gray' when disabled.                                | No       | `'primary'`  |
| `size`               | `'small' \| 'medium' \| 'large' \| 'string'`                      | The size of the button. Note: The component internally uses 'normal'.                         | No       | `'medium'`   |
| `fontWeight`         | `'light' \| 'regular' \| 'medium' \| 'bold'`                      | The font weight of the button text.                                                           | No       |              |
| `textTransform`      | `'none' \| 'capitalize' \| 'uppercase' \| 'lowercase'`            | Controls the text transformation (e.g., uppercase).                                           | No       |              |
| `round`              | `boolean`                                                         | If true, makes the button round (intended for icon buttons).                                  | No       | `false`      |
| `first`              | `boolean`                                                         | Style adjustment if it's the first element in a group.                                        | No       | `false`      |
| `disabled`           | `boolean`                                                         |                                                                                               | No       | `false`      |
| `testID`             | `string`                                                          | Test identifier for automation.                                                               | No       |              |
| `transparent`        | `boolean`                                                         | Makes the button background transparent.                                                      | No       | `false`      |
| `outline`            | `boolean`                                                         | Applies an outline style to the button.                                                       | No       | `false`      |
| `disableWhenClean`   | `boolean`                                                         | If true, the button is disabled when the form is pristine (no changes made).                  | No       | `false`      |
| `style`              | `object`                                                          | Custom styles to apply to the FormControl container.                                          | No       |              |
| `customAction`       | `{ type: string; payload?: any }`                                 | Dispatches a custom Redux action when the button is clicked after submitting the form.        | No       |              |

## SubmitHeader

This element renders a submit button, typically placed within a form's header area, wrapped in a `FormControl` for layout control. Clicking the button triggers the form submission process.

### Props

| Name          | Type                               | Description                                  | Required | Default    |
| :------------ | :--------------------------------- | :------------------------------------------- | :------- | :--------- |
| `label`       | `string`                           |                                              | Yes      |            |
| `icon`        | `string`                           | Icon name to display on the button.          | No       |            |
| `color`       | `string`                           | Button color (e.g., 'primary', 'secondary'). | No       |            |
| `size`        | `'small' \| 'medium' \| 'large'`   | Button size.                                 | No       |            |
| `fontWeight`  | `string`                           | Button text font weight.                     | No       |            |
| `textTransform` | `string`                           | Button text transformation (e.g., 'uppercase'). | No       |            |
| `transparent` | `boolean`                          | Makes the button background transparent.     | No       | `false`    |
| `outline`     | `boolean`                          | Applies an outline style to the button.      | No       | `false`    |
| `fullWidth`   | `boolean`                          |                                                  | No       | `false`    |
| `margin`      | `'none' \| 'dense' \| 'normal'`    |                                              | No       |            |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'`    |                                              | No       | `'normal'` |
| `variant`     | `'standard' \| 'outlined' \| 'filled'` | Variant style for the surrounding control.   | No       | `'standard'`|

## Switch

A form element that renders a toggle switch input, allowing users to select between two states (on/off).

### Props

| Name                | Type                         | Description                                       | Required | Default     |
| ------------------- | ---------------------------- | ------------------------------------------------- | -------- | ----------- |
| `label`             | `string`                     |                                                   | Yes      | `undefined` |
| `description`       | `string`                     |                                                   | No       | `''`        |
| `disabled`          | `boolean`                    |                                                   | No       | `false`     |
| `required`          | `boolean`                    |                                                   | No       | `false`     |
| `fullWidth`         | `boolean`                    |                                                   | No       | `false`     |
| `margin`            | `'none'\|'normal'\|'dense'` |                                                   | No       | `'normal'`  |
| `checkedValue`      | `any`                        | The value submitted when the switch is turned on. | No       | `1`         |
| `uncheckedValue`    | `any`                        | The value submitted when the switch is turned off.| No       | `0`         |

## Tags

A form element that allows users to input and manage a list of tags. Users can type tags and press Enter/Done to add them. Existing tags can be removed by clicking the close icon on the tag.

### Props

| Name             | Type                                                     | Description                                                                 | Required | Default      |
| :--------------- | :------------------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------- |
| `label`          | `string`                                                 |                                                                             | No       |              |
| `description`    | `string`                                                 |                                                                             | No       |              |
| `placeholder`    | `string`                                                 |                                                                             | No       | `'enter text'` |
| `variant`        | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined'` | The visual style variant of the input.                                      | No       | `'standard'` |
| `fullWidth`      | `boolean`                                                |                                                                             | No       | `false`      |
| `margin`         | `'normal' \| 'dense' \| 'none'`                          |                                                                             | No       |              |
| `required`       | `boolean`                                                |                                                                             | No       | `false`      |
| `paddingBottom`  | `'normal' \| 'dense' \| 'none'`                          |                                                                             | No       | `'normal'`   |
| `clearButtonMode`| `string`                                                 | Determines the visibility of the clear button (standard TextInput prop).    | No       |              |
| `editable`       | `boolean`                                                | If false, the input cannot be edited (standard TextInput prop).             | No       | `true`       |

## Text

A standard text input field for forms, allowing users to enter single or multiple lines of text.

### Props

| Name                  | Type                                                              | Description                                                                 | Required | Default         |
| :-------------------- | :---------------------------------------------------------------- | :-------------------------------------------------------------------------- | :------- | :-------------- |
| `label`        | `string`                                                          |                                                                             | No       |                 |
| `placeholder`  | `string`                                                          |                                                                             | No       |                 |
| `description`  | `string`                                                          |                                                                             | No       |                 |
| `variant`      | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined' \| 'livestream'` | The visual style variant of the input field.                              | No       | `'standard'`    |
| `fullWidth`    | `boolean`                                                         |                                                                             | No       | `false`         |
| `margin`       | `'none' \| 'normal' \| 'dense'`                                     |                                                                             | No       | `'normal'`      |
| `multiline`    | `boolean`                                                         | If `true`, allows multiple lines of text input (textarea).                  | No       | `false`         |
| `minHeight`    | `number`                                                          |                                                                             | No       |                 |
| `maxLength`    | `number`                                                          |                                                                             | No       |                 |
| `autoFocus`    | `boolean`                                                         |                                                                             | No       | `false`         |
| `autoCorrect`  | `boolean`                                                         | Enables or disables auto-correction for the input.                          | No       | `true`          |
| `autoCapitalize`| `'none' \| 'sentences' \| 'words' \| 'characters'`                | Controls automatic capitalization behavior.                                 | No       | `'sentences'`   |
| `editable`     | `boolean`                                                         | If `false`, the text input is not editable.                                 | No       | `true`          |
| `required`     | `boolean`                                                         |                                                                             | No       | `false`         |
| `clearButtonMode`| `'never' \| 'while-editing' \| 'unless-editing' \| 'always'`      | (iOS only) When to display the clear text button.                           | No       | `'never'`       |
| `validateAction`| `string`                                                          | Name of a registered action for backend validation triggered on blur.       | No       |                 |
| `findReplace`  | `{ find: string, replace: string }`                               | Configuration to automatically generate a slug-like value based on input. | No       |                 |
| `contextualDescription` | `string`                                               | Additional descriptive text displayed near the input.                       | No       |                 |
| `hasQRScanner` | `boolean`                                                         | If `true`, displays a QR code scanner icon button.                          | No       | `false`         |
| `qrScannerParamName` | `string`                                                  | Query parameter name to extract from the scanned QR code URL.               | No       | `'invite_code'` |
| `hasCopy`      | `boolean`                                                         | If `true`, displays a copy-to-clipboard icon button.                        | No       | `false`         |
| `backgroundColor`| `string`                                                          | Sets the background color for the input wrapper.                            | No       |                 |

## Textarea

Provides a multi-line text input field for forms.

### Props

| Name                  | Type                                               | Description                                                                                                | Required | Default          |
| :-------------------- | :------------------------------------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :--------------- |
| `name`                | `string`                                           | The name of the field used in the form state.                                                              | Yes      |                  |
| `label`               | `string`                                           |                                                                                                            | No       |                  |
| `placeholder`         | `string`                                           |                                                                                                            | No       |                  |
| `description`         | `string`                                           |                                                                                                            | No       |                  |
| `required`            | `boolean`                                          |                                                                                                            | No       | `false`          |
| `disabled`            | `boolean`                                          |                                                                                                            | No       | `false`          |
| `fullWidth`           | `boolean`                                          |                                                                                                            | No       | `false`          |
| `margin`              | `'none' \| 'normal' \| 'dense'`                    |                                                                                                            | No       | `'normal'`       |
| `variant`             | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined'` | The visual style variant of the input field.                                                               | No       | `'standard'`     |
| `minHeight`           | `number`                                           |                                                                                                            | No       |                  |
| `maxLength`           | `number`                                           |                                                                                                            | No       |                  |
| `autoFocus`           | `boolean`                                          |                                                                                                            | No       | `false`          |
| `autoCorrect`         | `boolean`                                          | Enables or disables autocorrection for the input.                                                          | No       | Platform default |
| `autoCapitalize`      | `'none' \| 'sentences' \| 'words' \| 'characters'` | Controls the automatic capitalization behavior of the text input.                                          | No       | `'none'`         |
| `editable`            | `boolean`                                          | If false, the text content cannot be modified by the user.                                                 | No       | `true`           |
| `clearButtonMode`     | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | (iOS only) Determines when the standard clear text button appears inside the text input.                 | No       | `'never'`        |
| `findReplace`         | `{ find: string, replace: string }`                | Defines patterns for find-and-replace operations on the input value, often used for generating derived text. | No       |                  |
| `contextualDescription`| `string`                                           | Additional description text that might be combined with dynamic content based on the input value.          | No       |                  |

## Time

A form element that allows users to select a specific time using a native time picker interface. This element is an alias for the `Date` element, configured specifically for time selection.

### Props

| Name             | Type                                       | Description                                                                 | Required | Default                  |
|------------------|--------------------------------------------|-----------------------------------------------------------------------------|----------|--------------------------|
| `label`          | `string`                                   |                                                                             | Yes      | -                        |
| `description`    | `string`                                   |                                                                             | No       | `undefined`              |
| `placeholder`    | `string`                                   |                                                                             | No       | `undefined`              |
| `displayFormat`  | `string`                                   | The format used to display the selected time (e.g., 'HH:mm', 'h:mm A').     | No       | `'HH:mm'` (Recommended)  |
| `resultFormat`   | `string`                                   | The format the selected time is stored in. Defaults to ISO 8601 format if unset. | No       | ISO 8601 String        |
| `timeFormat`     | `12 \| 24`                               | Specifies whether to use 12-hour or 24-hour format in the picker.         | No       | Locale default           |
| `initialValue`   | `string`                                   | An initial time value for the field (must match resultFormat if specified, otherwise ISO 8601). | No       | `undefined`              |
| `disabled`       | `boolean`                                  |                                                                             | No       | `false`                  |
| `required`       | `boolean`                                  |                                                                             | No       | `false`                  |
| `fullWidth`      | `boolean`                                  |                                                                             | No       | `false`                  |
| `margin`         | `'none' \| 'dense' \| 'normal'`            |                                                                             | No       | `'normal'`               |
| `variant`        | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined'` | The visual style variant of the input.                                      | No       | `'standard'`             |
| `time_zone_gmt`  | `string`                                   | Timezone identifier (e.g., 'UTC', 'America/New_York') for display formatting. | No       | User's current timezone |

**Note:** This element utilizes the `DatePickerField` component internally with its `datePickerMode` prop implicitly set to `'time'`. Props like `minDate`, `maxDate`, `startOfDay`, and `endOfDay` from `DatePickerField` are technically available but may have limited relevance or unexpected behavior in a time-only context.

## Typo

Renders styled text content within a form, suitable for labels, descriptions, or simple HTML snippets.

### Props

| Name            | Type     | Description                                                              | Required | Default     |
| --------------- | -------- | ------------------------------------------------------------------------ | -------- | ----------- |
| `label`         | `string` |                                                                          | No       | `undefined` |
| `numberOfLines` | `number` | Maximum number of lines for the label and description.                   | No       | `undefined` |
| `plainText`     | `string` | HTML content to render. Takes precedence over label/description if provided. | No       | `undefined` |
| `description`   | `string` |                                                                          | No       | `undefined` |
| `style`         | `object` | Custom style object for the label.                                       | No       | `undefined` |

## VideoUrl

This form element is intended for inputting video URLs. Currently, it is a placeholder component displaying a "Coming Soon" message and does not have specific configurable props beyond the standard `FormFieldProps`.

### Props

This component currently does not define specific props beyond the standard `FormFieldProps`.
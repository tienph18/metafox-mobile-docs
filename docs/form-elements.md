## AdvertiseCalculatorCost

The `AdvertiseCalculatorCost` element is a specialized text input field designed for calculating advertising costs based on a selected placement and a numeric input value (e.g., number of impressions, clicks). It displays the calculated total cost dynamically based on the input and the price associated with the selected placement option.

For a visual reference, see [AdvertiseCalculatorCost Gallery](./form-elements/AdvertiseCalculatorCost.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none'`, `'sentences'`, `'words'`, `'characters'` | Controls automatic capitalization. | | `'sentences'` |
| `autoCorrect` | `boolean` | | | `true` |
| `autoFocus` | `boolean` | | | `false` |
| `clearButtonMode` | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | When to show the clear button (iOS only). | | `'never'` |
| `disabled` | `boolean` | | | `false` |
| `editable` | `boolean` | Whether the input is editable. | | `true` |
| `fullWidth` | `boolean` | | | `false` |
| `initialUnit` | `number` | The base unit for the cost calculation (e.g., cost per 1000 impressions means `initialUnit` is 1000). | Yes | |
| `label` | `string` | | | |
| `margin` | `'none'`, `'dense'`, `'normal'`, `'small'` | | | `'normal'` |
| `maxLength` | `number` | | | |
| `minHeight` | `number` | | | |
| `multipleline` | `boolean` | Allows multiple lines of text input. | | `false` |
| `paddingBottom` | `'none'`, `'dense'`, `'normal'`, `'small'` | | | `'normal'` |
| `placeholder` | `string` | | | |
| `placementOptions` | `object` | An object mapping placement keys to their details, including the price per unit (e.g., `{ placement1: { price: 10 }, ... }`). | Yes | |
| `pricePattern` | `object` | An object defining the currency formatting (e.g., `{ thousand_separator: ',', decimal_separator: '.', precision: 2, symbol: '$', ... }`). | Yes | |
| `relatedInitialPrice` | `string` | The name of the form field holding the selected placement/option key. | Yes | |
| `required` | `boolean` | | | `false` |
| `totalNameLabel` | `string` | The translation key for the "Total Cost" label prefix. | | `total_cost` |
| `variant` | `'standard'`, `'outlined'`, `'standard-outlined'` | Specifies the visual style of the component. | | `'standard'` |

## Alert

Displays a styled alert box containing an HTML message. The appearance (color, icon) depends on the `severity` and `variant`.

For a visual reference, see [Alert Gallery](./form-elements/Alert.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `message` | `string` | The HTML content to display in the alert. | Yes | |
| `severity` | `'success' \| 'info' \| 'warning' \| 'error'` | Determines the alert type (info, success, warning, error), affecting color and icon. | | `'info'` |
| `variant` | `'standard'` | Specifies the visual style of the component. | | `'standard'` |

## Attachment

The Attachment element allows users to upload one or more files (photos, videos, or other types) within a form. It provides options for selecting files from the device library or capturing directly from the camera.

For a visual reference, see [Attachment Gallery](./form-elements/Attachment.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `cropping` | `boolean` | Enables image cropping after selection (currently applies to photos only). | | `false` |
| `current_files` | `FileItemShape[]` | An array of pre-existing files (used when editing). | | `[]` |
| `description` | `string` | | | |
| `disabled` | `boolean` | | | `false` |
| `file_type` | `'photo' \| 'video' \| 'file'` | Specifies the type of file allowed ('photo', 'video', or generic 'file'). | | `'photo'` |
| `fullWidth` | `boolean` | | | `false` |
| `include_exif` | `boolean` | If `true`, includes EXIF data with uploaded images. | | `false` |
| `isVideoUploadAllowed` | `boolean` | If `true`, allows video file uploads alongside photos. | | `false` |
| `item_type` | `string` | The backend item type associated with the attachment (e.g., 'photo', 'video'). | | `'unknown'` |
| `label` | `string` | | | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `max_files` | `number` | Maximum number of files that can be attached. | | `10` |
| `max_upload_filesize` | `object` | An object defining maximum upload size per file type (e.g., `{ photo: 5242880, video: 10485760 }`). | | `{}` |
| `maxFilesDescription` | `string` | Custom description text related to the maximum file limit. | | |
| `min_files` | `number` | Minimum number of files required. | | `1` |
| `multiple` | `boolean` | Allows selecting multiple files if `true`. | | `false` |
| `paddingBottom` | `string` | | | |
| `required` | `boolean` | | | `false` |
| `variant` | `'standard' \| 'outlined' \| 'filled' \| 'standard-inlined'` | Specifies the visual style of the component. | | `'standard-inlined'` |

## AttachPoll

Allows users to attach, view, edit, or remove a poll within a form. It presents a button to initiate the poll creation/editing process via a separate form screen (`form.edit` route) using the provided `formUrl`, and displays a preview of the attached poll using the `ui.AttachPollPreview` component.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | `undefined` |
| `disabled` | `boolean` | | | `false` |
| `formUrl` | `string` | API endpoint URL to fetch/submit the poll form data. | Yes | `undefined` |
| `fullWidth` | `boolean` | | | `true` |
| `label` | `string` | | | `undefined` |
| `margin` | `'none' \| 'normal' \| 'dense'` | | | `'normal'` |
| `placeholder` | `string` | | | `'attach_poll'` |
| `size` | `'small' \| 'medium'` | Defines the size of the control elements (like the button). | | `'medium'` |

## AuthenticatorQrCode

Displays a QR code, typically used for setting up two-factor authentication (2FA). It shows the QR code image, a button to attempt opening a 2FA app, a manual setup key (description), and a button to copy the key.

For a visual reference, see [AuthenticatorQrCode Gallery](./form-elements/AuthenticatorQrCode.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `content` | `string` | The content/data to encode in the QR code and the URL to open 2FA apps. | Yes | `undefined` |
| `description` | `string` | | | `undefined` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | | `undefined` |
| `margin` | `'none'`, `'dense'`, `'normal'` | | | - |
| `paddingBottom` | `'none'`, `'dense'`, `'normal'` | | Yes | - |
| `placeholder` | `string` | | | `undefined` |
| `variant` | `'standard'`, `'standard-inlined'` | Specifies the visual style of the component. | | `'standard'` |

## Autocomplete

A form element allowing users to select one or multiple options from a list, often populated dynamically via an API search. It presents the selected value(s) and opens a dedicated interface for searching and selecting options.

For a visual reference, see [Autocomplete Gallery](./form-elements/Autocomplete.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `choice_type` | `string` | Influences how choices are presented or handled internally. | | `undefined` |
| `disable_uncheck` | `boolean` | If `true`, prevents unselecting the currently selected option (single mode). | | `false` |
| `enable_search` | `boolean` | If `true`, enables a search input within the selection interface. | | `true` |
| `fullWidth` | `boolean` | | | `true` |
| `icon` | `string` (IconName) | Name of the icon to display, primarily used in the 'livestream' variant. | | `undefined` |
| `label` | `string` | | Yes | |
| `margin` | `string` ('normal', 'dense', 'none') | | | `'normal'` |
| `multiple` | `boolean` | If `true`, allows the user to select multiple options. | | `false` |
| `paddingBottom` | `string` ('normal', 'dense', 'none') | | | `undefined` |
| `placeholder` | `string` | | | `''` |
| `required` | `boolean` | | | `false` |
| `search_endpoint` | `string` | API endpoint URL used to fetch options dynamically based on user input. | Yes | |
| `search_params` | `object` | Additional parameters to include in the API request to `search_endpoint`. | | `{}` |
| `size` | `string` ('medium', 'small') | The size of the form field. | | `'medium'` |
| `variant` | `'standard'`, `'standard-inlined'`, `'standard-outlined'`, `'outlined'`, `'livestream'` | Specifies the visual style of the component. | | `'outlined'` |

## AvatarUpload

A form element that allows users to select and upload an avatar image, displaying a preview. It integrates with the device's image picker and handles basic validation display.

For a visual reference, see [AvatarUpload Gallery](./form-elements/AvatarUpload.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `borderColor` | `string` | Color of the border around the avatar image. | | `undefined` |
| `circle` | `boolean` | Renders the avatar preview as a circle. | | `true` |
| `fullWidth` | `boolean` | | | `false` |
| `margin` | `keyof typeof SizeEnum` | | | `'none'` |
| `paddingBottom` | `keyof typeof SizeEnum` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `size` | `string` | Size of the avatar preview (e.g., 'small', 'medium', 'xxlarge'). | | `'xxlarge'` |
| `spaceColor` | `string` | Color of the space around the avatar image. | | `undefined` |
| `spaceWidth` | `number` | Width of the space around the avatar image. | | `undefined` |

## Birthday

This component internally uses element `Date`, refer it for more information.

For a visual reference, see [Date Gallery](./form-elements/Date.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | - |
| `disabled` | `boolean` | | | `false` |
| `displayFormat` | `string` | The format (using moment.js tokens) to display the selected date. | | Locale default |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `string` | Sets the initial date displayed in ISO 8601 format. | | - |
| `label` | `string` | | | - |
| `margin` | `'none' \| 'normal' \| 'dense'` | | | `'normal'` |
| `maxDate` | `string` | The latest selectable date in ISO 8601 format (e.g., "2024-12-31"). | | Current Date |
| `minDate` | `string` | The earliest selectable date in ISO 8601 format (e.g., "1900-01-01"). | | - |
| `placeholder` | `string` | | | - |
| `required` | `boolean` | | | `false` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

## Button

A form element that renders a toggleable button. Its text changes based on its internal state (0 or 1), typically used to trigger an action or represent a binary choice within a form.

For a visual reference, see [Button Gallery](./form-elements/Button.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `cancelLabel` | `string` | The text displayed on the button when its value is 0 (inactive state). | Yes | |
| `disabled` | `boolean` | | | `false` |
| `fullWidth` | `boolean` | | | `true` |
| `label` | `string` | The text displayed on the button when its value is 1 (active state). | Yes | |
| `margin` | `'normal' \| 'dense' \| 'none'` | | | `'normal'` |
| `size` | `'small' \| 'medium'` | The size applied to the surrounding form control. | | `undefined` |

## Checkbox

A form element that renders a checkbox input field. It allows users to toggle between a checked and unchecked state, typically representing a boolean value or a specific selection.

For a visual reference, see [Checkbox Gallery](./form-elements/Checkbox.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `checkedValue` | `any` | The value submitted when the checkbox is checked. | | `1` |
| `description` | `string` | | | `''` |
| `disabled` | `boolean` | | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `isReverse` | `boolean` | If true, reverses the order of the label and checkbox control. | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `required` | `boolean` | | | `false` |
| `uncheckedValue` | `any` | The value submitted when the checkbox is unchecked. | | `0` |
| `variant` | `'outlined' \| 'standard-inlined'` | Specifies the visual style of the component. | | `'standard-inlined'` |

## CheckboxGroup

This element renders a group of checkboxes, allowing users to select multiple options from a predefined list. It integrates with Formik for state management and validation.

For a visual reference, see [CheckboxGroup Gallery](./form-elements/CheckboxGroup.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `disabled` | `boolean` | | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `hasFormOrder` | `boolean` | If `true`, prepends the `order` number to the label. | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `'normal' \| 'dense' \| 'none'` | | | `undefined` |
| `options` | `Array<{ label: string, value: any }>` | An array of objects defining the available checkbox options. | Yes | `[]` |
| `order` | `number` | The numerical order to display before the label (if `hasFormOrder` is true). | | `undefined` |
| `paddingBottom` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

## Chip

Renders a group of selectable chip buttons. Selecting a chip updates the form's `title` and `description` fields with the corresponding values from the selected option.

For a visual reference, see [Chip Gallery](./form-elements/Chip.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `label` | `string` | | Yes | |
| `options` | `RadioFieldOptions[]` | An array of option objects to render as chips. Each should have `title` and `description`. | Yes | `[]` |
| `required` | `boolean` | | | `false` |

## ClearSearch

This element displays a title and a conditional "Reset" button within a form. The button allows users to reset specific form fields (defined by `targetFields`) back to their initial values. The button only appears when the current values of the target fields differ from their initial state.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `align` | `string` | Alignment configuration (appears unused in the current implementation). | | `'right'` |
| `label` | `string` | The localization key for the text displayed on the reset button. | | `'reset'` |
| `targetFields` | `string[]` | An array of form field names that this element will reset when the button is pressed. | | `['sort', 'when', 'category_id']` |
| `title` | `string` | The localization key for the title displayed above the reset button. | | `'filter'` |

## Clickable

A form element that displays a label and a right arrow, acting as a button. When clicked, it dispatches a specified Redux action with given parameters. It's typically used to navigate to another screen or trigger a modal for further input or selection.

For a visual reference, see [Clickable Gallery](./form-elements/Clickable.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `action` | `string` | The Redux action type to dispatch on click. | Yes | |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `'normal' \| 'dense' \| 'none'` | | | `'normal'` |
| `name` | `string` | The name of the field in the form state. | Yes | |
| `paddingBottom` | `boolean` | | | `false` |
| `params` | `object` | The payload to send with the dispatched action. | Yes | |
| `severity` | `'error' \| 'warning' \| 'info' \| 'success'` | Sets the text color based on severity (e.g., for validation). | | |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

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

## CountryCityCode

This form element provides an input field that allows users to select a country and associated city/state code. It typically opens a dedicated selection interface (modal or screen) for browsing and choosing the appropriate code.

For a visual reference, see [CountryCityCode Gallery](./form-elements/CountryCityCode.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `backgroundColor` | `string` | Background color for the animated placeholder (used in 'standard-outlined' variant). | | `undefined` |
| `disable_uncheck` | `boolean` | Prevents the user from unselecting the current value if set to true. | | `false` |
| `enable_search` | `boolean` | Enables search functionality within the selection view. | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | `''` |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `required` | `boolean` | | | `false` |
| `search_endpoint` | `string` | API endpoint used for searching options if `enable_search` is true. | | `undefined` |
| `search_params` | `object` | Additional parameters for the search request. Values can be dynamically sourced from the form context. | | `undefined` |
| `variant` | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined'` | Specifies the visual style of the component. | | `'standard'` |

## countryStatePicker

This element provides a specialized picker for selecting a country and its corresponding state or province. It typically fetches state/province options dynamically based on the selected country from `CountryCityCode`.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `backgroundColor` | `string` | Background color for the element (used in specific variants). | | `undefined` |
| `disable_uncheck` | `boolean` | Prevents unselecting the current value if the field is required. | | `false` |
| `disabled` | `boolean` | | | `false` |
| `enable_search` | `boolean` | Enables searching within the options list (if applicable). | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | `''` |
| `margin` | `'normal' \| 'dense' \| 'none'` | | | `'normal'` |
| `paddingBottom` | `'normal' \| 'dense' \| 'none'` | | | `'normal'` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `search_endpoint` | `string` | API endpoint to fetch options dynamically (e.g., states based on country). | | `undefined` |
| `search_params` | `object` | Additional parameters for the search API endpoint. | | `undefined` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

## CustomButton

A form element that renders a button which dispatches a custom Redux action when pressed.

For a visual reference, see [CustomButton Gallery](./form-elements/CustomButton.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `customAction` | `{ type: string; payload?: any; meta?: any }` | An object defining the Redux action dispatched on press. `type` is required, `payload` and `meta` are optional. | Yes | |
| `disabled` | `boolean` | | | `false` |
| `label` | `string` | | Yes | |
| `name` | `string` | The unique identifier for the form field. | Yes | `CustomButtonField` |
| `variant` | `string` | Specifies the button style. Currently supports 'link'. | Yes | `'link'` |

## Date

A form element that allows users to select a date, time, or both using a native modal picker.

For a visual reference, see [Date Gallery](./form-elements/Date.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `datePickerMode` | `'date' \| 'time' \| 'datetime'` | Determines if the picker selects date, time, or both. | | `'datetime'` |
| `description` | `string` | | | |
| `disabled` | `boolean` | | | `false` |
| `displayFormat` | `string` | The `moment.js` format string used to display the selected date/time. | | `'DD/MM/YYYY - HH:mm'` |
| `endOfDay` | `boolean` | If `true`, sets the selected time to the end of the day (23:59:59). | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | `'close_time'` |
| `margin` | `'none' \| 'normal' \| 'dense'` | | | `'normal'` |
| `maxDate` | `string` | The maximum selectable date (ISO string or format specified by `momentResultFormat`). | | |
| `minDate` | `string` | The minimum selectable date (ISO string or format specified by `momentResultFormat`). | | |
| `placeholder` | `string` | | | |
| `required` | `boolean` | | | `false` |
| `startOfDay` | `boolean` | If `true`, sets the selected time to the start of the day (00:00:00). | | `false` |
| `time_zone_gmt` | `string` | Timezone identifier (e.g., 'Asia/Ho_Chi_Minh') for display formatting. | | User's timezone |
| `timeFormat` | `12 \| 24` | Specifies 12 or 24-hour time format for the picker. | | `12` |
| `variant` | `'standard' \| 'outlined' \| 'standard-outlined' \| 'outlined-inlined'` | Specifies the visual style of the component. | | `'standard'` |

## DateBasic

A form element component that provides a user interface for selecting a date, time, or datetime using a native modal picker. It integrates with Formik for form state management.

For a visual reference, see [Date Gallery](./form-elements/Date.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `datePickerMode` | `'date' \| 'time' \| 'datetime'` | Determines the type of picker shown (`date`, `time`, or `datetime`). | | `'date'` |
| `disabled` | `boolean` | | | `false` |
| `editable` | `boolean` | If `false`, the text input part is not directly editable by the user. | | `true` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `string` | An initial value to populate the date field with. | | `undefined` |
| `label` | `string` | | | `'close_time'` |
| `margin` | `string` | | | `normal` |
| `maxDate` | `string` | The latest selectable date (format defined by `momentResultFormat`). | | `undefined` |
| `minDate` | `string` | The earliest selectable date (format defined by `momentResultFormat`). | | `undefined` |
| `momentResultFormat` | `string` | The Moment.js format string used for parsing `minDate` and `maxDate`. | | `''` |
| `paddingBottom` | `string` | | | `normal` |
| `placeholder` | `string` | | | `''` |
| `required` | `boolean` | | | `false` |
| `resultFormat` | `string` | The desired format for the final value submitted by the form. | | `''` |
| `time_zone_gmt` | `string` | Specifies the GMT timezone offset (e.g., "+07:00"). | | `''` |
| `timeFormat` | `number` | Specifies the time format (e.g., `12` or `24` for 12/24 hour format). | | `12` |
| `valueFormat` | `string` | The Moment.js format string for displaying and storing the selected value. | | `'DD/MM/YYYY'` |
| `variant` | `'standard' \| 'outlined' \| 'standard-outlined' \| 'outlined-inlined'` | Specifies the visual style of the component. | | `'standard'` |

## Datetime

*Note: This element inherits most props from the base `Date` element.*

For a visual reference, see [Date Gallery](./form-elements/Date.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `datePickerMode` | `'date' \| 'time' \| 'datetime'` | Determines if the picker selects date, time, or both. | | `'datetime'` |
| `description` | `string` | | | |
| `disabled` | `boolean` | | | `false` |
| `displayFormat` | `string` | The Moment.js format string used to display the selected value. | | `'DD/MM/YYYY - HH:mm'` |
| `endOfDay` | `boolean` | If true, sets the selected date's time to the end of the day (23:59:59). | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `string` | An initial value for the date/time field (ISO 8601 format recommended). | | |
| `label` | `string` | | | `'close_time'` |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `maxDate` | `string` | The maximum selectable date (format depends on `momentResultFormat`). | | |
| `minDate` | `string` | The minimum selectable date (format depends on `momentResultFormat`). | | |
| `momentResultFormat` | `string` | The Moment.js format string used for parsing `minDate` and `maxDate`. | | |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `placeholder` | `string` | | | |
| `required` | `boolean` | | | `false` |
| `startOfDay` | `boolean` | If true, sets the selected date's time to the start of the day (00:00:00). | | `false` |
| `time_zone_gmt` | `string` | The timezone identifier (e.g., 'America/New_York') used for formatting. | | |
| `timeFormat` | `12 \| 24` | Specifies 12-hour or 24-hour time format for the picker. | | (Locale default) |
| `variant` | `'standard' \| 'outlined' \| 'standard-outlined' \| 'outlined-inlined'` | Specifies the visual style of the component. | | `'standard'` |

## Description

Displays a simple text label within a form, often used for informational purposes or section descriptions.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `keyof typeof SizeEnum` | | | `undefined` |
| `paddingBottom` | `keyof typeof SizeEnum` | | | `undefined` |
| `variant` | `keyof typeof Variant` | Specifies the visual style of the component. | | `'standard'` |

## DynamicTypo

Displays a dynamic description text based on the value of a related form field. It looks up the description from the `config.data` array using the value of the field specified in `config.relatedField`.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `data` | `Array<{ value: any; description: string; }>` | Array of value-description pairs. | Yes | `[]` |
| `fullWidth` | `boolean` | | | |
| `margin` | `'dense' \| 'normal' \| 'none'` | | | |
| `paddingBottom` | `'dense' \| 'normal' \| 'none'` | | | |
| `relatedField` | `string` | Name of the form field whose value determines the displayed description. | Yes | |
| `required` | `boolean` | | | |
| `variant` | `'outlined' \| 'filled' \| 'standard'` | Specifies the visual style of the component. | | |

## Editor

*Note: This element inherits most props from the base `Text` element.*

For a visual reference, see [Text Gallery](./form-elements/Text.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none' \| 'sentences' \| 'words' \| 'characters'` | Controls automatic capitalization behavior. | | `'sentences'` |
| `autoCorrect` | `boolean` | Enables or disables auto-correction for the input. | | `true` |
| `autoFocus` | `boolean` | | | `false` |
| `backgroundColor` | `string` | Sets the background color for the input wrapper. | | |
| `clearButtonMode` | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | (iOS only) When to display the clear text button. | | `'never'` |
| `contextualDescription` | `string` | Additional descriptive text displayed near the input. | | |
| `description` | `string` | | | |
| `editable` | `boolean` | If `false`, the text input is not editable. | | `true` |
| `findReplace` | `{ find: string, replace: string }` | Configuration to automatically generate a slug-like value based on input. | | |
| `fullWidth` | `boolean` | | | `false` |
| `hasCopy` | `boolean` | If `true`, displays a copy-to-clipboard icon button. | | `false` |
| `hasQRScanner` | `boolean` | If `true`, displays a QR code scanner icon button. | | `false` |
| `label` | `string` | | | |
| `margin` | `'none' \| 'normal' \| 'dense'` | | | `'normal'` |
| `maxLength` | `number` | | | |
| `minHeight` | `number` | | | |
| `multiline` | `boolean` | If `true`, allows multiple lines of text input (textarea). | | `false` |
| `placeholder` | `string` | | | |
| `qrScannerParamName` | `string` | Query parameter name to extract from the scanned QR code URL. | | `'invite_code'` |
| `required` | `boolean` | | | `false` |
| `validateAction` | `string` | Name of a registered action for backend validation triggered on blur. | | |
| `variant` | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined' \| 'livestream'` | Specifies the visual style of the component. | | `'standard'` |

## Email

*Note: This element inherits most props from the base `Text` element.*

For a visual reference, see [Text Gallery](./form-elements/Text.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `...rest` | `TextInputProps` | Other standard React Native `TextInput` props are accepted. | | `undefined` |
| `autoCapitalize` | `'none'`, `'sentences'`, `'words'`, `'characters'` | How to automatically capitalize text. For Email, defaults to 'none'. | | `'none'` |
| `autoFocus` | `boolean` | | | `false` |
| `clearButtonMode` | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | When to display the clear text button (iOS only). | | `'never'` |
| `description` | `string` | | | `undefined` |
| `disabled` | `boolean` | | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `keyboardType` | `string` | Determines which keyboard to open (e.g., 'numeric', 'email-address'). For Email, defaults to 'email-address'. | | `'email-address'` |
| `label` | `string` | | | `undefined` |
| `margin` | `'normal'`, `'dense'`, `'none'` | | | `'normal'` |
| `maxLength` | `number` | | | `undefined` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `returnKeyType` | `string` | Determines how the return key should look. | | `'default'` |
| `textContentType` | `string` | Give the keyboard and the system information about the expected semantic meaning for the content. For Email, defaults to 'emailAddress'. | | `'emailAddress'` |
| `validateAction` | `string` | Name of a registered action for backend validation on blur. | | `undefined` |
| `variant` | `'standard'`, `'outlined'`, `'filled'`, `'standard-outlined'` | Specifies the visual style of the component. | | `'standard'` |

## File

The `File` form element allows users to select and upload a single file, typically an image or video. It provides options to choose from the device library or capture directly using the camera. It handles file preview, upload progress (implicitly via `SinglePhotoItemView`), deletion, and file size validation.

For a visual reference, see [File Gallery](./form-elements/File.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `cropping` | `boolean` | Enable image cropping after selection (currently might have limitations). | | `false` |
| `description` | `string` | | | `''` |
| `extraProps` | `object` | Additional props for styling or behavior. | | `{}` |
| `file_type` | `string` | Type of file allowed ('photo', 'video'). | | `photo` |
| `fullWidth` | `boolean` | | | `false` |
| `include_exif` | `boolean` | Include EXIF data when selecting photos. | | `true` |
| `item_type` | `string` | The type identifier for the uploaded item on the backend. | | `unknown` |
| `label` | `string` | | | `''` |
| `margin` | `string` | | | `normal` |
| `max_upload_filesize` | `object` | Max file sizes in bytes (e.g., `{ photo: 5242880, video: 10485760 }`). `0` means no limit. | | `{ photo: 0, video: 0 }` |
| `paddingBottom` | `string` | | | `normal` |
| `preview_url` | `string` | URL of an existing image/file to preview initially. | | `undefined` |
| `required` | `boolean` | | | `false` |
| `upload_url` | `string` | The API endpoint for direct file uploads. | | `/file` |
| `variant` | `'standard' \| 'outlined' \| 'outlined-inlined' \| 'standard-inlined'` | Specifies the visual style of the component. | | `standard-inlined` |

## Form

The `Form` element acts as a container for rendering other form elements. It provides layout options and handles scrolling, including keyboard awareness and integration with bottom sheets. When `scrollable` is enabled, it groups elements into `top`, `bottom`, `full_space`, and other categories for layout purposes.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `disableContainerStyle` | `boolean` | If true and `scrollable` is true, disables the default `flex: 1` style applied to the scroll container. | | `false` |
| `elements` | `Record<string, any>` | An object containing configurations for nested form elements. | Yes | `{}` |
| `isBottomSheet` | `boolean` | If true, adapts scrolling behavior for use within a bottom sheet. | | `false` |
| `scrollable` | `boolean` | If true, wraps the main elements in a scrollable container with keyboard awareness. | | `false` |

## FormBottom

Renders a styled container at the bottom of a form, typically used to group related elements like submit buttons or secondary actions. It can display an optional label and description, and renders a collection of nested form elements.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | `undefined` |
| `elements` | `Record<string, FormFieldConfig>` | An object containing configurations for nested form elements to be rendered within this section. | Yes | `{}` |
| `label` | `string` | | | `undefined` |

## FormContent

The `FormContent` element acts as a container to group and render other form elements defined in its configuration. It can optionally display a label and description above the nested elements.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | `undefined` |
| `elements` | `Record<string, ElementConfig>` | An object containing configurations for nested elements. | Yes | |
| `label` | `string` | | | `undefined` |

## FormDescription

Displays a description text within a form, supporting simple HTML content.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | `null` |
| `numberOfLines` | `number` | Limits the number of lines displayed for the description text. | | `undefined` |
| `style` | `object` | Custom styling for the description container View. | | `{}` |

## FormFooter

Renders a footer section for a form, capable of displaying a label, description, and nested form elements.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | `null` |
| `elements` | `Record<string, ElementConfig>` | An object containing configurations for nested form elements. | Yes | `{}` |
| `label` | `string` | | | `null` |

## FormHeader

Configures the navigation header for a form screen, setting the title, back button (left), and submit button (right). This element renders `null` and uses `navigation.setOptions` to apply the header configuration.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `showLeftHeader` | `boolean` | Whether to show the left header button (Back). | | `true` |
| `showRightHeader` | `boolean` | Whether to show the right header button (Submit). | | `true` |
| `title` | `string` | The title displayed in the header. | | `schema.title` |

## FormTop

Renders a top section for a form, optionally displaying a label and description, and rendering a collection of nested form elements.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | `undefined` |
| `elements` | `Record<string, FormFieldConfig>` | Object containing configurations for nested form elements to be rendered. | Yes | |
| `label` | `string` | | | `undefined` |

## FriendPicker

A form element that allows users to select one or multiple friends from a list, typically fetched via an API. It presents a user-friendly interface for friend selection within forms.

For a visual reference, see [FriendPicker Gallery](./form-elements/FriendPicker.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `api_endpoint` | `string` | API endpoint to fetch friend suggestions. | Yes | `undefined` |
| `choice_type` | `string` | Type of choice mechanism. | | `undefined` |
| `disable_custom` | `boolean` | Disables custom privacy selection. | | `false` |
| `disable_uncheck` | `boolean` | Prevents unselecting if required. | | `false` |
| `disabled` | `boolean` | | | `false` |
| `enable_search` | `boolean` | Enables searching within the friend list. | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `OptionsItemShape[]` | Initial selected friend(s). | | `undefined` |
| `label` | `string` | | | `''` |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `multiple` | `boolean` | Allows selecting multiple friends. | | `false` |
| `options` | `OptionsItemShape[]` | Predefined list of options. | | `[]` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `undefined` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `showWithoutOptions` | `boolean` | Whether to show the field without options. | | `undefined` |
| `suboptions` | `SubOptionsShape` | Additional options or configurations. | | `undefined` |
| `value_type` | `string` | Specifies the type of value returned. | | `undefined` |
| `variant` | `'standard' \| 'outlined' \| 'standard-inlined' \| 'standard-outlined'` | Specifies the visual style of the component. | | `'standard'` |

## GatewayButton

Renders a button specific to a payment gateway (e.g., Apple Pay, Stripe). It handles setting the selected gateway ID, passing relevant data, and triggering form submission upon click. It can display platform-specific buttons (Apple Pay/Google Pay) or a generic button based on the `variant` prop.

For a visual reference, see [GatewayButton Gallery](./form-elements/GatewayButton.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `confirmation` | `{ title: string, message: string }` | Optional configuration for a confirmation dialog shown before submission (used for `activitypoint` variant). | | |
| `description` | `string` | | | `''` |
| `disabled` | `boolean` | | | `false` |
| `fullWidth` | `boolean` | | | `true` |
| `gateway_config` | `any` | Configuration specific to the selected payment gateway, passed to the form on submission. | Yes | |
| `gateway_id` | `string \| number` | The unique identifier for the payment gateway this button represents. | Yes | |
| `icon` | `string` | Optional icon name (from the icon set) to display on the generic button. | | |
| `item` | `any` | Item data associated with the payment, passed to the form on submission. | Yes | |
| `label` | `string` | | Yes | |
| `margin` | `'none' \| 'dense' \| 'normal' \| 'small'` | | | `'none'` |
| `size` | `'small' \| 'medium' \| 'large'` | Size applied to the underlying form control (affects spacing/layout). | | |
| `variant` | `'applepay' \| 'googlepay' \| 'stripe' \| 'paypal' \| 'activitypoint'` | The type of gateway. Determines rendering logic, platform availability (Apple/Google Pay), and behavior. | Yes | |

## Hidden

A form element that stores a value in the form state without rendering any visible UI element. It's typically used to pass data that shouldn't be directly modified by the user.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `defaultValue` | `string` | The default value to set if `config.value` is not provided. | | `null` |
| `value` | `string` | The specific value to set for the hidden field. | | `null` |

## HtmlLink

*Note: This element inherits most props from the base `LinkButton` element.*

For a visual reference, see [LinkButton Gallery](./form-elements/LinkButton.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `action` | `string` | A Redux action type to dispatch when the button is pressed. Takes precedence over `link` and `actionName`/`routerName`. | | |
| `actionName` | `string` | Specifies the type of navigation action (e.g., 'reset', 'navigate'). Used if `action` is not provided. | | `'navigate'` |
| `actionPayload` | `Record<string, any>` | The payload to include with the dispatched Redux action specified by `action`. | | `{}` |
| `description` | `string` | | | |
| `label` | `string` | | Yes | |
| `link` | `string` | A URL path to navigate to when the button is pressed. Used if `action` is not provided. | | |
| `margin` | `'normal'` | | Yes | |
| `routerName` | `string` | The name of the route to navigate to, used with `actionName`. Primarily for navigation actions like 'reset'. | | `'forgot-password'` |
| `textTransform` | `'none' \| 'capitalize' \| 'uppercase' \| 'lowercase'` | Controls the text transformation (e.g., uppercase, lowercase). | | |

## Information

Displays HTML content fetched based on the field's value, typically representing related information (e.g., a forum post).

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `undefined` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

## input

*Note: This element inherits most props from the base `Text` element.*

For a visual reference, see [Text Gallery](./form-elements/Text.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none'`, `'sentences'`, `'words'`, `'characters'` | Auto-capitalization behavior. | | `'sentences'` |
| `autoCorrect` | `boolean` | Enable/disable auto-correction. | | `true` |
| `autoFocus` | `boolean` | | | `false` |
| `backgroundColor` | `string` | Background color for the input container. | | |
| `clearButtonMode` | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Controls when the clear button appears (iOS only). | | `'never'` |
| `contextualDescription` | `string` | Additional description text, often used with `findReplace`. | | |
| `description` | `string` | | | |
| `disabled` | `boolean` | | | `false` |
| `editable` | `boolean` | If false, the text is not editable (overridden by `disabled`). | | `true` |
| `label` | `string` | | | `'close_time'` |
| `margin` | `'dense' \| 'normal' \| 'none'` | | | `'normal'` |
| `maxDate` | `string` | The latest selectable date/time (ISO 8601 format string). | | |
| `minDate` | `string` | The earliest selectable date/time (ISO 8601 format string). | | |
| `placeholder` | `string` | | | |
| `required` | `boolean` | | | `false` |
| `startOfDay` | `boolean` | If `true`, sets the selected time to the beginning of the day (00:00:00). | | `false` |
| `time_zone_gmt` | `string` | Timezone identifier (e.g., 'America/New_York') for calculations. | | User's setting |
| `timeFormat` | `12 \| 24` | Specifies whether to use 12-hour or 24-hour format in the time picker. | | User's setting |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

# InviteFriendPicker

A form element designed to allow users to select one or multiple friends for invitation purposes. It typically fetches friend suggestions via an API endpoint and presents them in a dedicated selection interface.

## Props

| Name | Type | Description | Required | Default |
| :-- | :-- | :-- | :-- | :-- |
| `label` | `string` | Field label text. | Yes | `''` |
| `api_endpoint` | `string` | API endpoint for friend suggestions. | Yes | `''` |
| `fullWidth` | `boolean` | Take full container width. |  | `false` |
| `margin` | `'none' \| 'dense' \| 'normal'` | Margin spacing. |  | `'normal'` |
| `required` | `boolean` | Field must have a value. |  | `false` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Display style variant. |  | `'standard'` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | Bottom padding spacing. |  | `'normal'` |
| `suboptions` | `SubOptionsShape` | Configuration for sub-options. |  | `undefined` |
| `disable_custom` | `boolean` | Disable custom privacy/selection option. |  | `false` |
| `multiple` | `boolean` | Allow selecting multiple friends. |  | `false` |
| `enable_search` | `boolean` | Enable search in picker screen. |  | `false` |
| `disable_uncheck` | `boolean` | Prevent unselecting chosen options. |  | `false` |
| `choice_type` | `string` | Type of choice (internal use). |  | `''` |
| `placeholder` | `string` | Placeholder text when no value selected. |  | `''` |
| `api_params` | `Record<string, any>` | Additional API request parameters. |  | `{ q: ':q' }` |

# LinkButton

This form element renders a button styled as a link. It can be configured to navigate to a specific route/link or dispatch a Redux action upon being pressed. It's often used for actions like navigating to a "Forgot Password" screen or triggering secondary form actions.

## Props

| Name | Type | Description | Required | Default |
| :-- | :-- | :-- | :-- | :-- |
| `label` | `string` | The text displayed on the link button. | Yes |  |
| `description` | `string` | A description text displayed above the button. | |  |
| `link` | `string` | A URL path (relative) to navigate to when pressed. Takes precedence over `actionName`/`routerName` if `action` is not set. | |  |
| `action` | `string` | The type string of a Redux action to dispatch when pressed. Takes precedence over `link` and `actionName`/`routerName`. | |  |
| `actionPayload` | `Record<string, any>` | The payload object to send with the dispatched Redux `action`. | | `{}` |
| `actionName` | `'navigate' \| 'reset'` | Specifies the navigation action type. Used if `action` and `link` are not provided. | | `'navigate'` |
| `routerName` | `string` | The name of the route to navigate to. Used with `actionName`. | | `'forgot-password'` |
| `textTransform` | `'none' \| 'capitalize' \| 'uppercase' \| 'lowercase'` | CSS text-transform property for the button label. | | `'none'` |
| `margin` | `'normal'` | Controls the margin around the form control. | | `'normal'` |

# Location

A form field that allows users to select a geographical location using a native location picker interface. Clicking the field opens the picker, and the selected location's address is displayed.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `label` | `string` | The label displayed for the form field. | Yes | |
| `placeholder` | `string` | Placeholder text shown when no location is selected (not shown for 'standard-outlined' variant). | | `''` |
| `variant` | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined' \| 'livestream'` | Controls the visual style of the component. | | `'standard'` |
| `fullWidth` | `boolean` | If `true`, the component takes the full width of its container. | | `false` |
| `margin` | `'none' \| 'dense' \| 'normal'` | Controls the margin around the component. | | `'normal'` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | Controls the bottom padding of the component. | | `'normal'` |
| `required` | `boolean` | Marks the field as required in the form validation. | | `false` |
| `disabled` | `boolean` | If `true`, the input field is disabled. | | `false` |
| `types` | `PlaceType[]` | Filters the types of places returned by the location picker (e.g., 'address', 'geocode', 'establishment'). | | |
| `inline` | `boolean` | Controls if the label is displayed inline with the input. | | `false` |

# MembershipQuestion

The `MembershipQuestion` form element allows users to define a question with different answer formats (Checkbox, Multiple Choice, or Written Answer) typically used for group membership applications. It includes fields for the question text, selecting the answer type, and managing answer options if applicable.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `label` | `string` | The label text displayed above the element. | | `undefined` |
| `description` | `string` | Additional descriptive text displayed below the label. | | `undefined` |
| `required` | `boolean` | Marks the field as required (visually). | | `false` |
| `multiline` | `boolean` | Allows the question input field to accept multiple lines. | | `false` |
| `clearButtonMode` | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Determines when the clear button appears on the text input (iOS only). | | `undefined` |
| `disabled` | `boolean` | Disables the entire form element. | | `false` |
| `maxLength` | `number` | Maximum number of answer options allowed for Checkbox/Multiple Choice types. | | `5` |
| `editable` | `boolean` | Determines if the question text input can be edited. | | `true` |
| `minHeight` | `number` | Sets the minimum height for the question text input. | | `undefined` |
| `paddingBottom` | `string`, `number` | Adds padding to the bottom of the form control. | | `undefined` |
| `margin` | `string` | Sets the margin around the form control. | | `undefined` |
| `fullWidth` | `boolean` | Makes the form control occupy the full available width. | | `false` |

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

# MultiChoice

The `MultiChoice` form element allows users to select one or multiple options from a predefined list, typically presented using checkboxes when multiple selections are allowed. It is functionally equivalent to the `Select` element but configured for multiple selections.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :------- | :------ |
| `label` | `string` | The text label displayed for the field. | Yes | |
| `description` | `string` | Additional descriptive text displayed below the field. | | |
| `options` | `OptionsItemShape[]` | An array of available options to select from. | Yes | `[]` |
| `multiple` | `boolean` | If true, allows selecting multiple options. Defaults to `true` for MultiChoice. | | `true` |
| `required` | `boolean` | Whether the field is required. | | `false` |
| `disabled` | `boolean` | If true, disables the field. | | `false` |
| `variant` | `'standard', 'outlined', 'filled'` | The visual style of the component. | | `'standard'` |
| `margin` | `'normal', 'dense', 'none'` | Defines the margin size around the component. | | `'normal'` |
| `fullWidth` | `boolean` | If true, the component takes up the full width of its container. | | `false` |
| `placeholder` | `string` | Placeholder text shown when no value is selected. | | `'select'` |
| `enable_search` | `boolean` | If true, enables a search input within the option selector modal. | | `false` |
| `disableClearable` | `boolean` | If true, prevents the user from clearing the selection (requires a value). | | `false` |
| `value_type` | `string` | Specifies the expected data type of the value ('array' or single value). | | `'array'` |
| `suboptions` | `SubOptionsShape` | Defines sub-options, often used for dependent selections. | | `undefined` |
| `useSectionList` | `boolean` | If true, uses a SectionList for displaying options (for grouped options). | | `false` |
| `showWithoutOptions` | `boolean` | If true, renders the component even if no options are provided. | | `false` |

# MultiFile

Allows users to select and upload multiple files (photos, videos, or other types based on configuration). This element is an alias for the `Attachment` element but typically used when multiple file selection is intended.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :------- | :------ |
| `label` | `string` | The label text for the field. | Yes | - |
| `description` | `string` | Additional descriptive text below the label. | | - |
| `multiple` | `boolean` | Allow selecting multiple files. Set to `true` for multi-file selection. | | `false` |
| `file_type` | `string` | The type of file allowed ('photo', 'video', 'attachment', etc.). | | `'photo'` |
| `item_type` | `string` | The resource type associated with the uploaded item (e.g., 'photo', 'blog'). | | `'unknown'` |
| `max_files` | `number` | Maximum number of files allowed. | | `10` |
| `min_files` | `number` | Minimum number of files required. | | `1` |
| `max_upload_filesize` | `object` | Maximum upload size per file type in bytes. | | - |
| `isVideoUploadAllowed` | `boolean` | Explicitly allow video uploads alongside photos. | | `false` |
| `cropping` | `boolean` | Enable image cropping after selection. | | `false` |
| `include_exif` | `boolean` | Include EXIF data with uploaded images. | | `false` |
| `maxFilesDescription` | `string` | Custom description related to the maximum file limit. | | - |
| `current_files` | `array` | Array of pre-existing file objects (used for editing). | | `[]` |
| `fullWidth` | `boolean` | Whether the element should take up the full width. | | `false` |
| `margin` | `'normal', 'dense', 'none'` | Margin style. | | `'normal'` |
| `variant` | `string` | The display variant of the form control. | | `'standard-inlined'` |
| `required` | `boolean` | Whether the field is required (validation). | | `false` |
| `disabled` | `boolean` | Disable the form element. | | `false` |
| `name` | `string` | The name of the field in the form state. | Yes | - |
| `paddingBottom` | `string` | Custom padding at the bottom. | | - |

# NumberCode

A form input element designed for entering numerical codes (like One-Time Passwords) digit by digit into separate input boxes.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :------- | :------ |
| `label` | `string` | The label displayed above the input fields. | | `undefined` |
| `editable` | `boolean` | Determines if the input fields are editable. | | `true` |
| `variant` | `'standard', 'outlined', 'filled'` | The visual style variant of the form control. | | `'standard'` |
| `paddingBottom` | `'dense', 'normal', 'none'` | Controls the bottom padding of the form control. | | `'dense'` |
| `margin` | `'dense', 'normal', 'none'` | Controls the margin of the form control. | | `undefined` |
| `required` | `boolean` | If true, marks the field as required. | | `false` |
| `fullWidth` | `boolean` | If true, the component stretches to the full width available. | | `false` |
| `clearInputs` | `boolean` | Controls input clearing behavior on press. | | `false` |
| `isAutoFillSupported` | `boolean` | Enables native OTP autofill support if available. | | `false` |
| `isAutoFocus` | `boolean` | If true, the first input box automatically receives focus. | | `false` |
| `codeLength` | `number` | The number of digits/input boxes for the code. | | `6` |
| `keyboardType` | `TextInputProps['keyboardType']` | Specifies the type of keyboard to display (e.g., 'numeric'). | | `'numeric'` |

# Password

The `Password` element provides a secure text input field specifically designed for entering passwords. It includes a toggle button to show or hide the entered password for user convenience. It integrates with Formik for form state management.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :------- | :------ |
| `label` | `string` | The label displayed above or alongside the input field. | | `''` |
| `placeholder` | `string` | Placeholder text shown when the input field is empty. | | `''` |
| `required` | `boolean` | Marks the field as mandatory, often visually indicated (e.g., with an asterisk). | | `false` |
| `disabled` | `boolean` | If true, the input field is disabled and cannot be interacted with. | | `false` |
| `variant` | `'standard'`, `'outlined'`, `'filled'`, `'standard-outlined'` | Defines the visual style of the input field (e.g., border, background). | | `'standard'` |
| `margin` | `'none'`, `'dense'`, `'normal'` | Controls the outer spacing around the form control. | | `'normal'` |
| `fullWidth` | `boolean` | If true, the component stretches to the full width of its container. | | `false` |
| `editable` | `boolean` | If false, the text content cannot be modified by the user. | | `true` |
| `returnKeyType` | `ReturnKeyTypeOptions` | Specifies the appearance of the keyboard's return key. | | `'next'` |
| `inputWapperStyle` | `ViewStyle` | Custom styles applied to the wrapper view containing the `TextInput`. | | `undefined` |
| `containerStyle` | `ViewStyle` | Custom styles applied to the outermost container of the component. | | `undefined` |
| `styleLabel` | `ViewStyle` | Custom styles applied specifically to the label text component. | | `undefined` |

# PointConversionAmountReceived

Displays a calculated monetary amount based on a value from another form field, an exchange rate, and a fee percentage. The result is formatted according to a specified currency pattern.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :------- | :------ |
| `label` | `string` | The base label text for the displayed amount (often an i18n key). | Yes | |
| `exchangeRate` | `number` | The numerical exchange rate used for conversion. | Yes | |
| `exchangeRatePattern` | `object` | An object defining the currency formatting rules (e.g., separators, precision). | Yes | |
| `feePercentage` | `number` | The fee percentage to be deducted (e.g., 0.05 for 5%). | Yes | |
| `relatedField` | `string` | The name of the form field providing the base value for the calculation. | Yes | |

# PollAnswer

A form element for managing a list of poll answers. Allows users to add, edit, and delete answer options, enforcing minimum/maximum answer counts and character limits per answer.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :------- | :------ |
| `minAnswers` | `number` | Minimum number of answers required. | Yes | *Varies* |
| `maxAnswers` | `number` | Maximum number of answers allowed (0=unlimited). | Yes | *Varies* |
| `maxLength` | `number` | Maximum character length for each answer. | | `undefined` |
| `disabled` | `boolean` | Disables the input fields and add/delete buttons. | | `false` |
| `variant` | `string` | Visual style variant ('standard', 'standard-outlined'). | | `'standard'` |
| `fullWidth` | `boolean` | If the element should occupy the full width. | | `false` |

# PollCloseTime

This element renders a date and time picker input field, specifically configured for selecting the closing time of a poll. It utilizes the underlying `DatePickerField` component.

## Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :------- | :------ |
| `label` | `string` | The text label displayed for the input field. | | `'close_time'` |
| `placeholder` | `string` | Placeholder text shown when the input is empty. | | |
| `description` | `string` | Additional descriptive text displayed below the input field. | | |
| `required` | `boolean` | If true, the field must have a value for form submission. | | `false` |
| `disabled` | `boolean` | If true, the input field is disabled and cannot be interacted with. | | `false` |
| `fullWidth` | `boolean` | If true, the input field spans the full width of its container. | | `false` |
| `margin` | `'dense'`, `'normal'`, `'none'` | Specifies the margin spacing around the field. | | `'normal'` |
| `variant` | `'standard'`, `'outlined'`, `'filled'` | Defines the visual style of the input field. | | `'standard'` |
| `datePickerMode` | `'date'`, `'time'`, `'datetime'` | Determines the type of picker displayed (date, time, or both). | | `'datetime'` |
| `displayFormat` | `string` | The format used to display the selected date and time in the input field. | | `'DD/MM/YYYY - HH:mm'` |
| `minDate` | `string` | The earliest selectable date/time (ISO 8601 format string). | | |
| `maxDate` | `string` | The latest selectable date/time (ISO 8601 format string). | | |
| `time_zone_gmt` | `string` | Timezone identifier (e.g., 'America/New_York') for calculations. | | User's setting |
| `timeFormat` | `12`, `24` | Specifies whether to use 12-hour or 24-hour format in the time picker. | | User's setting |
| `startOfDay` | `boolean` | If true, sets the selected time to the beginning of the day (00:00:00). | | `false` |
| `endOfDay` | `boolean` | If true, sets the selected time to the end of the day (23:59:59). | | `false` |

## Price

Renders a set of price input fields, often used for different currencies or price types. The actual input fields are defined by the `options` prop. This component conditionally renders different implementations based on the API version, but this documentation focuses on the behavior for API version 5.1.8 and later.

For a visual reference, see [Price Gallery](./form-elements/Price.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | |
| `disabled` | `boolean` | | | `false` |
| `findReplace` | `{ find: string \| RegExp, replace: string }` | Defines rules for replacing characters in the input value. | | |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `'normal' \| 'dense' \| 'none'` | | | |
| `maxLength` | `number` | | | |
| `options` | `Array<{ key: string, name: string, required?: boolean, requiredWhen?: object, ... }>` | Defines the individual price inputs (e.g., currencies). Each object requires `key` (label/value key) and `name`. Can include `required`. | Yes | `[]` |
| `paddingBottom` | `string \| number` | | | |
| `required` | `boolean` | | | `false` |
| `variant` | `'standard' \| 'standard-outlined'` | Specifies the visual style of the component. | | `'standard'` |

## Privacy

This element provides a user interface for selecting privacy settings, typically used for controlling who can see a piece of content (e.g., a post). It displays the currently selected privacy option (with an icon and label) and opens a dedicated selector view (`SelectPrivacyView`) when tapped.

For a visual reference, see [Privacy Gallery](./form-elements/Privacy.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | `undefined` |
| `disable_custom` | `boolean` | If `true`, prevents users from selecting custom privacy options. | | `false` |
| `disabled` | `boolean` | | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `'dense' \| 'normal' \| 'none'` | | | `'normal'` |
| `multiple` | `boolean` | If `true`, allows selecting multiple privacy options (currently single). | | `false` |
| `name` | `string` | The unique identifier for the field within the form. | Yes | |
| `options` | `Array<{ label: string, value: string }>` | An array of predefined privacy options available for selection. | Yes | `[]` |
| `paddingBottom` | `'dense' \| 'normal' \| 'none'` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `suboptions` | `SubOptionsShape` | Additional options, often used for custom privacy lists or friend lists. | | `[]` |
| `variant` | `'standard' \| 'outlined' \| 'standard-outlined' \| 'standard-inlined'` | Specifies the visual style of the component. | | `'standard-inlined'` |

## Progress

Renders a progress bar indicating the completion status, typically used within multi-step forms. It calculates progress based on a related field (representing the current step/value) and the total number of steps/value (expected in the form context).

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `undefined` |
| `paddingLeft` | `'none' \| 'dense' \| 'normal'` | Sets the left inner padding of the form control. | | `undefined` |
| `paddingRight` | `'none' \| 'dense' \| 'normal'` | Sets the right inner padding of the form control. | | `undefined` |
| `paddingTop` | `'none' \| 'dense' \| 'normal'` | Sets the top inner padding of the form control. | | `undefined` |
| `relatedField` | `string` | The name of the form field holding the current value (e.g., current step) for progress calculation. | Yes | |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

## question

*Note: This element inherits most props from the base `Text` element.*

For a visual reference, see [Text Gallery](./form-elements/Text.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none'`, `'sentences'`, `'words'`, `'characters'` | Controls how text input is automatically capitalized. | | `'sentences'` |
| `autoCorrect` | `boolean` | Controls whether autocorrection should be enabled. | | `true` |
| `autoFocus` | `boolean` | | | `false` |
| `backgroundColor` | `string` | Sets a custom background color for the input field. | | |
| `clearButtonMode` | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Controls when the standard clear button appears in the text field (iOS only). | | `'never'` |
| `contextualDescription` | `string` | Additional description shown below the input, often used for dynamic info. | | |
| `description` | `string` | | | |
| `disabled` | `boolean` | | | `false` |
| `editable` | `boolean` | If `false`, the text field value cannot be changed. | | `true` |
| `findReplace` | `{ find: string, replace: string }` | Configuration to display a transformed version of the input (e.g., slug). | | |
| `fullWidth` | `boolean` | | | `false` |
| `hasCopy` | `boolean` | If `true`, displays a copy-to-clipboard icon button. | | `false` |
| `hasQRScanner` | `boolean` | If `true`, displays a QR code scanner icon button. | | `false` |
| `keyboardType` | `string` | Specifies the type of keyboard to display (e.g., 'numeric', 'email-address'). | | `'default'` |
| `label` | `string` | | | |
| `margin` | `'normal'`, `'dense'`, `'none'` etc. | | | `'normal'` |
| `maxLength` | `number` | | | |
| `minHeight` | `number` | | | |
| `multiline` | `boolean` | If `true`, allows multiple lines of text input. | | `false` |
| `paddingBottom` | `'normal'`, `'dense'`, `'none'` etc. | | | |
| `placeholder` | `string` | | | |
| `qrScannerParamName` | `string` | The URL query parameter name to extract when using the QR scanner. | | `'invite_code'` |
| `required` | `boolean` | | | `false` |
| `returnKeyType` | `string` | Specifies the appearance of the return key (e.g., 'done', 'next'). | | `'done'` |
| `secureTextEntry` | `boolean` | If `true`, masks the text entered (for passwords). | | `false` |
| `validateAction` | `string` | Name of a resource action used for asynchronous backend validation on blur. | | |
| `variant` | `'standard'`, `'outlined'`, `'filled'`, `'livestream'` etc. | Specifies the visual style of the component. | | `'standard'` |

## QuizQuestion

A form element for creating and managing a list of quiz questions, each with multiple answers and a designated correct answer. Users can add/remove questions and answers within specified limits.

For a visual reference, see [QuizQuestion Gallery](./form-elements/QuizQuestion.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `defaultAnswers` | `number` | The default number of answer fields to show when adding a new question. | | `2` |
| `disabled` | `boolean` | | | `false` |
| `fullWidth` | `boolean` | | | `true` |
| `label` | `string` | | Yes | |
| `margin` | `'normal'`, `'dense'`, `'none'` | | | `'normal'` |
| `maxAnswerLength` | `number` | The maximum character length allowed for each answer text. | | `undefined` |
| `maxAnswers` | `number` | The maximum number of answers allowed per question. | | `20` |
| `maxLength` | `number` | | | `undefined` |
| `maxQuestions` | `number` | The maximum number of questions allowed. | | `10` |
| `minAnswers` | `number` | The minimum number of answers required per question. | | `2` |
| `minQuestions` | `number` | The minimum number of questions required. | | `1` |
| `paddingBottom` | `'normal'`, `'dense'`, `'none'` | | | `'normal'` |
| `required` | `boolean` | | | `false` |

## RadioGroup

A form element that displays a group of radio buttons, allowing the user to select a single option.

For a visual reference, see [RadioGroup Gallery](./form-elements/RadioGroup.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | `''` |
| `initialValue` | `string` | The initial value/selection for the radio group. | | `''` |
| `label` | `string` | | Yes | |
| `options` | `Array<{label: string, value: any, description?: string}>` | An array of objects defining each radio button. Each object needs `label` and `value`. `description` is optional. | Yes | `[]` |
| `order` | `number` | Optional number to prefix the label for ordering. | | |
| `required` | `boolean` | | | `false` |

## RadioLabelGroup

Renders a group of radio buttons, visually styled using circular icons, allowing the user to select only one option from a list. This element is typically used for membership questions or similar single-choice scenarios within a form.

For a visual reference, see [RadioLabelGroup Gallery](./form-elements/RadioLabelGroup.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `disabled` | `boolean` | | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `hasFormOrder` | `boolean` | If `true`, prepends the `order` number to the `label`. | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `'normal' \| 'dense' \| 'none' \| string` | | | `'normal'` |
| `options` | `Array<{ value: string, label?: string, disable?: boolean }>` | An array of objects defining each radio option. `value` is required, `label` and `disable` are optional. | Yes | `[]` |
| `order` | `number` | The numerical order to display before the label when `hasFormOrder` is `true`. | | |
| `paddingBottom` | `string` | | | |
| `required` | `boolean` | | | `false` |

## Range

A form element that renders a dual-handle slider, allowing users to select a range of values. It uses two separate field names (defined in `min.name` and `max.name` props) to store the selected minimum and maximum values in the form state.

For a visual reference, see [Range Gallery](./form-elements/Range.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `max` | `object { label: string, name: string, value: number }` | Config for the maximum value handle. `name` is the formik field name, `value` is the slider maximum limit. | Yes | |
| `min` | `object { label: string, name: string, value: number }` | Config for the minimum value handle. `name` is the formik field name, `value` is the slider minimum limit. | Yes | |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | |
| `required` | `boolean` | | | `false` |
| `step` | `number` | The granularity that the slider can step through values. | Yes | |

## ResetSearch

This element renders a button used within a search or filter form. When clicked, it resets the values of specified form fields (`targetFields`) back to their initial state as defined in the form's `initialValues`. The button is automatically hidden if the target fields currently hold their default values.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `align` | `string` | Alignment setting (specific usage may vary). | | `'right'` |
| `label` | `string` | | | `'reset'` |
| `targetFields` | `string[]` | An array of field names within the form that this component should reset. | | `['sort', 'when', 'category_id']` |
| `title` | `string` | A title associated with the element (specific usage may vary). | | `'filter'` |
| `variant` | `string` | Specifies the visual style of the component. | | `'standard'` |

## Row

Renders child form elements horizontally in a row, allowing control over their alignment.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `elements` | `Record<string, FormElementConfig>` | Configuration for child form elements to render within the row | Yes | |
| `justifyContent` | `'space-between' \| 'flex-start' \| 'flex-end' \| 'center' \| 'space-around' \| 'space-evenly'` | Specifies the alignment of child elements along the main axis. | | `'space-between'` |
| `style` | `ViewStyle` | Custom styles applied to the row container. | | |

## Select

The `Select` form element provides a dropdown or list interface for users to choose one or multiple options from a predefined set. It supports various configurations like search, multiple selections, and different visual styles.

For a visual reference, see [Select Gallery](./form-elements/Select.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `choice_type` | `string` | Specifies the type of choice control (e.g., 'radio', 'checkbox'). | | `undefined` |
| `description` | `string` | | | `undefined` |
| `disableClearable` | `boolean` | If `true`, prevents the user from clearing the selected value. | | `false` |
| `disable_custom` | `boolean` | If `true`, disables the ability to add custom options (if applicable). | | `false` |
| `disabled` | `boolean` | | | `false` |
| `enable_search` | `boolean` | If `true`, enables a search input within the options list. | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `multiple` | `boolean` | If `true`, allows selecting multiple options. | | `false` |
| `options` | `OptionsItemShape[]` | An array of available options for the select field. | Yes | `[]` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `placeholder` | `string` | | | `'select'` |
| `required` | `boolean` | | | `false` |
| `resetValue` | `boolean` | If `true`, indicates the value should be reset under certain conditions. | | `false` |
| `showWithoutOptions` | `boolean` | If `true`, renders the field even if the `options` array is empty. | | `false` |
| `suboptions` | `SubOptionsShape` | Additional options grouped under main options (e.g., for dependent selects). | | `undefined` |
| `useSectionList` | `boolean` | If `true`, uses a SectionList to display options (requires specific data structure). | | `false` |
| `value_type` | `string` | Specifies the type of value to store (e.g., 'array'). | | `undefined` |
| `variant` | `'standard' \| 'outlined' \| 'standard-outlined' \| 'standard-inlined'` | Specifies the visual style of the component. | | `'standard'` |

## SelectSubForm

This element renders a touchable area displaying an icon and the label of the currently selected option. Tapping it opens a bottom sheet containing a sub-form where the user can select one or multiple options from a predefined list (`options` and `suboptions`).

### Props

The component accepts standard `FormFieldProps` (`name`, `disabled`, `formik`) and a `config` object with the following properties:

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `choice_type` | `string` | Defines the selection mechanism in the sub-form (e.g., 'radio', 'checkbox'). | | `undefined` |
| `disable_custom` | `boolean` | If true, disables the ability to add custom options in the sub-form. | | `false` |
| `disable_uncheck` | `boolean` | If true, prevents users from deselecting an already selected option. | | `false` |
| `enable_search` | `boolean` | If true, enables a search input within the sub-form. | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `icon` | `string` | The name of the Lineficon icon to display next to the selected value. | Yes | `''` |
| `initialValue` | `any` | The initial value of the form field. | | `undefined` |
| `label` | `string` | | | `''` |
| `margin` | `'dense' \| 'normal' \| 'none'` | | | `'normal'` |
| `multiple` | `boolean` | If true, allows multiple options to be selected in the sub-form. | | `false` |
| `options` | `OptionsItemShape[]` | An array of primary options to be displayed in the sub-form. | Yes | `[]` |
| `paddingBottom` | `'dense' \| 'normal' \| 'none'` | | | `undefined` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `showWithoutOptions` | `boolean` | If true, the element is rendered even when no `options` are provided. | | `false` |
| `suboptions` | `SubOptionsShape` | An object containing secondary options, often dependent on the primary selection. | | `undefined` |
| `useSectionList` | `boolean` | If true, the sub-form uses a `SectionList` for displaying options, suitable for grouped data. | | `false` |
| `value_type` | `string` | Specifies the data type of the value (e.g., 'string', 'number'). | | `undefined` |
| `variant` | `'standard' \| 'outlined' \| ...` | Specifies the visual style of the component. | | `'standard'` |

## SFAutocomplete

The `SFAutocomplete` element provides an autocomplete input field, allowing users to search and select one or multiple options from a predefined list or dynamically fetched data source. It opens a bottom sheet for option selection.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `canLoadMore` | `boolean` | Whether more options can be loaded (pagination) from the search endpoint. | | `false` |
| `disable_uncheck` | `boolean` | Prevent unselecting the current value (makes selection required if a value exists). | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | | `''` |
| `labelKey` | `string` | Key to use for the option's display label. | | `'name'` |
| `margin` | `normal`, `dense`, `none` | | | `normal` |
| `multiple` | `boolean` | Allow multiple selections. | | `false` |
| `option_default` | `Array<any>` | Default options to use if `useOptionContext` is true and no context value exists. | | `[]` |
| `options` | `OptionsItemShape[]` | Predefined options list (used if `search_endpoint` is not provided). | | `[]` |
| `paddingBottom` | `normal`, `dense`, `none` | | | `normal` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `search_endpoint` | `string` | API endpoint URL to fetch options dynamically. | | `undefined` |
| `search_params` | `object` | Additional parameters for the search API endpoint. | | `{}` |
| `useOptionContext` | `boolean` | Whether to use a shared option context for managing selected options. | | `false` |
| `valueKey` | `string` | Key to use for the option's value. | | `'id'` |
| `variant` | `standard`, `outlined` | Specifies the visual style of the component. | | `standard` |

## SFDate

A form element that allows users to select a date, time, or both using a native modal picker. It displays the selected value in a specified format.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `datePickerMode` | `'date' \| 'time' \| 'datetime'` | Determines if the picker allows selecting date, time, or both. | | `'datetime'` |
| `displayFormat` | `string` | The Moment.js format string for displaying the selected value in the input field. | | `'DD/MM/YYYY - HH:mm'` |
| `editable` | `boolean` | If `false`, the text input part is not directly editable (picker still works). | | `true` |
| `endOfDay` | `boolean` | If true, sets the selected date's time to the end of the day (23:59:59). | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `string` | The initial value for the date picker (ISO 8601 format). | | `undefined` |
| `label` | `string` | | | `'close_time'` |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `maxDate` | `string` | The maximum selectable date/time (ISO 8601 format or format specified by `momentResultFormat`). | | `undefined` |
| `minDate` | `string` | The minimum selectable date/time (ISO 8601 format or format specified by `momentResultFormat`). | | `undefined` |
| `momentResultFormat` | `string` | The Moment.js format string used for parsing `minDate` and `maxDate`. | | `undefined` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `'none'` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `startOfDay` | `boolean` | If true, sets the selected date's time to the start of the day (00:00:00). | | `false` |
| `time_zone_gmt` | `string` | The GMT timezone string (e.g., 'Asia/Ho_Chi_Minh') for date calculations. | | `undefined` |
| `timeFormat` | `12 \| 24` | Specifies 12 or 24-hour time format for the time picker. | | `12` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

## SFDatetime

A form input element that allows users to select a date, time, or both using a native modal picker. It displays the selected value in a formatted text input. This element is an alias for `SFDate` but typically configured with `datePickerMode: 'datetime'`.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `datePickerMode` | `'date'\|'time'\|'datetime'` | Determines if the picker selects date, time, or both. | Yes | `'datetime'` |
| `disabled` | `boolean` | | | `false` |
| `displayFormat` | `string` | Moment.js format for displaying the selected date/time in the input. | Yes | `'DD/MM/YYYY - HH:mm'` |
| `editable` | `boolean` | If false, prevents direct text input, forcing picker use. | | `true` |
| `endOfDay` | `boolean` | Set selected date's value to the end of the day (23:59:59). | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | `'close_time'` |
| `margin` | `'none'\|'dense'\|'normal'` | | Yes | `'normal'` |
| `maxDate` | `string` | Maximum selectable date (ISO 8601 format). | | |
| `minDate` | `string` | Minimum selectable date (ISO 8601 format). | | |
| `placeholder` | `string` | | Yes | |
| `required` | `boolean` | | Yes | `false` |
| `startOfDay` | `boolean` | Set selected date's value to the start of the day (00:00:00). | | `false` |
| `time_zone_gmt` | `string` | IANA time zone name (e.g., 'Asia/Saigon') for date calculations. Defaults to device timezone if omitted. | Yes | Device Timezone |
| `timeFormat` | `12 \| 24` | Use 12-hour or 24-hour format in the time picker. | | System Default |
| `variant` | `'standard'\|'outlined'\|...` | Specifies the visual style of the component. | Yes | `'standard'` |

## SFFilterButton

This form element renders a button, typically represented by an icon. When pressed, it opens a bottom sheet containing a sub-form (`ui.SubFormBuilder`) based on the main form's schema. This allows users to configure and apply filter criteria, which are then reflected in the main form's values upon submission of the sub-form.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `choice_type` | `string` | Defines the selection mechanism (e.g., 'radio', 'checkbox'). | | `undefined` |
| `disable_custom` | `boolean` | If `true`, disables custom value input in the filter form. | | `false` |
| `disable_uncheck` | `boolean` | If `true`, prevents users from unselecting an already selected option. | | `false` |
| `enable_search` | `boolean` | If `true`, enables a search input within the filter form options. | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `OptionsItemShape[]` | Default selected values for the filter options. | | `undefined` |
| `label` | `string` | | | `''` |
| `margin` | `keyof typeof SizeEnum` | | | `undefined` |
| `multiple` | `boolean` | If `true`, allows multiple selections in the filter form. | | `false` |
| `options` | `OptionsItemShape[]` | The list of available options to display in the filter form. | | `[]` |
| `paddingBottom` | `keyof typeof SizeEnum` | | | `undefined` |
| `placeholder` | `string` | | | `''` |
| `required` | `boolean` | | | `false` |
| `showWithoutOptions` | `boolean` | If `true`, the button is shown even when there are no `config.options`. | | `false` |
| `suboptions` | `SubOptionsShape` | Configuration for sub-options within the filter form. | | `undefined` |
| `useSectionList` | `boolean` | If `true`, uses a `SectionList` component to render options in the filter form. | | `false` |
| `value_type` | `string` | Specifies the expected data type of the filter value. | | `undefined` |
| `variant` | `keyof typeof Variant` | Specifies the visual style of the component. | | `'standard'` |

## SFFilterForm

Renders a button that opens a bottom sheet containing a sub-form, typically used for applying filters within a larger form. Pressing the button navigates to a dedicated screen (`FORM_BOTTOM_SHEET`) where the filter options, defined by the `options` and `suboptions` props, are presented.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `choice_type` | `string` | Specifies the type of choice input used in the sub-form (e.g., 'checkbox'). | | `undefined` |
| `disable_custom` | `boolean` | Disables custom options in the sub-form. | | `false` |
| `disable_uncheck` | `boolean` | Prevents unselecting options once selected in the sub-form. | | `false` |
| `enable_search` | `boolean` | Enables a search input within the sub-form. | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `OptionsItemShape[]` | Initial values for the filter options within the sub-form. | | `undefined` |
| `label` | `string` | | | `undefined` |
| `margin` | `normal` \| `dense` \| `none` | | | `normal` |
| `multiple` | `boolean` | Allows multiple selections in the sub-form. | | `false` |
| `options` | `OptionsItemShape[]` | The list of options to display within the sub-form. | Yes | `[]` |
| `paddingBottom` | `normal` \| `dense` \| `none` | | | `normal` |
| `placeholder` | `string` | | | `undefined` |
| `showWithoutOptions` | `boolean` | Determines if the filter button should be shown even when no options exist. | | `false` |
| `suboptions` | `SubOptionsShape` | Configuration for the sub-form displayed in the bottom sheet. | Yes | `undefined` |
| `useSectionList` | `boolean` | Uses a `SectionList` for displaying options in the sub-form if true. | | `false` |
| `value_type` | `string` | Specifies the expected data type of the selected value(s) in the sub-form. | | `undefined` |
| `variant` | `standard` \| `outlined` \| `filled` | Specifies the visual style of the component. | | `standard` |

## SFFilterPrice

The `SFFilterPrice` element provides a form input for selecting a price range (minimum and maximum). It displays the selected range and opens a bottom sheet for users to enter or modify the 'from' and 'to' price values.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `enable_search` | `boolean` | Configuration passed to the bottom sheet component (FilterPriceField). | | `false` |
| `findReplace` | `any` | Configuration passed to the bottom sheet component (FilterPriceField). | | |
| `fromFieldLabel` | `string` | Label for the minimum price input in the bottom sheet. | | |
| `fromFieldName` | `string` | The formik field name for the minimum price value. | | `'price_from'` |
| `fromFieldPlaceholder` | `string` | Placeholder text for the minimum price input in the bottom sheet. | | |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `string` | | | |
| `paddingBottom` | `string` | | | |
| `required` | `boolean` | | | `false` |
| `toFieldLabel` | `string` | Label for the maximum price input in the bottom sheet. | | |
| `toFieldName` | `string` | The formik field name for the maximum price value. | | `'price_to'` |
| `toFieldPlaceholder` | `string` | Placeholder text for the maximum price input in the bottom sheet. | | |
| `variant` | `string` | Specifies the visual style of the component. | | `'standard'` |

## SFScrollView

A form element that renders its child elements within a horizontal ScrollView. It allows users to scroll horizontally through a set of form inputs or components.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `elements` | `Record<string, ElementConfig>` | Defines the child form elements to render within the scroll view. | Yes | |
| `paddingBottom` | `string` | | | `paddingBase` |

## SFSearchBox

The `SFSearchBox` component renders a search input field integrated directly into the screen's header navigation bar. It automatically handles focus, clearing, and debounced value updates for form submission.

*Note: This element is only used in a search form.*

### Props

The component accepts standard `FormFieldProps` (`name`, `config`, `disabled`, `formik`). The primary configuration is done via the `config` object:

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none' \| 'sentences' \| 'words' \| 'characters'` | Auto-capitalization behavior. | | `'none'` |
| `autoCorrect` | `boolean` | Enable/disable auto-correction. | | `false` |
| `autoFocus` | `boolean` | | | `true` if empty |
| `clearButtonMode` | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | How the clear button behaves (iOS only). | | `undefined` |
| `description` | `string` | | | `undefined` |
| `editable` | `boolean` | If the input is editable. | | `true` |
| `fullWidth` | `boolean` | | | `false` |
| `margin` | `keyof typeof SizeEnum` | | | `undefined` |
| `maxLength` | `number` | | | `undefined` |
| `minHeight` | `number` | | | `undefined` |
| `multipleline` | `boolean` | If the input allows multiple lines. | | `false` |
| `paddingBottom` | `keyof typeof SizeEnum` | | | `undefined` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `showSearchIcon` | `boolean` | Whether to show the search icon. | | `true` |
| `variant` | `keyof typeof Variant` | Specifies the visual style of the component. | | `undefined` |

## SFSelect

The `SFSelect` element provides a dropdown-like selection interface, typically opening a bottom sheet for users to choose one or multiple options from a list. It supports features like search, sections, and conditional options based on other fields.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoSubmit` | `boolean` | Submits the form automatically on value change. | | `false` |
| `choice_type` | `string` | Type of choice mechanism (used internally, e.g., 'radio', 'checkbox'). | | `undefined` |
| `disableClearable` | `boolean` | Prevents clearing/unselecting the chosen option(s). | | `false` |
| `disable_custom` | `boolean` | Disables custom privacy options if applicable. | | `false` |
| `enable_search` | `boolean` | Enables searching within the options list in the bottom sheet. | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `OptionsItemShape[]` | Initial selected value(s). | | `undefined` |
| `label` | `string` | | Yes | `undefined` |
| `margin` | `'dense' \| 'normal' \| 'none'` | | | `'normal'` |
| `multiple` | `boolean` | Allows multiple selections if true. | | `false` |
| `optionRelatedMapping` | `Record<string, OptionsItemShape[]>` | Mapping object for options based on the `relatedFieldName`'s value. | | `undefined` |
| `options` | `OptionsItemShape[]` | The list of selectable options. | Yes | `[]` |
| `paddingBottom` | `'dense' \| 'normal' \| 'none'` | | | `'normal'` |
| `placeholder` | `string` | | | `undefined` |
| `relatedFieldName` | `string` | Name of a related form field for conditional logic (e.g., filtering options). | | `undefined` |
| `required` | `boolean` | | | `false` |
| `resetValue` | `boolean` | Resets the value under certain conditions (used internally). | | `false` |
| `showWithoutOptions` | `boolean` | Renders the component even if no `options` are provided. | | `false` |
| `suboptions` | `SubOptionsShape` | Additional options grouped under main options. | | `undefined` |
| `useSectionList` | `boolean` | Uses a SectionList for displaying options in the bottom sheet if true. | | `false` |
| `value_type` | `string` | Specifies the type of value expected (e.g., 'string', 'number'). | | `undefined` |
| `variant` | `'standard' \| 'outlined' \| etc.` | Specifies the visual style of the component. | | `'standard'` |

## SFSwitch

A form element that renders a switch (toggle) control. It allows users to select between two states, typically representing on/off or true/false.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `checkedValue` | `boolean \| number` | The value assigned to the field when the switch is checked (on). | | `1` |
| `description` | `string` | | | `''` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `'dense' \| 'normal' \| 'none'` | | | `normal` |
| `paddingBottom` | `'dense' \| 'normal' \| 'none'` | | | `normal` |
| `required` | `boolean` | | | `false` |
| `uncheckedValue` | `boolean \| number` | The value assigned to the field when the switch is unchecked (off). | | `0` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | 'standard-inlined' | Specifies the visual style of the component. | | `'standard-inlined'` |

## SFTabSelect

A form element that renders a horizontal list of tabs, allowing the user to select one option. The selected value is stored in the form state.

*Note: This element is only used in a search form.*

### Props

Props are passed via the `config` object within the form definition.

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `bounces` | `boolean` | Determines if the horizontal tab list bounces when scrolled to the end. | | `false` |
| `options` | `Array<{ label: string, value: any, showWhen?: Record<string, any> }>` | An array of objects defining the tabs. Each object should have a `label` (display text) and a `value`. Can include `showWhen` conditions. | Yes | `[]` |

## SFText

The `SFText` element renders a standard text input field within a form. It supports various configurations like multiline input, validation, QR code scanning, and copy-to-clipboard functionality.

*Note: This element is only used in a search form.*

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none'`, `'sentences'`, `'words'`, `'characters'` | Controls automatic capitalization. | | `'sentences'` |
| `autoCorrect` | `boolean` | Enables auto-correction. | | `true` |
| `autoFocus` | `boolean` | | | `false` |
| `backgroundColor` | `string` | Sets the background color of the input. | | `undefined` |
| `clearButtonMode` | `'never'`, `'while-editing'`, `'unless-editing'`, `'always'` | Controls the visibility of the clear button (iOS only). | | `'never'` |
| `contextualDescription` | `string` | Additional description text. | | `undefined` |
| `description` | `string` | | | `undefined` |
| `disabled` | `boolean` | | | `false` |
| `editable` | `boolean` | If `false`, the text is not editable. | | `true` |
| `findReplace` | `{ find: string, replace: string }` | Defines find/replace rules for generating a slug displayed below the input. | | `undefined` |
| `fullWidth` | `boolean` | | | `false` |
| `hasCopy` | `boolean` | Adds a copy-to-clipboard icon/button. | | `false` |
| `hasQRScanner` | `boolean` | Adds a QR code scanner icon/button. | | `false` |
| `label` | `string` | | | `undefined` |
| `margin` | `'none'`, `'dense'`, `'normal'` | | | `'normal'` |
| `maxLength` | `number` | | | `undefined` |
| `minHeight` | `number` | | | `undefined` |
| `multiline` | `boolean` | Allows multiple lines of text input. | | `false` |
| `order` | `number` | Order of the element in the form. | | `undefined` |
| `paddingBottom` | `'none'`, `'dense'`, `'normal'` | | | `'normal'` |
| `placeholder` | `string` | | | `undefined` |
| `qrScannerParamName` | `string` | Query parameter name to extract from the scanned QR code URL. | | `'invite_code'` |
| `required` | `boolean` | | | `false` |
| `validateAction` | `string` | Action name for backend validation on blur. | | `undefined` |
| `variant` | `'standard'`, `'outlined'`, `'filled'`, `'standard-outlined'`, `'livestream'` | Specifies the visual style of the component. | | `'standard'` |

## SimpleFriendPicker

A form element that allows users to select one or multiple friends from a searchable list. It displays selected friends as chips and provides an interface to browse and search all available friends fetched via API.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `OptionsItemShape[]` | An array of initially selected friend objects. | | `[]` |
| `label` | `string` | | | `''` |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `multiple` | `boolean` | If `true`, allows selecting multiple friends. | | `false` |
| `onFocus` | `(event: any) => void` | Callback function triggered when the input focuses. | | `undefined` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `undefined` |
| `placeholder` | `string` | | | `'Search friends by their name'` |
| `required` | `boolean` | | | `false` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

## SingleVideoFile

This form element allows users to select a single video, either by uploading a file directly or by providing a URL (depending on the `file_type` configuration). It displays a preview of the selected video and handles file size validation.

For a visual reference, see [SingleVideoFile Gallery](./form-elements/SingleVideoFile.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `allow_upload` | `boolean` | Controls if direct video upload is allowed (used when `file_type` is not 'link'). | | `true` |
| `extraProps` | `object` | Additional props, often containing context like `module_name` and `resource_name` for validation URLs. | | `{}` |
| `fetchEndpoint` | `string` | Optional endpoint for fetching video details when `file_type` is 'link'. | | |
| `file_type` | `'video' \| 'link'` | Specifies whether to handle a direct video upload ('video') or a video URL ('link'). | Yes | |
| `fullWidth` | `boolean` | | | `false` |
| `item_type` | `string` | Specifies the type of item being uploaded (e.g., 'video'). | Yes | |
| `label` | `string` | | | |
| `margin` | `'normal' \| 'dense' \| 'none'` | | | `'normal'` |
| `max_upload_filesize` | `number \| { video: number, photo: number }` | Maximum allowed file size in bytes. Can be an object with different limits for video/photo. | Yes | |
| `paddingBottom` | `'normal' \| 'dense' \| 'none'` | | | `'normal'` |
| `required` | `boolean` | | | `false` |
| `storage_id` | `number \| null` | Optional ID for a specific storage service. | | `null` |
| `upload_url` | `string` | The endpoint URL for uploading the file. | Yes | |

## Slider

A form element that allows users to select a value from a specified range by sliding a handle along a track.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `fullWidth` | `boolean` | | | `false` |
| `inline` | `boolean` | (Part of Config type, but not directly used in this component's logic) | | `false` |
| `label` | `string` | | Yes | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `maximumValue` | `number` | The maximum value of the slider. | | `undefined` |
| `meta` | `MetaShape` | Additional metadata for the field. | | `undefined` |
| `minimumValue` | `number` | The minimum value of the slider. | | `undefined` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `step` | `number` | The granularity with which the slider can step through values. | | `undefined` |
| `variant` | `keyof typeof Variant` | Specifies the visual style of the component. | | `'standard-inlined'` |

## SocialButtons

This element renders a container for multiple social login buttons. It dynamically adjusts the layout based on the number of buttons: displaying them in a row if there are more than two, and stacked vertically otherwise. It also handles platform-specific visibility, hiding the Apple login button on Android devices.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `elements` | `Record<string, any>` | Configuration objects for each individual social button element. | Yes | |
| `totalButton` | `number` | The total count of configured social buttons, used to determine layout. | Yes | |

## SpamQuestion

This element renders a text input field, often accompanied by an image, designed to present a question to the user to prevent spam submissions.

For a visual reference, see [SpamQuestion Gallery](./form-elements/SpamQuestion.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `clearButtonMode` | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | Controls when the clear text button appears in the input field (iOS only). | | `undefined` |
| `disabled` | `boolean` | | | `false` |
| `editable` | `boolean` | Determines if the text input field can be edited by the user. | | `true` |
| `fullWidth` | `boolean` | | | `false` |
| `imageUri` | `string` | The URI for the image associated with the spam question. | Yes | |
| `label` | `string` | | | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `undefined` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `undefined` |
| `placeholder` | `string` | | | |
| `required` | `boolean` | | | `false` |
| `variant` | `'standard' \| 'outlined' \| 'standard-inlined'` | Specifies the visual style of the component. | | `'standard-inlined'` |

## SponsorCalculatorCost

This form element provides a numeric input field that calculates and displays a total cost based on the entered value, an initial unit count, and a price per unit. It's typically used for scenarios like calculating sponsorship costs based on impressions or days.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | |
| `disabled` | `boolean` | | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `initialPrice` | `number` | The price per `initialUnit`. | Yes | |
| `initialUnit` | `number` | The base unit used for the cost calculation (e.g., number of impressions). | Yes | |
| `label` | `string` | | | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `maxLength` | `number` | | | |
| `placeholder` | `string` | | | |
| `pricePattern` | `object` | An object defining the currency format (`symbol`, `currency_code`, etc.). | Yes | |
| `required` | `boolean` | | | `false` |
| `totalNameLabel` | `string` | The translation key for the label prefix before the calculated total cost. | | `'total_cost'` |
| `variant` | `'standard' \| 'outlined' \| 'standard-outlined'` | Specifies the visual style of the component. | | `'standard'` |

## StepButton

A button element designed for multi-step forms, allowing navigation between steps (previous/next) or form submission. It interacts with a form field (specified by `currentStepName` or defaulting to `_current_step`) to manage the active step.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `actionType` | `'previous' \| 'next' \| 'submit'` | Determines the button's behavior (navigate previous, next, or submit). | Yes | `undefined` |
| `currentStepName` | `string` | The name of the form field tracking the current step index. | | `FormStepVariable.CURRENT_KEY` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | `''` |
| `margin` | `'small' \| 'medium' \| 'large' \| 'none'` | | | `undefined` |
| `paddingBottom` | `'small' \| 'medium' \| 'large' \| 'none'` | | | `undefined` |
| `style` | `ViewStyle` | Custom styling applied to the surrounding form control. | | `undefined` |
| `variant` | `'standard' \| 'outlined'` | Specifies the visual style of the component. | | `'standard'` |

## Submit

A button element used to trigger form submission. It integrates with Formik to handle the submit action and can be configured with various visual styles and behaviors.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `color` | `'primary' \| 'secondary' \| 'error' \| 'warning' \| 'info' \| 'success' \| 'inherit' \| string` | The color of the button. Defaults to 'gray' when disabled. | | `'primary'` |
| `customAction` | `{ type: string; payload?: any }` | Dispatches a custom Redux action when the button is clicked after submitting the form. | | |
| `disableWhenClean` | `boolean` | If true, the button is disabled when the form is pristine (no changes made). | | `false` |
| `disabled` | `boolean` | | | `false` |
| `first` | `boolean` | Style adjustment if it's the first element in a group. | | `false` |
| `fontWeight` | `'light' \| 'regular' \| 'medium' \| 'bold'` | The font weight of the button text. | | |
| `fullWidth` | `boolean` | | | `false` |
| `icon` | `string` | Name of the icon to display on the button. | | |
| `label` | `string` | | Yes | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `outline` | `boolean` | Applies an outline style to the button. | | `false` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `round` | `boolean` | If true, makes the button round (intended for icon buttons). | | `false` |
| `size` | `'small' \| 'medium' \| 'large' \| 'string'` | The size of the button. Note: The component internally uses 'normal'. | | `'medium'` |
| `style` | `object` | Custom styles to apply to the FormControl container. | | |
| `textTransform` | `'none' \| 'capitalize' \| 'uppercase' \| 'lowercase'` | Controls the text transformation (e.g., uppercase). | | |
| `transparent` | `boolean` | Makes the button background transparent. | | `false` |
| `variant` | `'standard' \| 'outlined' \| 'contained'` | Specifies the visual style of the component. | | `'standard'` |

## SubmitHeader

This element renders a submit button, typically placed within a form's header area, wrapped in a `FormControl` for layout control. Clicking the button triggers the form submission process.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `color` | `string` | Button color (e.g., 'primary', 'secondary'). | | |
| `fontWeight` | `string` | Button text font weight. | | |
| `fullWidth` | `boolean` | | | `false` |
| `icon` | `string` | Icon name to display on the button. | | |
| `label` | `string` | | Yes | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | |
| `outline` | `boolean` | Applies an outline style to the button. | | `false` |
| `paddingBottom` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `size` | `'small' \| 'medium' \| 'large'` | Button size. | | |
| `textTransform` | `string` | Button text transformation (e.g., 'uppercase'). | | |
| `transparent` | `boolean` | Makes the button background transparent. | | `false` |
| `variant` | `'standard' \| 'outlined' \| 'filled'` | Specifies the visual style of the component. | | `'standard'` |

## Switch

A form element that renders a toggle switch input, allowing users to select between two states (on/off).

For a visual reference, see [Switch Gallery](./form-elements/Switch.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `checkedValue` | `any` | The value submitted when the switch is turned on. | | `1` |
| `description` | `string` | | | `''` |
| `disabled` | `boolean` | | | `false` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | Yes | `undefined` |
| `margin` | `'none'\|'normal'\|'dense'` | | | `'normal'` |
| `required` | `boolean` | | | `false` |
| `uncheckedValue` | `any` | The value submitted when the switch is turned off. | | `0` |

## Tags

A form element that allows users to input and manage a list of tags. Users can type tags and press Enter/Done to add them. Existing tags can be removed by clicking the close icon on the tag.

For a visual reference, see [Tags Gallery](./form-elements/Tags.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `clearButtonMode` | `string` | Determines the visibility of the clear button (standard TextInput prop). | | |
| `description` | `string` | | | |
| `editable` | `boolean` | If false, the input cannot be edited (standard TextInput prop). | | `true` |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | | |
| `margin` | `'normal' \| 'dense' \| 'none'` | | | |
| `paddingBottom` | `'normal' \| 'dense' \| 'none'` | | | `'normal'` |
| `placeholder` | `string` | | | `'enter text'` |
| `required` | `boolean` | | | `false` |
| `variant` | `'standard' \| 'outlined' \| 'outlined-inlined' \| 'standard-outlined' \| 'standard-inlined'` | Specifies the visual style of the component. | | `'standard'` |

## Text

A standard text input field for forms, allowing users to enter single or multiple lines of text.

For a visual reference, see [Text Gallery](./form-elements/Text.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none' \| 'sentences' \| 'words' \| 'characters'` | Controls automatic capitalization behavior. | | `'sentences'` |
| `autoCorrect` | `boolean` | Enables or disables auto-correction for the input. | | `true` |
| `autoFocus` | `boolean` | | | `false` |
| `backgroundColor` | `string` | Sets the background color for the input wrapper. | | |
| `clearButtonMode` | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | (iOS only) When to display the clear text button. | | `'never'` |
| `contextualDescription` | `string` | Additional descriptive text displayed near the input. | | |
| `description` | `string` | | | |
| `editable` | `boolean` | If `false`, the text input is not editable. | | `true` |
| `findReplace` | `{ find: string, replace: string }` | Configuration to automatically generate a slug-like value based on input. | | |
| `fullWidth` | `boolean` | | | `false` |
| `hasCopy` | `boolean` | If `true`, displays a copy-to-clipboard icon button. | | `false` |
| `hasQRScanner` | `boolean` | If `true`, displays a QR code scanner icon button. | | `false` |
| `label` | `string` | | | |
| `margin` | `'none' \| 'normal' \| 'dense'` | | | `'normal'` |
| `maxLength` | `number` | | | |
| `minHeight` | `number` | | | |
| `multipleline` | `boolean` | If `true`, allows multiple lines of text input (textarea). | | `false` |
| `placeholder` | `string` | | | |
| `qrScannerParamName` | `string` | Query parameter name to extract from the scanned QR code URL. | | `'invite_code'` |
| `required` | `boolean` | | | `false` |
| `validateAction` | `string` | Name of a registered action for backend validation triggered on blur. | | |
| `variant` | `'standard' \| 'standard-inlined' \| 'standard-outlined' \| 'outlined'` | Specifies the visual style of the component. | | `'standard'` |

## Textarea

Provides a multi-line text input field for forms.

For a visual reference, see [Textarea Gallery](./form-elements/Textarea.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `autoCapitalize` | `'none' \| 'sentences' \| 'words' \| 'characters'` | Controls the automatic capitalization behavior of the text input. | | `'none'` |
| `autoCorrect` | `boolean` | Enables or disables autocorrection for the input. | | Platform default |
| `autoFocus` | `boolean` | | | `false` |
| `clearButtonMode` | `'never' \| 'while-editing' \| 'unless-editing' \| 'always'` | (iOS only) Determines when the standard clear text button appears inside the text input. | | `'never'` |
| `contextualDescription` | `string` | Additional description text that might be combined with dynamic content based on the input value. | | |
| `description` | `string` | | | |
| `disabled` | `boolean` | | | `false` |
| `editable` | `boolean` | If false, the text content cannot be modified by the user. | | `true` |
| `findReplace` | `{ find: string, replace: string }` | Defines patterns for find-and-replace operations on the input value, often used for generating derived text. | | |
| `fullWidth` | `boolean` | | | `false` |
| `label` | `string` | | | |
| `margin` | `'none' \| 'normal' \| 'dense'` | | | `'normal'` |
| `maxLength` | `number` | | | |
| `minHeight` | `number` | | | |
| `name` | `string` | The name of the field used in the form state. | Yes | |
| `placeholder` | `string` | | | |
| `required` | `boolean` | | | `false` |
| `variant` | `'standard' \| 'outlined' \| 'standard-outlined'` | Specifies the visual style of the component. | | `'standard'` |

## Time

*Note: This element inherits most props from the base `Date` element.*

For a visual reference, see [Date Gallery](./form-elements/Date.md)

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | `undefined` |
| `disabled` | `boolean` | | | `false` |
| `displayFormat` | `string` | The format used to display the selected time (e.g., 'HH:mm', 'h:mm A'). | | `'HH:mm'` |
| `fullWidth` | `boolean` | | | `false` |
| `initialValue` | `string` | An initial time value for the field (must match resultFormat if specified, otherwise ISO 8601). | | `undefined` |
| `label` | `string` | | Yes | |
| `margin` | `'none' \| 'dense' \| 'normal'` | | | `'normal'` |
| `placeholder` | `string` | | | `undefined` |
| `required` | `boolean` | | | `false` |
| `resultFormat` | `string` | The format the selected time is stored in. Defaults to ISO 8601 format if unset. | | ISO 8601 String |
| `time_zone_gmt` | `string` | Timezone identifier (e.g., 'UTC', 'America/New_York') for display formatting. | | User's current timezone |
| `timeFormat` | `12 \| 24` | Specifies whether to use 12-hour or 24-hour format in the picker. | | Locale default |
| `variant` | `'standard' \| 'outlined' \| 'filled' \| 'standard-outlined'` | Specifies the visual style of the component. | | `'standard'` |

## Typo

Renders styled text content within a form, suitable for labels, descriptions, or simple HTML snippets.

### Props

| Name | Type | Description | Required | Default |
| :--- | :--- | :---------- | :-------- | :------- |
| `description` | `string` | | | `undefined` |
| `label` | `string` | | | `undefined` |
| `numberOfLines` | `number` | Maximum number of lines for the label and description. | | `undefined` |
| `plainText` | `string` | HTML content to render. Takes precedence over label/description if provided. | | `undefined` |
| `style` | `object` | Custom style object for the label. | | `undefined` |

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
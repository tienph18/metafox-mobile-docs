# MultiFile

Allows users to select and upload multiple files (photos, videos, or other types based on configuration). This element is an alias for the `Attachment` element but typically used when multiple file selection is intended.

## Props

| Name                  | Type                                       | Description                                                                 | Required | Default            |
| :-------------------- | :----------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------------- |
| `label`               | `string`                                   | The label text for the field.                                               | Yes      | -                  |
| `description`         | `string`                                   | Additional descriptive text below the label.                                | No       | -                  |
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
| `fullWidth`           | `boolean`                                  | Whether the element should take up the full width.                          | No       | `false`            |
| `margin`              | `'normal' \| 'dense' \| 'none'`            | Margin style.                                                               | No       | `'normal'`         |
| `variant`             | `string`                                   | The display variant of the form control.                                    | No       | `'standard-inlined'` |
| `required`            | `boolean`                                  | Whether the field is required (validation).                                 | No       | `false`            |
| `disabled`            | `boolean`                                  | Disable the form element.                                                   | No       | `false`            |
| `name`                | `string`                                   | The name of the field in the form state.                                    | Yes      | -                  |
| `paddingBottom`       | `string`                                   | Custom padding at the bottom.                                               | No       | -                  |
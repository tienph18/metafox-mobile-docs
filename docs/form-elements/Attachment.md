# Attachment

The Attachment element allows users to upload one or more files (photos, videos, or other types) within a form. It provides options for selecting files from the device library or capturing directly from the camera.

## Props

| Name                  | Type                                       | Description                                                                 | Required | Default            |
| :-------------------- | :----------------------------------------- | :-------------------------------------------------------------------------- | :------- | :----------------- |
| `label`               | `string`                                   | The label displayed above the attachment area.                              | No       |                    |
| `description`         | `string`                                   | Additional descriptive text displayed below the label.                      | No       |                    |
| `required`            | `boolean`                                  | Whether the field is mandatory.                                             | No       | `false`            |
| `disabled`            | `boolean`                                  | Disables the attachment input.                                              | No       | `false`            |
| `fullWidth`           | `boolean`                                  | If `true`, the element takes the full width of its container.               | No       | `false`            |
| `margin`              | `'none' \| 'dense' \| 'normal'`            | The margin spacing around the element.                                      | No       | `'normal'`         |
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
| `paddingBottom`       | `string`                                   | Custom padding-bottom style value.                                          | No       |                    |
# File

The `File` form element allows users to select and upload a single file, typically an image or video. It provides options to choose from the device library or capture directly using the camera. It handles file preview, upload progress (implicitly via `SinglePhotoItemView`), deletion, and file size validation.

## Props

| Name                  | Type                                                    | Description                                                                                                | Required | Default            |
| :-------------------- | :------------------------------------------------------ | :--------------------------------------------------------------------------------------------------------- | :------- | :----------------- |
| `label`               | `string`                                                | The label text for the field.                                                                              | No       | `''`               |
| `description`         | `string`                                                | Helper text displayed below the label or in selection prompts.                                             | No       | `''`               |
| `required`            | `boolean`                                               | Marks the field as required.                                                                               | No       | `false`            |
| `variant`             | `string`                                                | Visual style variant ('standard', 'outlined', 'filled', 'standard-inlined', 'livestream').                 | No       | `standard-inlined` |
| `fullWidth`           | `boolean`                                               | If true, the component takes the full width.                                                               | No       | `false`            |
| `margin`              | `string`                                                | Margin size ('none', 'dense', 'normal').                                                                   | No       | `normal`           |
| `paddingBottom`       | `string`                                                | Padding bottom size ('none', 'dense', 'normal').                                                           | No       | `normal`           |
| `preview_url`         | `string`                                                | URL of an existing image/file to preview initially.                                                        | No       | `undefined`        |
| `max_upload_filesize` | `object`                                                | Max file sizes in bytes (e.g., `{ photo: 5242880, video: 10485760 }`). `0` means no limit.               | No       | `{ photo: 0, video: 0 }` |
| `file_type`           | `string`                                                | Type of file allowed ('photo', 'video').                                                                   | No       | `photo`            |
| `cropping`            | `boolean`                                               | Enable image cropping after selection (currently might have limitations).                                  | No       | `false`            |
| `include_exif`        | `boolean`                                               | Include EXIF data when selecting photos.                                                                   | No       | `true`             |
| `item_type`           | `string`                                                | The type identifier for the uploaded item on the backend.                                                  | No       | `unknown`          |
| `upload_url`          | `string`                                                | The API endpoint for direct file uploads.                                                                  | No       | `/file`            |
| `extraProps`          | `object`                                                | Additional props for styling or behavior.                                                                  | No       | `{}`               |
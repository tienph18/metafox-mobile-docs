# SingleVideoFile

This form element allows users to select a single video, either by uploading a file directly or by providing a URL (depending on the `file_type` configuration). It displays a preview of the selected video and handles file size validation.

## Props

| Name                  | Type                                          | Description                                                                                                | Required | Default        |
| :-------------------- | :-------------------------------------------- | :--------------------------------------------------------------------------------------------------------- | :------- | :------------- |
| `label`               | `string`                                      | The display label for the form field.                                                                      | No       | -              |
| `required`            | `boolean`                                     | Whether the field is required.                                                                             | No       | `false`        |
| `fullWidth`           | `boolean`                                     | If `true`, the control stretches to full width.                                                            | No       | `false`        |
| `margin`              | `'normal' \| 'dense' \| 'none'`               | Controls the margin around the element.                                                                    | No       | `'normal'`     |
| `paddingBottom`       | `'normal' \| 'dense' \| 'none'`               | Controls the bottom padding of the element.                                                                | No       | `'normal'`     |
| `variant`             | `'standard' \| 'outlined' \| 'filled'`        | The visual style variant of the form control.                                                              | No       | `'standard'`   |
| `item_type`           | `string`                                      | Specifies the type of item being uploaded (e.g., 'video').                                                 | Yes      | -              |
| `upload_url`          | `string`                                      | The endpoint URL for uploading the file.                                                                   | Yes      | -              |
| `max_upload_filesize` | `number \| { video: number, photo: number }` | Maximum allowed file size in bytes. Can be an object with different limits for video/photo.                | Yes      | -              |
| `file_type`           | `'video' \| 'link'`                           | Specifies whether to handle a direct video upload ('video') or a video URL ('link').                       | Yes      | -              |
| `allow_upload`        | `boolean`                                     | Controls if direct video upload is allowed (used when `file_type` is not 'link').                          | No       | `true` (implied) |
| `storage_id`          | `number \| null`                              | Optional ID for a specific storage service.                                                                | No       | `null`         |
| `fetchEndpoint`       | `string`                                      | Optional endpoint for fetching video details when `file_type` is 'link'.                                   | No       | -              |
| `extraProps`          | `object`                                      | Additional props, often containing context like `module_name` and `resource_name` for validation URLs. | No       | `{}`           |
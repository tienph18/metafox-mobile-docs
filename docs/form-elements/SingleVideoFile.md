## SingleVideoFile

This form element allows users to select a single video, either by uploading a file directly or by providing a URL (depending on the `file_type` configuration). It displays a preview of the selected video and handles file size validation.

## Visual Examples

**File Type: video**

![File Type Video](../assets/SingleVideoFile/file_type-video.png)

**File Type: link**

![File Type Link Empty](../assets/SingleVideoFile/file_type-link.png)
![File Type Link with URL](../assets/SingleVideoFile/file_type-link-1.png)

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

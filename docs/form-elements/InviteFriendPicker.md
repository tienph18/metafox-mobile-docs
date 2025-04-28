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
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

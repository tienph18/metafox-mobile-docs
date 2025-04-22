# AttachPoll

Allows users to attach, view, edit, or remove a poll within a form. It presents a button to initiate the poll creation/editing process via a separate form screen (`form.edit` route) using the provided `config.formUrl`, and displays a preview of the attached poll using the `ui.AttachPollPreview` component.

## Props

| Name          | Type                               | Description                                                                 | Required | Default       |
| :------------ | :--------------------------------- | :-------------------------------------------------------------------------- | :------- | :------------ |
| `formUrl`     | `string`                           | API endpoint URL to fetch/submit the poll form data.                        | Yes      | `undefined`   |
| `label`       | `string`                           | The label text for the form control (handled by `FormControl`).             | No       | `undefined`   |
| `description` | `string`                           | Description text displayed below the control (handled by `FormControl`).    | No       | `undefined`   |
| `placeholder` | `string`                           | Placeholder text/translation key for the attach button.                     | No       | `'attach_poll'` |
| `disabled`    | `boolean`                          | Disables the field interaction.                                             | No       | `false`       |
| `fullWidth`   | `boolean`                          | If `true`, the control stretches to the full width of its container.        | No       | `true`        |
| `margin`      | `'none' \| 'normal' \| 'dense'`    | Defines the margin spacing around the control.                              | No       | `'normal'`    |
| `size`        | `'small' \| 'medium'`              | Defines the size of the control elements (like the button).                 | No       | `'medium'`    |
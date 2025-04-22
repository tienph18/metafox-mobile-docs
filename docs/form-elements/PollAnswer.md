# PollAnswer

A form element for managing a list of poll answers. Allows users to add, edit, and delete answer options, enforcing minimum/maximum answer counts and character limits per answer.

## Props

| Name         | Type    | Description                                       | Required | Default     |
| :----------- | :------ | :------------------------------------------------ | :------- | :---------- |
| `minAnswers` | number  | Minimum number of answers required.             | Yes      | *Varies*    |
| `maxAnswers` | number  | Maximum number of answers allowed (0=unlimited). | Yes      | *Varies*    |
| `maxLength`  | number  | Maximum character length for each answer.         | No       | `undefined` |
| `disabled`   | boolean | Disables the input fields and add/delete buttons. | No       | `false`     |
| `variant`    | string  | Visual style variant ('standard', 'standard-outlined'). | No       | `'standard'`|
| `fullWidth`  | boolean | If the element should occupy the full width.    | No       | `false`     |
# QuizQuestion

A form element for creating and managing a list of quiz questions, each with multiple answers and a designated correct answer. Users can add/remove questions and answers within specified limits.

## Props

| Name              | Type                                    | Description                                                                 | Required | Default     |
| :---------------- | :-------------------------------------- | :-------------------------------------------------------------------------- | :------- | :---------- |
| `label`           | `string`                                | The label text displayed for the form element.                              | Yes      |             |
| `fullWidth`       | `boolean`                               | If `true`, the element takes up the full width of its container.            | No       | `true`      |
| `margin`          | `'normal'`, `'dense'`, `'none'`         | Defines the margin spacing around the element.                              | No       | `'normal'`  |
| `required`        | `boolean`                               | If `true`, the field is marked as required.                                 | No       | `false`     |
| `variant`         | `'standard'`, `'outlined'`, `'filled'`  | The display style variant of the form control.                              | No       | `'standard'`|
| `paddingBottom`   | `'normal'`, `'dense'`, `'none'`         | Defines the bottom padding spacing for the element.                         | No       | `'normal'`  |
| `minQuestions`    | `number`                                | The minimum number of questions required.                                   | No       | `1`         |
| `maxQuestions`    | `number`                                | The maximum number of questions allowed.                                    | No       | `10`        |
| `minAnswers`      | `number`                                | The minimum number of answers required per question.                        | No       | `2`         |
| `maxAnswers`      | `number`                                | The maximum number of answers allowed per question.                         | No       | `20`        |
| `defaultAnswers`  | `number`                                | The default number of answer fields to show when adding a new question.     | No       | `2`         |
| `disabled`        | `boolean`                               | If `true`, the entire element is disabled.                                  | No       | `false`     |
| `maxLength`       | `number`                                | The maximum character length allowed for the question text.                 | No       | `undefined` |
| `maxAnswerLength` | `number`                                | The maximum character length allowed for each answer text.                  | No       | `undefined` |
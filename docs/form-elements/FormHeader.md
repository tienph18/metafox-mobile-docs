# FormHeader

Configures the navigation header for a form screen, setting the title, back button (left), and submit button (right). This element renders `null` and uses `navigation.setOptions` to apply the header configuration.

## Props

| Name                   | Type    | Description                                      | Required | Default         |
| :--------------------- | :------ | :----------------------------------------------- | :------- | :-------------- |
| `title`                | string  | The title displayed in the header.               | No       | `schema.title`  |
| `showLeftHeader`       | boolean | Whether to show the left header button (Back).   | No       | `true`          |
| `showRightHeader`      | boolean | Whether to show the right header button (Submit).| No       | `true`          |
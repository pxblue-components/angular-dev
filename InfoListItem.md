# InfoListItem

The InfoListItem is intended to be used in List views. It positions a title as well as optional subtitle(s), icon, and status stripe.

<img width="100%" alt="Info List Items in a variety of styles" src="./images/infoListItem.png">

## Usage

```typescript
// app.module.ts
import { InfoListItemModule } from '@pxblue/angular-components';
...
imports: [
    InfoListItemModule
  ],
```

```html
// your-component.html
<pxb-info-list-item title="Status" divider="full" [statusColor]="colors.green[500]">
    <mat-icon [style.color]="colors.green[500]" icon>eco</mat-icon>
</pxb-info-list-item>
```

## API

Parent element (`pxb-info-list-item`) attributes:

<div style="overflow: auto;">

| Attributes        | Description                            | Type                 | Required | Default        |
| ----------------- | -------------------------------------- | -------------------- | -------- | -------------- |
| avatar            | Show a colored background for the icon | `boolean`            | no       | false          |
| chevron           | Add a chevron icon on the right        | `boolean`            | no       | false          |
| dense             | Smaller height row with less padding   | `boolean`            | no       | false          |
| divider           | Show a row separator below the row     | `'full' | 'partial'` | no       |                |
| hidePadding       | Remove left padding if no icon is used | `boolean`            | no       | false          |
| statusColor       | Left border color                      | `string`             | no       |                |
| subtitle          | The text to show on the second line    | `string | string[]`  | no       |                |
| subtitleSeparator | Separator character for subtitle       | `string`             | no       | '·' ('\u00B7') |
| title             | The text to show on the first line     | `string`             | yes      |                |
| wrapSubtitle      | Whether to wrap subtitle on overflow   | `boolean`            | no       | false          |
| wrapTitle         | Whether to wrap title on overflow      | `boolean`            | no       | false          |

</div>

Child element with attributes:

<div style="overflow: auto;">

| Attributes      | Description                           | Required | Default |
| --------------- | ------------------------------------- | -------- | ------- |
| icon            | A component to render for the icon    | no       |         |
| left-component  | Component to render on the left side  | no       |         |
| right-component | Component to render on the right side | no       |         |

</div>
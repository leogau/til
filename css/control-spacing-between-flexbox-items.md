# Control Spacing Between Flexbox Items

The cleanest way to do this is using padding on the flexbox container and margin on the flexbox items.

```css
$gap: 10px;

dl {
  display: flex;
  flex-wrap: wrap;
  padding: $gap/2;

  dt, dd {
    margin: $gap/2;}

  dt { // full width, acts as header
    flex: 0 0 calc(100% - #{$gap});}

  dd { // default grid: four columns
    flex: 0 0 calc(25% - #{$gap});}

  .half { // hall width columns
    flex: 0 0 calc(50% - #{$gap});}

}
```

[Source](http://stackoverflow.com/a/27621985)

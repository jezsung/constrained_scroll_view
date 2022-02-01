## Motivation

Whenever the size of the screen changes, by the keyboard or the mobile resolution, our content should react to those changes dynamically and still be visible to the user. How do we do that? The easiest solution would be just wrapping the content with the SingleChildScrollView or ListView which makes the child scorllable by default. But what if the content is smaller than the height of the screen in vertical view and it bigger in horizontal view? You wouldn't want to make it scrollable when it's in vertical view. ConstrainedScrollView solves this problem elegantly.

## Getting started

Just wrap your Column widget with the ConstrainedScrollView. That's it. It works!

```dart
ConstrainedScrollView(
  child: Column(
    children: [
      ...
    ],
  ),
)
```

If you want to use the Flexible or Expanded widgets within the Column, then set the `flex` property to true.

```dart
ConstrainedScrollView(
  flex: true,
  child: Column(
    children: [
      ...
    ],
  ),
)
```

A GridView whose items the user can interactively reorder by dragging. 

Compared to the given `ReorderableListView`, it
is possible to reorder different sizes of widgets with or without animation.

<p>
  <img src="https://github.com/karvulf/flutter-reorderable-grid-view/blob/master/doc/flutter_reordable_grid_view_preview_ios.gif?raw=true"
    alt="An animated image of the iOS ReordableGridView UI" height="400"/>
</p>

## Features

Use this package in your Flutter App to:
- Enable a reordering logic with different widgets
- Simplified widget
- Works with all kind of widgets that are rendered inside
- Animated when reordering items

## Getting started
Simply add `ReordableGridView` to your preferred Widget and specify a list of children.

## Usage

```dart
import 'package:flutter_reorderable_grid_view/reorderable_grid_view.dart';
import 'package:flutter/cupertino.dart';
import 'package:flutter/material.dart';

class HomePage extends StatelessWidget {
  const HomePage({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      backgroundColor: Colors.grey,
      body: SafeArea(
        child: Padding(
          padding: const EdgeInsets.all(20),
          child: ReorderableGridView(
            children: List.generate(
              20,
                  (index) => Container(
                color: Colors.blue,
                height: 100,
                width: 100,
                child: Text(
                  'test $index',
                  style: const TextStyle(
                    fontSize: 20,
                    color: Colors.white,
                  ),
                ),
              ),
            ),
          ),
        ),
      ),
    );
  }
}
```

## Additional information
###ReordableGridView
| Parameter | Description | Default Value
| :------------- | :------------- | :-------------: |
| children | Displays all given children that are build inside a Wrap. | -
| spacing | Spacing in vertical direction between children. | 8
| runSpacing | Spacing in horizontal direction between children. | 8
| enableAnimation | Enables the animation when changing the positions of childrens after drag and drop. | true
| enableLongPress | Decides if the user needs a long press to move the item around. | true

## Future
If you have feature requests or found some problems, feel free and open your issues in the GitHub project.

Thank you for using this package.
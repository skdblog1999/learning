# Day 1

## Flutter CLI

1. `flutter create <prject-name>`
2. `flutter run`
3. `flutter run -d <available-devices>`
4. `flutter doctor`
5. `flutter devices`

## `runApp()`

It takes the given Widget and makes it the root of the widget tree.

## Basic Widgets

### `Text`

The `Text` widget lets you create a run of styled text within your application.

### `Row`, `Column`

These flex widgets let you create flexible layouts in both the horizontal (`Row`) and vertical (`Column`) directions. The design of these objects is based on the web’s flexbox layout model.

### `Stack`

Instead of being linearly oriented (either horizontally or vertically), a `Stack` widget lets you place widgets on top of each other in paint order. You can then use the [`Positioned`](https://api.flutter.dev/flutter/widgets/Positioned-class.html) widget on children of a `Stack` to position them relative to the top, right, bottom, or left edge of the stack. Stacks are based on the web’s absolute positioning layout model.

### `Container`

The `Container` widget lets you create a rectangular visual element. A container can be decorated with a [`BoxDecoration`](https://api.flutter.dev/flutter/painting/BoxDecoration-class.html), such as a background, a border, or a shadow. A `Container` can also have margins, padding, and constraints applied to its size. In addition, a `Container` can be transformed in three dimensional space using a matrix.



## `uses-material-design: true`

It allows you to use the predefined set of [Material icons](https://design.google.com/icons/).

## `MaterialApp`

Many Material Design widgets need to be inside of a [`MaterialApp`](https://api.flutter.dev/flutter/material/MaterialApp-class.html) to display properly, in order to inherit theme data.

## `Expanded`

Expands to fill any remaining available space that hasn’t been consumed by the other children.

## StatelessWidget vs StatefulWidget

Stateless widgets receive arguments from their parent widget, which they store in [`final`](https://dart.dev/guides/language/language-tour#final-and-const) member variables.

`StatefulWidgets` are special widgets that know how to generate `State` objects, which are then used to hold state.

## StatefulWidget

```dart
class Counter extends StatefulWidget {
  // This class is the configuration for the state. It holds the
  // values (in this case nothing) provided by the parent and used by the build
  // method of the State. Fields in a Widget subclass are always marked "final".

  @override
  _CounterState createState() => _CounterState();
}

class _CounterState extends State<Counter> {
  int _counter = 0;

  void _increment() {
    setState(() {
      // This call to setState tells the Flutter framework that
      // something has changed in this State, which causes it to rerun
      // the build method below so that the display can reflect the
      // updated values. If you change _counter without calling
      // setState(), then the build method won't be called again,
      // and so nothing would appear to happen.
      _counter++;
    });
  }

  @override
  Widget build(BuildContext context) {
    // This method is rerun every time setState is called,
    // for instance, as done by the _increment method above.
    // The Flutter framework has been optimized to make rerunning
    // build methods fast, so that you can just rebuild anything that
    // needs updating rather than having to individually change
    // instances of widgets.
    return Row(
      children: <Widget>[
        RaisedButton(
          onPressed: _increment,
          child: Text('Increment'),
        ),
        Text('Count: $_counter'),
      ],
    );
  }
}

```

## Layouts

### `Container`

Use a `Container` when you want to add padding, margins, borders, or background color, to name some of its capabilities.

### `ListTile`

[ListTile](https://api.flutter.dev/flutter/material/ListTile-class.html),  an easy-to-use widget with properties for leading and trailing icons,  and up to 3 lines of text.

### `ListView`

[ListView](https://api.flutter.dev/flutter/widgets/ListView-class.html),  a column-like layout that automatically scrolls if its content is too long  to fit the available space

## Aligning Widgets

You control how a row or column aligns its children using the `mainAxisAlignment` and `crossAxisAlignment` properties. For a row, the main axis runs horizontally and the cross axis runs vertically. For a column, the main axis runs vertically and the cross axis runs horizontally.

## Adding Assets in Flutter

```
flutter:
  assets:
    - assets/my_icon.png
    - assets/background.png

To include all assets under a directory, specify the directory name with the / character at the end

flutter:
  assets:
    - directory/
    - directory/subdirectory/

```


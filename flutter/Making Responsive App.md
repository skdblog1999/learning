# Making Responsive UI’s

1. Forcing Portrait Mode

   ```dart
   SystemChrome.setPreferredOrientations(DeviceOrientation.portraitUp);
   ```

   

2. Getting Orientation

   ```dart
   MediaQuery.of(context).orientation
   ```

   
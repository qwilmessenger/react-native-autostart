
# react-native-autostart

## Getting started

`$ npm install react-native-autostart --save`

### Mostly automatic installation

`$ react-native link react-native-autostart`

### Manual installation


#### Android

1. Open up `android/app/src/main/java/[...]/MainActivity.java`
  - Add `import com.qwil.autostart.RNAutostartPackage;` to the imports at the top of the file
  - Add `new RNAutostartPackage()` to the list returned by the `getPackages()` method
2. Append the following lines to `android/settings.gradle`:
  	```
  	include ':react-native-autostart'
  	project(':react-native-autostart').projectDir = new File(rootProject.projectDir, 	'../node_modules/react-native-autostart/android')
  	```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
  	```
      compile project(':react-native-autostart')
  	```


## Usage
```javascript
import RNAutostart from 'react-native-autostart';

// open the autostart preferences menu for device
RNAutostart.open();
```
  
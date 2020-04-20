# Change log (200417)

- props.selected 배열을 push / splice를 이용하여 직접 수정하던 부분을 filter / concat으로 대체했음
- props.selectedMarker를 컴포넌트 대신 컴포넌트를 반환하는 함수로 변경하고, 인덱스를 받도록 수정

[![version](https://img.shields.io/npm/v/react-native-camera-roll-picker.svg)](https://www.npmjs.org/package/react-native-camera-roll-picker) [![npm](https://img.shields.io/npm/dt/react-native-camera-roll-picker.svg)](https://www.npmjs.org/package/react-native-camera-roll-picker)

# react-native-camera-roll-picker

CameraRoll Picker component for React native

<a href="https://github.com/jjecgd/react-native-camera-roll-picker/blob/master/demo/demo.gif"><img src="https://github.com/jjecgd/react-native-camera-roll-picker/blob/master/demo/demo.gif" width="350"></a>

Requires `react-native >=0.43.0`

## Add to Project

- Install component through npm

```
$ npm install react-native-camera-roll-picker --save
```

- Install CameraRoll from @react-native-community

```
$ npm install @react-native-community/cameraroll
```

- Require component

```
import CameraRollPicker from 'react-native-camera-roll-picker';
```

## Basic Usage

```js
<CameraRollPicker callback={this.getSelectedImages} />
```

## Props

- `callback` : Callback function when images was selected. (is required!). Return a selected image array and current selected image.
- `initialNumToRender` : Specifies how many rows we want to render on our first render pass. (Default: 5)
- `groupTypes` : The group where the photos will be fetched, one of 'Album', 'All', 'Event', 'Faces', 'Library', 'PhotoStream' and 'SavedPhotos'. (Default: SavedPhotos)
- `assetType` : The asset type, one of 'Photos', 'Videos' or 'All'. (Default: Photos)
- `selected` : Already be selected images array. (Default: [])
- `selectSingleItem` : Boolean to select only one single image at time. (Default: `false`)
- `maximum` : Maximum number of selected images. (Default: 15)
- `imagesPerRow` : Number of images per row. (Default: 3)
- `imageMargin` : Margin size of one image. (Default: 5)
- `containerWidth` : Width of camer roll picker container. (Default: device width)
- `selectedMarker` : Get custom selected image marker component function. (Default: checkmark) (Example: `(index) => <View><Text>{index}</Text></View>`).
- `backgroundColor` : Set background color. (Default: white).
- `emptyText`: Text to display instead of a list when there are no photos found. (Default: 'No photos.')
- `emptyTextStyle`: Styles to apply to the `emptyText`. (Default: `textAlign: 'center'`)
- `loader`: Loader component node. (Default: `<ActivityIndicator />`)

## How to install

```
$ yarn add react-native-camera-roll-picker@git+https://github.com/jjecgd/react-native-camera-roll-picker.git
```

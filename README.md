# React Native SwipeView Flat


## Getting Started

- [Installation](#installation)
- [Basic Usage](#basic-usage)
- [Properties](#properties)

### Installation
```bash
$ npm i react-native-swipeview-flat --save
```

### Basic Usage
```jsx
import React, {Component} from 'react';
import { StyleSheet, Text, View } from 'react-native';

import SwipeView from 'react-native-swipeview-flat';

export default class App extends Component {

  render() {

    return (
      <View style={styles.container}>
        <SwipeView
          scroll={scrolling => console.log(scrolling)}
          renderVisibleContent={() => <Text style={styles.text}>SwipeMe</Text>}
        />
      </View>
    );
  };
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    alignItems: 'center',
    justifyContent: 'center',
  },
  text: {
    backgroundColor: 'whitesmoke',
    padding: 20,
  }
});

```
![alt text](http://res.cloudinary.com/rishabhbhatia/image/upload/c_scale,w_200/v1504599144/swipeview/swipeview-basic-v1.0.1.gif)

### Properties

#### Basic

| Prop  | Type | Description | Default|
| :------------ |:---------------:| :---------------:| :-----|
| leftOpenValue | `number` | TranslateX: How much view opens from the left when swiping left-to-right (positive number). | 0 |
| rightOpenValue | `number` | TranslateX: How much view opens from the right when swiping right-to-left (negative number). | 0 |
| swipeDuration | `number` | Duration of the slide out swipe animation. | 250 |
| swipeToOpenPercent | `number` | What % of the left/right openValue does the user need to swipe past to trigger onSwipedLeft/onSwipedRight actions. | 35 |
| disableSwipeToLeft | `bool` | Disable ability to swipe view to left. | false |
| disableSwipeToRight | `bool` | Disable ability to swipe view to right. | false |
| onSwipedLeft | `func` | Called when left swipe is completed. | - |
| onSwipedRight | `func` | Called when right swipe is completed. | - |
| previewSwipeDemo | `bool` | Should the view do a slide out preview to show that it is swipe-able. | false |
| previewDuration | `number` | Duration of the slide out preview animation. | 300 |
| previewOpenValue | `number` | TranslateX value for the slide out preview animation. | -60 |
| previewOpenDelay | `number` | Delay before starting preview animation. | 350 |
| previewCloseDelay | `number` | Delay before closing preview animation. | 300 |
| swipingLeft | `bool` | Should swiping initialize with right-to-left. This should be useful for swipe previews ex: +ve previewOpenValue `swipingLeft: false` & -ve previewOpenValue `swipingLeft: true`. | true |
| recalculateHiddenLayout | `bool` | Enable hidden row onLayout calculations to run always. | false |
| directionalDistanceChangeThreshold | `number` | Change the sensitivity of the row. | 2 |
| scroll | `func` | Called when swipe actions starts/ends

#### Views
| Prop  | Type | Description | Default|
| :------------ |:---------------:| :---------------:| :-----|
| renderVisibleContent | `func` | Main Content view. | - |
| renderLeftView | `func` | Left view to render behind the right view. | - |
| renderRightView | `func` | Right view to render behind the item view. | - |

## Contribution

* rishabhbhatia
* eugenehp

## Credits

Inspirations:
* react-native-swipe-list-view [(Github)](https://github.com/jemise111/react-native-swipe-list-view)
* react-native-todo [(GitHub)](https://github.com/rishabhbhatia/react-native-todo)
* react-native-swipeview [(GitHub)](https://github.com/rishabhbhatia/react-native-swipeview)

## Questions

Create an issue](https://github.com/eugenehp/react-native-swipeview/issues/new)

## License

Released under the [Mit License](https://opensource.org/licenses/MIT)

# react-native-animated-modal
Animated simple modal on React Native.

## Installation
```
npm install react-native-animated-modal
```

## Documentation

| Prop  | Description  | Type  | Default  | Required  |
|---|---|---|---|---|
| isOpen | Open state of modal. | boolean | false | **YES** |
| toggleFunc | Changing open state of modal function.  | func | 'indigo' | **YES** |
| easing | Animation easing. [Please read](https://reactnative.dev/docs/easing) | string | 'linear' | **NO** |
| animationTime | Animation running time. | number | 750 | **NO** |
| width | Width of modal. (device screen width percentage) | number | 80 | **NO** |
| height | Height of modal. (device screen height percentage) | number | null | **NO** |
| modalColor | Background color of modal. | string | 'white' | **NO** |
| backdropColor | Background color of modal backdrop. | string | 'rgba(0, 0, 0, 0.8)' | **NO** |
| modalRadius | Border radius value of modal view. (px) | number | 15 | **NO**  |
| modalStyle | Custom style of modal view. | object | null | **NO**  |
| isFullScreen | Size of modal view. (full screen or not) | boolean | false | **NO**  |
| onShow | The function you want to work while modal is turned on. | func | - | **NO**  |
| onClose | The function you want to work while modal is turned off. | func | - | **NO**  |

## Usage
```
const [isOpen, setIsOpen] = useState(false);

const toggleFunc = () => {
    setIsOpen(!isOpen);
};

<TouchableOpacity onPress={() => toggleFunc()}>
    <View style={{padding: 30}}>
        <Text>Open modal</Text>
    </View>
</TouchableOpacity>

// Add end of the view that has flexibility of 1.
<Modal
    isOpen={isOpen}
    toggleFunc={toggleFunc}
    animationType='bounce'
>
    <View style={{padding: 30}}>
        <TouchableOpacity
            style={{alignSelf: 'flex-end', marginBottom: 10,}}
            onPress={() => toggleFunc()}>
            <Text>Close</Text>
        </TouchableOpacity>
        <Text>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut
            labore et dolore magna aliqua.
        </Text>
    </View>
</Modal>
```

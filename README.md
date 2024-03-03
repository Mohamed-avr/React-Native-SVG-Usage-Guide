# React-Native-Svg
Integrate SVG in your react native projects

You might have realized that React Native does not support SVG icons, but fear not here is a solution how to integrate svg icons

## 1 Installation :skull:
 First install [react native svg](https://github.com/software-mansion/react-native-svg?tab=readme-ov-file#installation).

npm 
```
npm install react-native-svg
```

yarn 
```
yarn add react-native-svg
```

## 2 Create icon component 
in your react app create an componentFileName.js as a component then inside this component import react-native-svg library 
and insert the SVG file 
example : 

``` javascript

import React from "react";
import { View, Text } from "react-native";
import Svg, { Path, Rect, G, Defs, ClipPath } from "react-native-svg";

export default function IconName() {
  return (
    <View
      style={{
        display: "flex",
        justifyContent: "center",
        alignItems: "center",
      }}
    >
      <Svg
        width="24"
        height="24"
        viewBox="0 0 24 24"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <Path
          fillRule="evenodd"
          clipRule="evenodd"
          d="M7.71389 12.0031C7.71389 12.2281 7.66955 12.451 7.58342 12.659C7.49728 12.8669 7.37103 13.0559 7.21187 13.215C7.05271 13.3742 6.86376 13.5005 6.65581 13.5866C6.44786 13.6727 6.22497 13.7171 5.99989 13.7171C5.7748 13.7171 5.55192 13.6727 5.34397 13.5866C5.13602 13.5005 4.94707 13.3742 4.78791 13.215C4.62875 13.0559 4.5025 12.8669 4.41636 12.659C4.33022 12.451 4.28589 12.2281 4.28589 12.0031C4.28589 11.5485 4.46647 11.1125 4.78791 10.7911C5.10935 10.4696 5.54531 10.2891 5.99989 10.2891C6.45447 10.2891 6.89043 10.4696 7.21187 10.7911C7.53331 11.1125 7.71389 11.5485 7.71389 12.0031ZM11.9999 13.7181C12.4546 13.7181 12.8907 13.5374 13.2122 13.2159C13.5338 12.8944 13.7144 12.4583 13.7144 12.0036C13.7144 11.5488 13.5338 11.1128 13.2122 10.7912C12.8907 10.4697 12.4546 10.2891 11.9999 10.2891C11.5452 10.2891 11.1091 10.4697 10.7876 10.7912C10.466 11.1128 10.2854 11.5488 10.2854 12.0036C10.2854 12.4583 10.466 12.8944 10.7876 13.2159C11.1091 13.5374 11.5452 13.7181 11.9999 13.7181ZM17.9999 13.7181C18.4546 13.7181 18.8907 13.5374 19.2122 13.2159C19.5338 12.8944 19.7144 12.4583 19.7144 12.0036C19.7144 11.5488 19.5338 11.1128 19.2122 10.7912C18.8907 10.4697 18.4546 10.2891 17.9999 10.2891C17.5452 10.2891 17.1091 10.4697 16.7876 10.7912C16.466 11.1128 16.2854 11.5488 16.2854 12.0036C16.2854 12.4583 16.466 12.8944 16.7876 13.2159C17.1091 13.5374 17.5452 13.7181 17.9999 13.7181Z"
          fill="#7C7C7C"
        />
      </Svg>
    </View>
  );
}

```
Before to move to the next step please make sure that you changed Svg tags to Svg react native library tags ? 
look to the code above and this table you will understand 

The table: 
| Svg tags        | Library tags       |
| --------------- | ------------------ |
| `<svg>`         | `<Svg>`            |
| `<rect>`        | `<Rect>`           |
| `<circle>`      | `<Circle>`         |
| `<path>`        | `<Path>`           |
| `<line>`        | `<Line>`           |
| `<polyline>`    | `<Polyline>`       |
| `<polygon>`     | `<Polygon>`        |
| `<ellipse>`     | `<Ellipse>`        |
| `<text>`        | `<Text>`           |
| `<tspan>`       | `<TSpan>`          |
| `<textPath>`    | `<TextPath>`       |
| `<g>`           | `<G>`              |
| `<defs>`        | `<Defs>`           |
| `<clipPath>`    | `<ClipPath>`       |
| `<mask>`        | `<Mask>`           |


Also the same with properties: 
| SVG Attribute      | React Native Property |
| ------------------ | --------------------- |
| `fill-rule`        | `fillRule`            |
| `clip-rule`        | `clipRule`            |
| `stroke-width`     | `strokeWidth`         |
| `stroke-linecap`   | `strokeLinecap`       |
| `stroke-linejoin`  | `strokeLinejoin`      |
| `stroke-miterlimit`| `strokeMiterlimit`    |
| `stroke-opacity`   | `strokeOpacity`       |
| `stroke-dasharray` | `strokeDasharray`     |
| `stroke-dashoffset`| `strokeDashoffset`    |


## 3 Add your icon component to any any screen you want 
now just import your component , example: 

``` javascript

import React from "react";
import { View, Text } from "react-native";

// export the icon component 
import IconName from "./NavBarIconsComponents/IconName";

export default function App() {
  return (
  <View>
    <IconName />
 </View>
   );
}

```
You can pass the widht and the height and the colors as props to contole it more, example  ` <PlusIcon height={28} width={28} color={iconColor} /> `


# I hope this helped you!! 


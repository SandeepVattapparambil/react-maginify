![reactmagnifier-logo](logo/logo.png)

# ReactMagnifier v0.0.1

ReactMagnifier is a simple and highly configurable react plugin to perform image magnification. This is a **UMD** module, so it can be used isomorphically.
> **Note:** The name of the npm package is @react-ui-lib/react-magnifier

## Features

* Light weight (18 KB minified)
* Written in Typescript
* Highly customizable
* Supports touch screens as well
* Supports event listeners 
* Supports all kinds of images and image urls, high resolutions as well
* Supports custom css styles
* Supports client-side react apps as well as server-side rendered react apps

## Table of Contents

<!--ts-->
* [About](#reactmagnifier-v001)
* [Features](#features)
* [Demo](#demo)
* [Installation](#installation)
* [Sample Usage](#sample-usage)
* [Dependency](#dependency)
* [Changelog](#changelog)
    * [v0.0.1](#v001)
* [API Documentation](#api-documentation)
* [Tests](#tests)
* [License](#license)
* [Acknowledgements](#acknowledgements)
<!--te-->

## Demo

![demo-gif](logo/sample.gif)
More examples and demos can be found in `example` folder in the root of the repo.

## Installation

Install the package from NPM using:
```sh
npm i @react-ui-lib/react-magnifier
```

## Sample Usage

Add the component to your project using:

```js
import ReactMagnifier from "@react-ui-lib/react-magnifier";
import image from './path/image";

 <ReactMagnifier
      imageUrl={image}
      zoomSize={3}
      imageAltText={"Some text"}
      imageHeight={400}
      imageWidth={600}
      magnifierHeight={200}
      magnifierWidth={200}
      magnifierRadius={50}
      magnifierBorderColor={"white"}
      magnifierBorderStyle={"solid"}
      magnifierBorderWidth={2}
      magnifierShadow={true}
      cursor={"none"}
      getMagnifier={showEvent}
      customImgStyles={'myClass'}
      customContainerStyles={'aClass'}
   />
```

## Dependency

This component requires the following node modules as its dependency:

* `react` - The react js core library, version `(16.12.0)` is used here.
* `react-dom` - The react js dom library, version`(16.12.0)` is used here.

## Changelog

#### v0.0.1

* Initial stable build
* Includes all essential features and cuistomizations

## API Documentation

### Props

The following table gives all the possible input props and its default values and customizations.

| Props | Type | Required | Default | Description | 
| :-- | :-- | :-- | :-- | :-- |
| **`imageUrl`** | *String* | yes | empty | Url string for the image to be displayed and magnified.This is a mandatory prop. If not supplied, the component will throw `ReactMagnifier Error: Image url is missing!. <ReactMagnifier imageUrl={url}/> is required.` error in console, but will not break your apps ui.| 
| `imageAltText` | *String* | no | `react-magnifier-image` | The `alt` text value for the image |
| `imageHeight` | *Number* | no | 200 | Height of the image |
| `imageWidth` | *Number* | no | 200 | Width of the image |
| `magnifierHeight` | *Number* | no | 100 | Height of the magnifier |
| `magnifierWidth` | *Number* | no | 100 | Width of the magnifier |
| `magnifierRadius` | *Number* | no | 50 | Border radius of the magnifier |
| `magnifierBorderColor` | *String* | no | `#000` | Border color of the magnifier |
| `magnifierBorderStyle` | *String* | no | `solid` | Border style of the magnifier |
| `magnifierBorderWidth` | *Number* | no | 3 | Border width of the magnifier |
| `magnifierShadow` | *Boolean* | no | `true` | Box shadow for the magnifier|
| `cursor` | *String* | no | `none` | Mouse cursor on magnifier |
| `zoomSize` | *Number* | no | 2 | Magnification factor |
| `getMagnifier` | *Function* | no | empty | Get reference to the image under magnification. The function prop returns the html element. It also includes custom events fired inside the component. |
| `customImgStyles` | *String* | no | empty | White space separated CSS class names in a single string format. It can be used to override the styles of react magnifier, example : `myClass newClass ..` |
| `customContainerStyles` | *String* | no | empty | White space separated CSS class names in a single string format. It can be used to override the styles of react magnifier, example : `myClass newClass ..` |

### Events
The following `events` are available on the ReactMagnifier component. These are available on the element returned from `getMagnifier` function prop

| Event | Type | Description | 
| :-- | :-- | :-- |
| `magnifier-initialized` | *CustomEvent* | This event is triggered when the magnifier is initialized for the first time. This event is triggered only once |
| `magnfier-moved` | *CustomEvent* | This event is triggered anytime the magnifier is moved |
| `magnifier-visible` | *CustomEvent* | This event is triggered when the magnifier is visible when hovered over the image |
| `magnifier-invisible` | *CustomEvent* | This event is triggered when the magnifier is invisible when moved out of the image |

These events can be used to trigger custom logic in your app when magnifier is initialized and used.

## Contributing
All suggestions and pull requests are welcome. Please read the [CODE_OF_CONDUCT](https://github.com/SandeepVattapparambil/react-magnify/blob/master/CODE_OF_CONDUCT.md) and [CONTRIBUTING](https://github.com/SandeepVattapparambil/react-magnify/blob/master/CONTRIBUTING.md) files before contributing.

## Tests
This project includes unit tests written in `Jest` testing library. Tests can be run by the npm script
```sh
npm run test
```

## License
MIT License

Copyright (c) 2020 Sandeep Vattapparambil [http://www.sandeepv.in](http://www.sandeepv.in)

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Acknowledgements
This project is inspired from [Blowup.js](https://paulkr.github.io/blowup.js/), but not copied or does not include any or part of it in this project.

Made with :heart: by [Sandeep Vattapparambil](https://github.com/SandeepVattapparambil).
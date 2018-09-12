# react-audio-waveform
Render waveforms from arrays of peak data generated by [Audio Waveform](https://github.com/bbc/audiowaveform) quickly and easily.

#### Installation

`npm install react-audio-waveform --save`

or

`yarn add react-audio-waveform`

#### Usage

```jsx
import Waveform from "react-audio-waveform"

// ...

<Waveform
  barWidth={4}
  peaks={this.props.peaks}
  height={200}
  pos={this.props.pos}
  duration={210}
  onClick={this.handleClick}
  color="#676767"
  progressGradientColors={[[0, "#888"], [1, "#aaa"]]}
/>
```
  
#### Options

|      Parameter     |      Description    |  Permitted Values  |       Default      |
| ------------------ | ------------------- | ------------------ | ------------------ |
| `barWidth`  | Width of the peaks | Number | `undefined` |
| `color`  | The main waveform's color | String (hex value) | `undefined` |
| `duration` | Audio length in seconds | Number |  `undefined` |
| `gradientColors`  | The main waveform's color as an array of arrays containing start positions (from 0 to 1) and colors; example: `[[0, "#888888"], [1, "#aaaaaa"]]` | Array | `undefined` |
| `height` | The waveform's height | Integer | `undefined` |
| `onClick` | Handler for seeking. This is a function with a single argument of seconds as a number. | function | `() => {}` |
| `peaks` | Array of peaks. | Array | `undefined` |
| `pixelRatio` | Determines how many pixels to fit inside a single pixel space. | Number | The current device's pixel ratio |
| `pos` | The audio's current position in seconds | Number | `undefined` |
| `progressColor`  | The progress waveform's color | String (hex value) | `undefined` |
| `progressGradientColors`  | The progress waveform's color as an array of arrays containing start positions (from 0 to 1) and colors; example: `[[0, "#888888"], [1, "#aaaaaa"]]` | Array | `undefined` |

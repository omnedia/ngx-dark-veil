# ngx-dark-veil

<a href="https://ngxui.com" target="_blank" style="display: flex;gap: .5rem;align-items: center;cursor: pointer; padding: 0 0 0 0; height: fit-content;">
  <img src="https://ngxui.com/assets/img/ngxui-logo.png" style="width: 64px;height: 64px;">
</a>

This library is part of the NGXUI ecosystem. <br>
View all available components at [https://ngxui.com](https://ngxui.com)

`@omnedia/ngx-dark-veil` is an Angular library that creates an animated, shader-based "dark veil" effect. This component provides a dynamic, noise-infused background with hue shift, warp distortion, and scanline effects, perfect for sci-fi, cyberpunk, or atmospheric UI designs.

## Features

* High-performance WebGL shader-based background.
* Adjustable hue shift for color customization.
* Configurable noise, warp, and scanline intensity.
* Automatic rendering only when in view (performance-friendly).
* Standalone Angular component, compatible with Angular 20+.

## Installation

```bash
npm install @omnedia/ngx-dark-veil ogl
```

## Usage

Import the `NgxDarkVeilComponent` into your Angular component:

```typescript
import {NgxDarkVeilComponent} from '@omnedia/ngx-dark-veil';

@Component({
  ...
    imports:
[
  ...,
  NgxDarkVeilComponent
],
...
})
```

Then use it in your template:

```html

<om-dark-veil
  [hueShift]="180"
  [noiseIntensity]="0.1"
  [scanlineIntensity]="0.05"
  [warpAmount]="0.02"
  [scanlineFrequency]="4.0"
  [speed]="1"
  [resolutionScale]="1"
  style="width: 100%; height: 400px; display: block;"
></om-dark-veil>
```

## How It Works

* **Hue Shift**: Rotates colors of the generated shader texture.
* **Noise**: Adds dynamic grain for a gritty, analog look.
* **Scanlines**: Simulates CRT-like horizontal scanline patterns.
* **Warp**: Distorts the texture for a glitchy feel.
* **Performance Optimization**: Uses an IntersectionObserver to only animate when visible.

## API

```html

<om-dark-veil
  [hueShift]="hueShift"
  [noiseIntensity]="noiseIntensity"
  [scanlineIntensity]="scanlineIntensity"
  [warpAmount]="warpAmount"
  [scanlineFrequency]="scanlineFrequency"
  [speed]="speed"
  [resolutionScale]="resolutionScale"
></om-dark-veil>
```

### Inputs

* `hueShift` (number): Degrees to rotate hue. Default `0`.
* `noiseIntensity` (number): Noise grain strength. Default `0`.
* `scanlineIntensity` (number): Scanline darkness. Default `0`.
* `warpAmount` (number): Warp distortion strength. Default `0`.
* `scanlineFrequency` (number): Number of scanlines. Default `0`.
* `speed` (number): Animation speed multiplier. Default `1`.
* `resolutionScale` (number): Internal render resolution scale. Default `1`.

## Example

```html

<om-dark-veil
  [hueShift]="220"
  [noiseIntensity]="0.15"
  [scanlineIntensity]="0.1"
  [warpAmount]="0.03"
  [scanlineFrequency]="5.0"
  [speed]="1.2"
  style="width: 100%; height: 500px; display: block;"
></om-dark-veil>
```

This will create a dark veil with a blue hue, moderate noise, visible scanlines, and slight warping.

## Styling

`<om-dark-veil>` renders a `<canvas>` that fills its container. You can style the container with standard CSS to set position, size, and layout.

Example:

```css
om-dark-veil {
  border-radius: 12px;
  overflow: hidden;
  display: block;
}
```

## Contributing

Contributions are welcome. Please submit a pull request or open an issue to discuss your ideas.

## License

This project is licensed under the MIT License.

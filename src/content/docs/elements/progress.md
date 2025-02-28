---
title: o-progress web-component
---

`<o-progress>` is a standard web-component for rendering a radial progress bar. Just one o-progress can be used per orbit.
It has two elements: a progress bar and a background bar that show the max range progress bar can achieve.

### Customization
  
- **o-progress size:** Each `.o-progress` can be adjusted using the CSS class utility `.shrink-10` to `.shrink-90`, allowing the o-progress to shrink by a specified percentage. On opposite way, the CSS class utility `.grow-1x` to `.grow-12x`, allowing the o-progress to expand by a mutiple of `.orbit` size. Note that `shrink-*` and `.grow-*x` can't be used at same time.
  
- **Look and feel:** o-progress has special attributes: 
  - `value`: To set a number that represents the progress bar value.
  - `max`: To set the max allowed `value`.
  - `shape`: To set a different endings looks. Currently, you can choose between `circle`, `arrow`, `slash`, `backslash` and `zigzag` shapes. Default `none`.
  - Use following CSS custom vars to define colors: `--color` and `--hover-color` for progress bar, `--bgcolor` for background bar.

- **Adjust radial layout:**
  - **`.angle-*`:** Set arbitrary o-progress angle from 0 to 360 degrees, overrriding automatic radial arragement.
  - **`.inner-orbit`:** To place an`.o-progress` just below its orbit.
  - **`.outer-orbit`:** To place `.o-progress` just above its orbit.
  - **`.quarter-inner-orbit`:** To place `.o-progress` a 25% into its orbit.
  - **`.quarter-outer-orbit`:** To place `.o-progress` a 25% outer its orbit.
  
**Important:** 
  - `<o-progress>` can only be used into `.orbit` or `.orbit-*`.
  - `<o-progress>` doesn't support ellipse shape. See `.orbit` section for more information.

### Usage

```html
<div class="orbit"> 
  <o-progress value="75" max="100" shape="circle"></o-progress>
</div>
```

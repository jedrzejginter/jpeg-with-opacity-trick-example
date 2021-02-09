# JPEG with opacity trick ([inspiration](https://css-tricks.com/transparent-jpg-svg/))

Simple trick to have JPEG image with opacity, using SVG Clip Path.

## Code
```svg
<svg
  xmlns="http://www.w3.org/2000/svg"
  xmlns:xlink="http://www.w3.org/1999/xlink"
  viewBox="0 0 512 384"
>
  <defs>
    <clipPath id="clip">
      <circle cx="256" cy="192" r="192" />
    </clipPath>
  </defs>
  <image
    href="./image.jpg"
    clip-path="url(#clip)"
    width="512"
    height="384"
    x="0"
    y="0"
  />
</svg>
```

## Result

_The gray background is applied by wrapping div to show that opacity is there._

<div style="background-color: #ccc">
  <svg
    xmlns="http://www.w3.org/2000/svg"
    xmlns:xlink="http://www.w3.org/1999/xlink"
    viewBox="0 0 512 384"
  >
    <defs>
      <clipPath id="clip">
        <circle cx="256" cy="192" r="192" />
      </clipPath>
    </defs>
    <image
      href="./image.jpg"
      clip-path="url(#clip)"
      width="512"
      height="384"
      x="0"
      y="0"
    />
  </svg>
</div>

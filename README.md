# crypto-qrcode

Combines elements of https://github.com/spothq/cryptocurrency-icons and https://github.com/man15h/vue-cryptoicon to create QR codes with coloured icons in the middle.

## To do

### 1

Start with https://github.com/spothq/cryptocurrency-icons and once you have the instance of the canvas you can easily draw an image at the center. Something like
 
```ts
const logo = new Image();
logo.src = 'logo.png';
logo.onload = () => {
  const ctx = qrCodeCanvas.getContext('2d');
  ctx.imageSmoothingEnabled = false;
  // This puts a 50x50 logo right at the center of a 200x200 canvas
  ctx.drawImage(logo, 75, 75, 50, 50);
}
```
Or... maybe create with using an SVG renderer https://github.com/soldair/node-qrcode/issues/237#issuecomment-673436444

### 2

Then have a look at https://github.com/man15h/vue-cryptoicon and incorporate the color feature for the icon. Note that on their demo page https://vue-cryptoicon.netlify.app/ they have set the correct colouring for each icon when the "color" option is selected, hence for color settings of each icon, please use those colours.

***

[Mozilla Public License Version 2.0](https://www.mozilla.org/en-US/MPL/2.0/)

Thanks to:
- https://github.com/spothq/cryptocurrency-icons
- https://github.com/man15h/vue-cryptoicon

The word "QR Code" is a registered trademark of DENSO WAVE INCORPORATED

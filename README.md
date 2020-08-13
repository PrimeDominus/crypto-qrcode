# crypto-qrcode

Combines elemnts of https://github.com/spothq/cryptocurrency-icons and https://github.com/man15h/vue-cryptoicon to create QR codes with coloured icons in the middle.

## To do

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
Then have a look at https://github.com/man15h/vue-cryptoicon and incorporate the color feature for the icon.

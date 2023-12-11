>Ref: [[CSS#Example CSS At-Rules]]

Create new HTML temple and link it with some CSS file to do the assignment below step by step.

###### 1. Import Google Font
You can go to [Google Font](https://fonts.google.com/) to pick up your right font from them or just copy the following code into your CSS file.

```css
@import url('https://fonts.googleapis.com/css2?family=Mali:ital,wght@0,200;0,300;0,400;0,500;0,600;0,700;1,200;1,300;1,400;1,500;1,600;1,700&family=Roboto:ital,wght@0,300;0,400;0,500;0,700;0,900;1,100;1,300;1,400;1,500;1,700;1,900&display=swap');
```

- add `<h1>` and `<p>` with some text in your HTML file
- add `font-family: 'Mali', cursive;` to your body.
-  then see how your font change

>Hint: [[CSS#@import]]

###### 2. Custom Media Screen
Customizing media queries in CSS is a crucial aspect of creating responsive designs. You can use media queries to customize styles for different screen sizes. 

To debugging in mobile screen you have to go to developer mode by `right click` and select `Inspect` menu as the following picture (or using `Ctrl + Shift + I`).
![[inspect-menu.png]]
Then click on the device icon inside the red circle. You can toggle it at any time to switch between device mode and full-screen mode.
![[toggle-device-settings.png]]
On `Dimensions: Responsive` menu, you can pick any size of devices from the list.
![[responsive-devices.png]]

Another way, you click on the top bar (arrow 1) or drag (arrow 2) to change the screen width.
![[change-device-screen.png]]

The First suggested device is `iPhone SE` for the smallest device then go to our assignment.

- add some style to `<h1>` and `<p>` such as `color: slategray;` both header and paragraph.
- then use `@media screen` to custom style when screen wider than `768px`, set color to `red`.
- add another `@media screen` to custom style when screen wider than `1024px`, set color to `green`.
- add `@media screen` again to custom style when screen wider than `1440px`, set color to `blue`.
- change your screen width and see the results.

![[media-screen-change.gif]]
If you want background color like GIF above try `rgba(0,0,0,0.1)` and change each unit follow the color `red`, `green`, `blue` to `255` such as for red `rgba(255, 0, 0, 0.1)`.

>Hint: [[CSS#@media]]

###### 3. Custom Font Face
Download all [Custom Font](https://drive.google.com/drive/folders/1GPm59Rv1kROeiTypB6qz1QoRGmo9-fBz?usp=drive_link) for the lesson. At the top of your CSS code (between @import and others) add the following code:
```css
/* Define the English font */
@font-face {
  font-family: 'Custom Font';
  src: url("fonts/Silkscreen-Bold.ttf") format("truetype");
  unicode-range: U+0020-007E; /* Specify the Unicode range for English characters */
}

@font-face {
  font-family: 'Custom Font';
  src: url("fonts/Silkscreen-Regular.ttf") format("truetype");
  unicode-range: U+0020-007E; /* Specify the Unicode range for English characters */
}

/* Define the Thai font */
@font-face {
  font-family: "Custom Font";
  src: url("fonts/MN-MooPing-Bold.ttf") format("truetype");
  unicode-range: U+0E00-0E7F; /* Specify the Unicode range for Thai characters */
}

@font-face {
  font-family: "Custom Font";
  src: url("fonts/MN-MooPing-Regular.ttf") format("truetype");
  unicode-range: U+0E00-0E7F; /* Specify the Unicode range for Thai characters */
}
```

Then try to call the "Custom Font" e.g. `font-family: "Custom Font";`. To see what happens.
- add `<h1>` both "English" and "Thai" language.
- add `<p>` both "English" and "Thai" language.
- inside `<p>` add `<strong>` to wrap some of both "English" and "Thai" language.

![[custom-font-face.png]]

>Hint: [[CSS#@font-face]]

###### 4. Keyframes Animation
- from the previous section, wrap the `<h1>` and `<p>` with `<div>` which use class like `box`.
- add animation slide in into `box` class.

![[animation-slide-in.gif]]

>Hint: [[CSS#@keyframes]]


#css #phase-1 #assignment #css-at-rules
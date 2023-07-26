# simpleLoader

HTML FILE:
1. The HTML document begins with the `<!DOCTYPE html>` declaration.
2. The `<html>` element marks the start of the HTML document.
3. The `<head>` section contains meta tags and links to the CSS file and sets the title of the page.
4. The `<meta name="viewport" content="width=device-width, initial-scale=1.0">` ensures proper rendering on various devices.
5. The `<title>` element sets the title of the page to "Loader".
6. The `<link rel="stylesheet" href="style.css">` links the external CSS file named "style.css" to the HTML document.
7. The `<body>` element starts the body section of the HTML document.
8. The loader is wrapped in a `<section>` element to center it on the page.
9. The `<div class="loader">` contains a series of 20 `<span>` elements, each representing a circle with a custom property "--i" set to values from 1 to 20.
10. CSS styles, defined in the "style.css" file, control the loader's appearance and animation.
11. The loader's animation is achieved using CSS animations and pseudo-elements (::before).
12. The "animateBg" animation provides a color-changing effect to the background of the section.
13. Each circle is positioned absolutely within the loader and rotates at different angles using the custom property "--i".
14. The "animate" animation scales the pseudo-elements (::before) of each circle to create a glowing effect, making the circles appear and disappear smoothly.

CSS FILE:
1. `*`: Targets all elements and sets some common styles to reset their margins, padding, and box-sizing.
2. `section`: Targets the section element containing the loader and sets its properties.
   - `display: flex`: Uses flexbox for layout.
   - `justify-content: center`: Centers the content horizontally within the section.
   - `align-items: center`: Centers the content vertically within the section.
   - `min-height: 100vh`: Sets the minimum height of the section to 100% of the viewport height.
   - `background: #003541`: Sets the background color of the section to a dark teal (#003541).
   - `animation: animateBg 10s linear infinite`: Applies an animation called "animateBg" to create a color-changing effect with a 10-second duration and linear timing.

3. `@keyframes animateBg`: Defines the animation called "animateBg" using `@keyframes`.
   - `0%`: Specifies the starting keyframe of the animation.
      - `filter: hue-rotate(0deg)`: Sets the hue rotation to 0 degrees.
   - `100%`: Specifies the ending keyframe of the animation.
      - `filter: hue-rotate(360deg)`: Sets the hue rotation to 360 degrees, creating a full color cycle.

4. `section .loader`: Targets the loader container inside the section and sets its properties.
   - `position: relative`: Positions the loader container relative to its normal position.
   - `width: 120px`: Sets the width of the loader container to 120 pixels.
   - `height: 120px`: Sets the height of the loader container to 120 pixels.

5. `section .loader span`: Targets the individual circles inside the loader container and sets their properties.
   - `position: absolute`: Positions each circle absolutely within the loader container.
   - `top: 0; left: 0; width: 100%; height: 100%`: Positions each circle to cover the entire loader container.
   - `transform: rotate(calc(18deg * var(--i)))`: Applies a rotation to each circle based on its custom property (--i) value, creating a circular arrangement.

6. `section .loader span::before`: Targets the pseudo-element "before" for each circle and sets its properties.
   - `content: ""`: Adds content to the pseudo-element (a small circle).
   - `position: absolute`: Positions the pseudo-element absolutely within its parent circle.
   - `top: 0; left: 0; width: 15px; height: 15px`: Sets the size and position of the pseudo-element to create a smaller circle.
   - `border-radius: 20%`: Rounds the corners of the pseudo-element, creating a circular shape.
   - `background: #00d0ff`: Sets the background color of the pseudo-element to a bright blue (#00d0ff).
   - `box-shadow`: Adds multiple box shadows to the pseudo-element, creating a glowing effect with varying sizes.
   - `animation: animate 2s linear infinite`: Applies an animation called "animate" to each pseudo-element, with a 2-second duration, linear timing, and infinite repetition.
   - `animation-delay: calc(0.1s * var(--i))`: Delays the start of the animation for each pseudo-element based on its custom property (--i) value.

7. `@keyframes animate`: Defines the animation called "animate" using `@keyframes`.
   - `0%`: Specifies the starting keyframe of the animation.
      - `transform: scale(1)`: Sets the scale of the pseudo-element to its original size.
   - `80%, 100%`: Specifies the ending keyframes of the animation.
      - `transform: scale(0)`: Sets the scale of the pseudo-element to 0, making it disappear.


Output:


<img width="185" alt="image" src="https://github.com/AmishaSharma12002/simpleLoader/assets/92213190/07febe43-11c0-4ef4-90c3-af16e080cb20">

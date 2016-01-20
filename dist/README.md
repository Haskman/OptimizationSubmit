### Running the website
A live version of the project can be accessed on haskman.github.io/optimization.
For offline access:
1) Clone the repository on your PC
2) For the optimized version, which can be accessed on 'dist' folder, the website can be run simply by running index.html on a web browser
3) The original version is located on the 'src' folder and can be accessed the same way



####Steps taken to optimize
1) Image sizes reduced
    - Index page thumbnails compressed using Adobe Photoshop
    - Pizzeria image compressed using Adobe Photoshop
    - A new thumbnail with lower size and resolution created for the index page: pizzeria-mini
2) Render blocking prevented 
    - Render blocking prevented using media queries on the landing page
3) CSS for index page minified.
    - style.css for the landing page minified using an online tool
4) Removed Forced Synchronous Layout for the background moving pizzas
    - Made appropriate changes in views/js/main.js as commented in order to prevent FSL, especially in loops
5) Edited style.css to account for animated elements causing the whole page to print
    - Used 'will-change: transform' so that the browser potentially creates additional layers for smaller elements that change as the user scrolls
    - Added 'transform: translateZ(0)' and 'backface-visibility: hidden' to trigger hardware acceleration
6) Replaced jQuery element access calls with their faster versions
    - Those changes are commented on the code



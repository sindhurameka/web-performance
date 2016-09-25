# Website Performance Optimization Project

## Instructions to run the application

### Checking page speed score of index.html

1. Unzip and open the file SindhuraMeka_Project4
2. Open terminal and start python server in the project folder
   ```bash
  $> cd /path/to/your-project-folder
  $> python -m SimpleHTTPServer 8080
  ```
3. Download and install [ngrok](https://ngrok.com/) in the top level of the project folder.
  ``` bash
  $> cd /path/to/your-project-folder
  $> ./ngrok http 8080
  ```
4. Copy the public URL ngrok gives you in the Google PageSpeed Insights Website (https://developers.google.com/speed/pagespeed/insights/)
5. You can see the pagespeed score for desktop and mobile version of the page

### Checking the Optimizations made to pizza.html

#### Checking 60 FPS
1. Open the file SindhuraMeka_Project4
2. In the project folder open views/pizza.html using the browser
3. Open google developer tools when on the page
4. Click on the timeline tab and press the record start button and scroll the page and stop the recording
5. Once the recording is stopped a timeline will appear on the screen you can see the Frames per second rate from the fps column.

#### Checking the time to resize pizzas

1. Open the file SindhuraMeka_Project4
2. In the project folder open views/pizza.html using the browser
3. Open google developer tools when on the page
4. Click the console tab and move the pizza resize slider on the screen to see the timing it takes to resize the pizzas

## Optimization made in the project

### To increase the pagespeed score

* Compressed and resized the images
* Eliminated render-blocking JavaScript and CSS in above-the-fold content.
   * Inlined the CSS.
   * Used media=print attribute for print.css link.
   * Used async attribute for script tag.
* Minified the index.html File

### For getting rid of Jank in pizza.html

* Made changes to updatepositions fuction in views/js/main.js file
* Used getElementbyId or getElementsbyClassName instead of QuerySelectors when necessary to optimize the performance.
* Got the inloop value constant calculations ouside the loop and stored them in variables and used those variables in loop
* Also made changes to the number of pizzas to show based on viewport sizes.

### Decrease the time to resize pizza

* Changes made to resizepizza fuction
* Used getElementbyId or getElementsbyClassName instead of QuerySelectors when necessary to optimize the performance.
* In ChangePizzaSizes fuction got the inloop value constant calculations ouside the loop and stored them in variables and used those variables in loop.



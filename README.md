## Website Performance Optimization portfolio project

###To run the application -
    - Download the project files from the github repository and unzip them. Then open index.html in any browser.
    - Go to http://apoorvksingh.github.io/optimize_website/

##Optimizations -

###index.html
    - The contents of the css file brought within the HTML file, specified in <head> (avoid render blocking)
    - The url referenced for the Google fonts was brought within the <style> tag
    - THe images were optimized to the best possible size and resolution, resulting in saving a lot of the data required to be loaded
    - Both the script files were defined as async (avoid parser blocking)
    - The images that were referenced as external url were downloaded to the local directory and accessed locally to remove external calls


###main.js - JS file for pizzas
    - Replace querySelector with getElementById()
    - Replace querySelectorAll with getElementsByClassName()
    - In the function changePizzaSizes(size), get variable assignments out of the loop to avoid the overhead of assigning them in each loop run
    - Line : 542 , Declaration of movingPizza brought outside the loop to avoid overhead of calling the function each time
    - Line : 543 , Variable elem initialised within the for loop declaration to avoid it being created every time the loop runs
    - Line : 541 , Ran the for loop 48 times instead of 200

###views/css/styles.css
    - Added Transform and backface-visibility properties to enable harware accelerated CSS
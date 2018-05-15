# discourse-spinner-theme-component
Add a loading spinner to the initial discourse load.

This assumes a light theme with a white background.  If your theme uses another color background, change the CSS file to include a different color.

## CSS Explaination

`#main {background: white;}`

The main container is naturally a higher z-index than the header so this step ensures that once it loads, it will cover up the spinner.

## Header Explaination

`<div class="spinner" style="margin: 70px calc(50vw - 19px); position: absolute;"></div>`

This loads the built-in discourse CSS spinner, but feel free to use another if you’d prefer.

This code will center the spinner on your screen and place it high up enough to not create a duplicate spinner when doing page loads later on. The calc is half of the 30px spinner width (15px), plus the 4px border.

## Discuss
https://meta.discourse.org/t/found-a-workable-css-hack-to-show-spinner-loader-on-slow-initial-load/84199

Modified to work better with express/connect compiler. 

* All mixins are now functions to prevent unused mixins from polluting compiled scripts.
* Use line comments vs block comments.
* Added box-sizing mixin

    // LESS

    h1 {
      .box-sizing;
    }

    h2 {
      .box-sizing(content-box);
    }

    /* Compiled CSS */

    h1 {
      -moz-box-sizing: border-box;
      -webkit-box-sizing: border-box;
      box-sizing: border-box; 
    }

    h2 {
      -moz-box-sizing: content-box;
      -webkit-box-sizing: content-box;
      box-sizing: content-box; 
    }

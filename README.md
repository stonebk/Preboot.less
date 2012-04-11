Modified to work better with express/connect compiler. 

### Changes

* All mixins are now functions to prevent unused mixins from polluting compiled scripts.
* Use line comments vs block comments.
* Added box-sizing mixin
* Added user-select mixin

### Mixins

Box Sizing:

    /* LESS */
    
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

User Select:

    /* LESS */
    
    h1 {
      .box-sizing;
    }
    
    h2 {
      .box-sizing(text);
    }
    
    /* Compiled CSS */
    
    h1 {
      -webkit-user-select: none;
      -khtml-user-select: none;
      -moz-user-select: none;
      -o-user-select: none;
      user-select: none;
    }
    
    h2 {
      -webkit-user-select: text;
      -khtml-user-select: text;
      -moz-user-select: text;
      -o-user-select: text;
      user-select: text;
    }

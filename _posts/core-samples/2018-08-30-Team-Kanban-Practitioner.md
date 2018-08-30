---
layout: post
category : Trainings
tagline: "Team Kanban Practitioner"
tags : [Kanban, TKP]
img : syntax-hightlight.jpg
img2 :
img3 :
author : Pablo Domingo
title2 : Esta es una pequeña descripción del contenido del curso
title3 :
css:
js:
bgcolor: ff5a71
keywords: kanban, flow, bottlenecks, certification
canonical: https://fullit.github.io

---
{% include JB/setup %}

Hello world! Is the first post on helium jekyll
<!--more-->
# Aprende a trabajar en equipo

Lorem ipsum dolor sit amet, consectetur adipiscing elit. Phasellus consequat luctus neque eget commodo. Sed a molestie lorem. Fusce lectus mauris, vulputate sollicitudin ullamcorper ut, semper at risus. Nunc porta ut velit non fringilla. Pellentesque egestas eros vitae suscipit imperdiet. Cras imperdiet a velit sit amet placerat. Morbi dolor quam, semper ac venenatis ac, pretium at ex. Suspendisse fermentum mi sit amet risus congue ullamcorper. Sed sed ultrices libero. Cras pulvinar dui efficitur felis maximus, ac dictum leo egestas. Pellentesque ut dictum odio. Aliquam varius viverra orci, quis blandit mi blandit vitae. Donec non semper augue, ut consectetur ligula. Aenean tellus tortor, sagittis sed iaculis quis, imperdiet et ex. Mauris id libero sed diam euismod pharetra.

Mauris nec pulvinar elit, in fermentum leo. Curabitur volutpat ullamcorper diam id dapibus. Donec dolor eros, dictum vitae quam sit amet, imperdiet dapibus libero. Nullam vel ligula non velit tincidunt volutpat. Maecenas at magna enim. Nunc quis molestie lectus. Maecenas facilisis finibus consequat.

Curabitur vitae elementum nulla, at cursus elit. Suspendisse elementum auctor lorem eu sodales. Curabitur accumsan efficitur maximus. Ut purus lacus, dapibus ut elit vitae, imperdiet ultrices diam. Donec pharetra quis urna et auctor. Sed non augue vel lacus scelerisque mattis. In ac eros quis felis laoreet luctus vitae eget libero.

Sed egestas lectus urna, et lacinia nulla suscipit nec. Sed sed consequat nulla. Morbi lobortis ex tellus, quis aliquam magna gravida quis. Ut mattis dui nec euismod tempor. Ut sit amet felis tincidunt, ultrices ligula eu, dapibus nulla. Aliquam efficitur magna in elit placerat, vel placerat augue interdum. In hac habitasse platea dictumst. Sed ac mollis lacus. Praesent eleifend justo ut nunc fermentum, eget luctus dui ultricies.

Integer interdum fringilla commodo. Integer finibus purus diam, at gravida metus interdum ac. Curabitur posuere, felis facilisis consectetur convallis, enim nulla ultricies nisi, at pretium sapien lorem ac diam. Integer ac ex consequat, facilisis justo sit amet, auctor quam. Curabitur luctus suscipit ante sed aliquet. Donec non molestie sapien, ut pellentesque odio. In lobortis porta auctor. Sed eu convallis est, eget ultricies ligula. Maecenas facilisis laoreet velit, eget rutrum ligula malesuada in. Vestibulum sapien lacus, congue ut mi ut, faucibus dapibus massa. Morbi vel ligula eget lacus vehicula tincidunt.

# Aprende a observar cómo tu trabajo trabaja por ti

<!--more-->
## ¿A quien va dirigido?

The following example shows how to highlight a piece of code throughout the use of Javascript:

{% highlight javascript %}

    /*jshint browser: true, strict: true, undef: true */
    /*global define: false */

    ( function( window ) {

    'use strict';

    // class helper functions from bonzo https://github.com/ded/bonzo

    function classReg( className ) {
      return new RegExp("(^|\\s+)" + className + "(\\s+|$)");
    }

    // classList support for class management
    // altho to be fair, the api sucks because it won't accept multiple classes at once
    var hasClass, addClass, removeClass;

    if ( 'classList' in document.documentElement ) {
      hasClass = function( elem, c ) {
        return elem.classList.contains( c );
      };
      addClass = function( elem, c ) {
        elem.classList.add( c );
      };
      removeClass = function( elem, c ) {
        elem.classList.remove( c );
      };
    }
    else {
      hasClass = function( elem, c ) {
        return classReg( c ).test( elem.className );
      };
      addClass = function( elem, c ) {
        if ( !hasClass( elem, c ) ) {
          elem.className = elem.className + ' ' + c;
        }
      };
      removeClass = function( elem, c ) {
        elem.className = elem.className.replace( classReg( c ), ' ' );
      };
    }

    function toggleClass( elem, c ) {
      var fn = hasClass( elem, c ) ? removeClass : addClass;
      fn( elem, c );
    }

    var classie = {
      // full names
      hasClass: hasClass,
      addClass: addClass,
      removeClass: removeClass,
      toggleClass: toggleClass,
      // short names
      has: hasClass,
      add: addClass,
      remove: removeClass,
      toggle: toggleClass
    };

    // transport
    if ( typeof define === 'function' && define.amd ) {
      // AMD
      define( classie );
    } else {
      // browser global
      window.classie = classie;
    }

    })( window );

{% endhighlight %}

## Code highlighting with rounge and Prism

Another snippet rendered with the CSS code syntax:


``` CSS
    @import url('https://fonts.googleapis.com/css?family=Alfa+Slab+One|Gentium+Book+Basic');
    /* Reset CSS
     * --------------------------------------- */
    body,div,dl,dt,dd,ul,ol,li,h1,h2,h3,h4,h5,h6,pre,
    form,fieldset,input,textarea,p,blockquote,th,td {
        padding: 0;
        margin: 0;
    }
    a{
        text-decoration:none;
    }
    table {
        border-spacing: 0;
    }
    fieldset,img {
        border: 0;
    }
    address,caption,cite,code,dfn,em,strong,th,var {
        font-weight: normal;
        font-style: normal;
    }
```
## Using snippet rendered with the HTML code syntax

``` HTML

<div id="fullpage">
    <div data-anchor="0section" class="section" id="section0">

        <h1 class="heavy">Ready to follow <br />your <span class="pink">dreams?</span></h1>
        <br /><h2 class="large-blur">
            <span class="highlight-container"><span class="highlight">
                Put your dreams on first and follow that!
            </span></span>

            <br />



        </h2>
            <div class="intro-scroll-down">
              <a data-menuanchor="1section" href="#1section">
                <span class="mouse">
                  <span class="mouse-dot"></span>
                </span>
              </a>
            </div>



    </div>
```

**Check the markdown of this example in order to fully comprehend the correct syntax.**

[Here](https://github.com/sentenza/sentenza.github.io/issues/1) you can find more detailed information.

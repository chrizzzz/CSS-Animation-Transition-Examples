# CSS Animation and Transitions Examples

## Table of Contents

- [Hover Animation](#hoverAnimation)
- [Fade-In Animation](#FadeInAnimation)
- [Loading-Spinner Animation](#LoadingSpinner)

## <a name="hoverAnimation"></a> Hover Animation

<button class="myButton">
click me!
</button>

<style>
  .myButton {
    /* innen Abstand zum Text  */
    padding: 10px 20px;
    /* Schrift und Hintergrundfarbe  */
    color: white;
    background-color: grey;

    /* button mit abgerundeten Ecken  */
    border-radius: 4px;
    /* button ohne sichtbare Umrandung  */
    border: none;

    transition: background-color 250ms ease-in 100ms;
  }

  .myButton:hover {
    background-color: red;
  }
</style>

```html
<button class="myButton">
  click me!
</button>

<style>
  .myButton {
    /* innen Abstand zum Text  */
    padding: 10px 20px;
    /* Schrift und Hintergrundfarbe  */
    color: white;
    background-color: grey;

    /* button mit abgerundeten Ecken  */
    border-radius: 4px;
    /* button ohne sichtbare Umrandung  */
    border: none;
  }

  .myButton:hover {
    background-color: red;
  }
</style>
```

## Fade-In Animation

<a name="FadeInAnimation"/>

<a onclick="toogleFadeIn();">Toogle Fadein Animation</a>
<button class="fadeInButton">
click me!
</button>

<script>
    function toogleFadeIn () {
        const fadeInButton = document.getElementsByClassName("fadeInButton")[0];
        if(fadeInButton.classList.contains("fadeInButton--active")){
            fadeInButton.classList.remove("fadeInButton--active");
        }else{
             fadeInButton.classList.add("fadeInButton--active");
        }
    }
</script>

<style>
  .fadeInButton {
    /* innen Abstand zum Text  */
    padding: 10px 20px;
    /* Schrift und Hintergrundfarbe  */
    color: white;
    background-color: grey;

    /* button mit abgerundeten Ecken  */
    border-radius: 4px;
    /* button ohne sichtbare Umrandung  */
    border: none;

    transform: translateY(30px);
    opacity: 0;
    transition: transform 500ms ease-in, opacity 500ms ease-in;
  }


.fadeInButton--active {
  transform: translateY(0);
  opacity: 1;
}
</style>

```html
<button class="myButton">
  click me!
</button>

<style>
  .myButton {
    /* innen Abstand zum Text  */
    padding: 10px 20px;
    /* Schrift und Hintergrundfarbe  */
    color: white;
    background-color: grey;

    /* button mit abgerundeten Ecken  */
    border-radius: 4px;
    /* button ohne sichtbare Umrandung  */
    border: none;
  }

  .fadeInButton {
    /* innen Abstand zum Text  */
    padding: 10px 20px;
    /* Schrift und Hintergrundfarbe  */
    color: white;
    background-color: grey;

    /* button mit abgerundeten Ecken  */
    border-radius: 4px;
    /* button ohne sichtbare Umrandung  */
    border: none;

    transform: translateY(30px);
    opacity: 0;
    transition: transform 500ms ease-in, opacity 500ms ease-in;
  }

  .fadeInButton--active {
    transform: translateY(0);
    opacity: 1;
  }
</style>
```

## <a name="LoadingSpinner">Loading-Spinner</a>

<div class="loadingSpinnerContainer">
<div class="loadingSpinner">
  <div class="border">
    <div class="center"></div>

  </div>
</div>
<div>
<div>
Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet. Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam nonumy eirmod tempor invidunt ut labore et dolore magna aliquyam erat, sed diam voluptua. At vero eos et accusam et justo duo dolores et ea rebum. Stet clita kasd gubergren, no sea takimata sanctus est Lorem ipsum dolor sit amet.

Duis autem vel eum iriure dolor in hendrerit in vulputate velit esse molestie consequat, vel illum dolore eu feugiat nulla facilisis at vero eros et accumsan et iusto odio dignissim qui blandit praesent luptatum zzril delenit augue duis dolore te feugait nulla facilisi. Lorem ipsum dolor sit amet,

</div>
</div>
<style>
@keyframes spinner {
from {
transform: rotate(0deg);
}
to {
transform: rotate(360deg);
}
}
.loadingSpinnerContainer{
position: relative;
height: 250px;
width: 100%;
}
.loadingSpinner {
position: absolute;
top: 0;
left: 0;
width: 100%;
height: 100%;
opacity: 0.75;
overflow: hidden;
z-index: 1;
background-color: #3d3e3f;
display: flex;
align-items: center;
justify-content: center;
}
.border {
width: 100px;
height: 100px;
border-radius: 100px;
background-image: linear-gradient(to right, #870a0a 5%, red 10%, yellow);
padding: 4px;
animation-name: spinner;
animation-duration: 1s;
animation-iteration-count: infinite;
animation-direction: alternate;
}
.center {
width: 100%;
height: 100%;
border-radius: 100%;
background-color: #3d3e3f;
}
</style>

```html
<div class="loadingSpinnerContainer">
  <div class="loadingSpinner">
    <div class="border">
      <div class="center"></div>
    </div>
  </div>
  <div>
    <div>
      text
    </div>
  </div>
  <style>
    @keyframes spinner {
      from {
        transform: rotate(0deg);
      }
      to {
        transform: rotate(360deg);
      }
    }

    .loadingSpinner {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      opacity: 0.75;
      overflow: hidden;
      z-index: 1;
      background-color: #3d3e3f;
      display: flex;
      align-items: center;
      justify-content: center;
    }
    .border {
      width: 100px;
      height: 100px;
      border-radius: 100px;
      background-image: linear-gradient(to right, #870a0a 5%, red 10%, yellow);
      padding: 4px;
      animation-name: spinner;
      animation-duration: 1s;
      animation-iteration-count: infinite;
      animation-direction: alternate;
    }
    .center {
      width: 100%;
      height: 100%;
      border-radius: 100%;
      background-color: #3d3e3f;
    }
  </style>
</div>
```

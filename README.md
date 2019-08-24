# Pure CSS slider
20 lines of code - that's it. Please include credit.

```
/*
Author: Rien Heuver, rienheuver@gmail.com
Clean Slider, this is all that is needed
*/
.slider {
    display: grid;
    grid-template-columns: 1fr;
    overflow: hidden;
    width: 100%;
    perspective: 400px;
}

.slide {
    grid-column: 1/2;
    grid-row: 1/2;
    transition: transform 300ms ease-in-out;
}

.slide-next {
    transform: translateX(100%);
}

.slide-prev {
    transform: translateX(-100%);
}
```
Also as gist: https://gist.github.com/rienheuver/df5ff228c6883f96f47f94a6d6c49a2d

## Usage
An example is provided in the html of this repository.
The following HTML creates the most simple slider with 3 slides. Of course any number of slides is supported. In this example, the second slide is currently active. All slides with class `slide-prev` will be to the left by default, all slides with class `slide-next` will be to the right. To activate a certain slide, simply remove the `slide-prev` or `slide-next` class. To deactivate a slide, add the `slide-prev` or `slide-next` class, dependent on where the slide should go.
```
<div class="slider">
    <div class="slide slide-prev">Slide 1</div>
    <div class="slide">Slide 2</div>
    <div class="slide slide-next">Slide 3</div>
</div>
```

## Customisation
Anything about this slider can be customised. If you have suggestions or requests for examples, please contact me.

### Fading slides
Remove the last 7 lines of code that handle the transforms on `prev-slide` and `next-slide` and add the following code:
 ```
 .prev-slide, .next-slide {
     opacity: 0;
 }
 ```
 Also, change the transition-property on `.slider`  from
 ```
 transition: transform 300ms ease-in-out
 ```
 into
 ```
 transition: opacity 300ms ease-in-out
 ```

 ## Author
 Rien Heuver, rienheuver@gmail.com

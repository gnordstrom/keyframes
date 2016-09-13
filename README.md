# lesson-keyframes

##objective
We're going to try to replicate this: https://spencerkekauoha.github.io/lesson-waves-keyframes/
We're going to do it with only using css, and we'll learn how to use @keyframes. http://www.w3schools.com/cssref/css3_pr_animation-keyframes.asp

##step one
create a index.html file.
create a style.css file.

#step two
 add both css files to your html.
 *index.html*
 `   <link rel="stylesheet" href="reset.css" media="screen" title="no title">
     <link rel="stylesheet" href="style.css" media="screen" title="no title">
`
make sure the last linked css file is the one you want to have the final say.

#step three
add the images in the img folder to the index. place them in a container with the class 'wave-container'.
give the the back wave a class of 'backwave' and thre front wave a class of 'frontwave'
  `<section class="wave-container">
      <div class="backwave">
        <img src="/img/great_wave_backwave.png" alt="wavy wavy" />
      </div>
      <div class="frontwave">
        <img src="/img/great_wave_frontwave.png" alt="wavy wavy" />
      </div>
    </section>`

#step four
add the great_wave_background.png image to the wave-container's background. try to get the images to look like one image.


#step five
lets add some keyframes. keyframe rules let us describe when we want css animations to happen. For our example we're going to change where our images should be position.  

*style.css*
`@keyframes backWaves {
  0% {top: 30px}
  50% {top: 20px}
  100% {top: 30px}
}

@keyframes frontWaves {
  0% {top: 0px}
  50% {top: 10px}
  100% {top: 0px}
}`


#step six
 Now lets use our keyframes and add the animation property to both our backwave and frontwave. For our frontwave we're going to use the frontWaves keyframe and it should last five seconds and loop an infinite amount of times
 `  animation: frontWaves 5s infinite;`

For our backwave we'll use the backWaves keyframe for the same duration and loops.


#step black diamond

Now both waves should be moving. if you notice at the bottom there is some empty space below where the bottom image will move into sometimes. Try putting a frame around the gaps, or hide the overflow on the body to make our animation seamless. you can check my solution branch for an example of working code. 

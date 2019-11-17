## Explanation
#### CSS for animated bouncing loader.
```
.loader {
  display: flex;
  justify-content: center;
  align-items: center;
}
``` 
``` display: flex; ``` property will place the bouncing page loader in the middle of the page both horizontally and vertically.
#### Loader circles
```
.loader > span {
  background: #FAD000;
  border-radius: 50%;
  margin: 5rem 0.5rem;
  animation: bouncingLoader 0.6s infinite alternate;
}
.loader > span:nth-child(2) {
  animation-delay: 0.2s;
}
.loader > span:nth-child(3) {
  animation-delay: 0.4s;
}
```
Each loader circle has ```width: 1rem;``` and ```height:1rem;``` with ```#FFB651``` color. By default, the shape of page loader is in square. To give it a circular shape the border-radius is set to 50%.
#### Creating Animation Keyframe(```@keyframes```)
> Keyframes are used to define the animation behavior and give us complete control of one cycle of a CSS animation.
> Inside a ```@keyframe``` rule, we use the keywords ```from``` and ```to``` in order to specify a starting and ending point for animation. Equivalently, we can also use **0% * for ```from``` which depicts the starting point and *100%** for ```to``` depicting the ending point of animation.
> A simple representation of these percentages is shown below:
> ``` @keyframes animationNameHere {
>  0% { opacity: 1; }
>  30% { opacity: 0.75; }
>  50% { opacity: 0.5; }
>  100% { opacity: 0.25; }
> }
#### Define the animation called bouncingLoader
```@keyframes bouncingLoader {
  from {
    width: 0.1rem;
    height: 0.1rem;
    opacity: 1;
    transform: translate3d(0);
  }
  to {
    width: 1rem;
    height: 1rem;
    opacity: 0.1;
    transform: translate3d(0, -1rem, 0);
  }
}
```
#### Using Animation Delay with Keyframe
``` 
animation: bouncingLoader 0.6s infinite alternate;
```
Styling the element that is to be animated with ```animation``` property and/or its sub-properties. Using this property we can control the ```timing```, ```duration```, and other details of animation.
> ```animation: animation-name, animation-duration, animation-iteration-count, animation-direction;```

- **```animation-name```**: Defines the name of your animation which is ```loader``` in my case.
- **```animation-duration```**: Configures the length of time which your animation will take to complete one cycle.
- **```animation-iteration-count```**: Tells how many times you want your animation cycle to play before it stops.
- **```animation-direction```**: Defines that in which direction is your animation going to play.
---
## Demo
---

#### Source : [Bouncing Loader](https://scotch.io/tutorials/create-a-bouncing-page-loader-with-css3-animations)

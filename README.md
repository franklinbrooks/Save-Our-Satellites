# Save Our Satellites Game

[Play it here!](http://baliff-otter-21637.bitballoon.com/)

### Screen shot of inspiration for project: 
  ![StarMaster by Activision 1982](http://www.8-bitcentral.com/images/reviews/atari2600/starmaster2600Screen.jpg)

###My whiteboard for project
  ![Whiteboard of project](https://github.com/franklinbrooks/WDI_HAKUNA_MATATA/blob/master/Project1GA/20161215_151913.jpg)

###My implementation of project
  ![As deployed on my GitHubPage](https://353a23c500dde3b2ad58-c49fe7e7355d384845270f4a7a0a7aa1.ssl.cf2.rackcdn.com/58573994c4d9cc6dc44bf258/screenshot.png)

### Technologies Used
- HTML
- CSS
- JavaScript

### Code Example quote
```javascript
let checkIt = function() {
  const gameBoard = document.getElementById("game");
  let target = document.getElementById('target1');
  let friendly = document.getElementById('satellite');
  el = target.getBoundingClientRect();
  la = friendly.getBoundingClientRect();
  let left = el.left + window.scrollX;
  let laLeft = la.left + window.scrollX;
  let top = el.top + window.scrollY;
  let laTop = la.top + window.scrollY;
  console.log(`laLeft is ${laLeft} and laTop is ${laTop}`);
  if ((left > 582 && left < 622) && (top > 230 && top < 270)) {
    score++;
    enemies--;
    outputNewMessages();
    gameBoard.removeChild(target);
    explodeIt();
    determineIt();
  } else if ((laLeft > 600 && laLeft < 650) && (laTop > 225 && laTop < 265)) {
    satellites = satellites - 1;
    outputNewMessages();
    gameBoard.removeChild(friendly);
    explodeIt();
    determineIt();
  }
}
````
### Build Strategy
This game uses JavaScript to handle scoring and logic, and to bind player keyboard events to screen events. JS also interacts with HTML and CSS to manage visual elements.

### Contributing
This project was developed as part of the Web Development Immersive program at General Assembly in NYC, December 2016. My mentor for this build was [Joe Keohan](joe.keohan@generalassemb.ly), who provided valuable guidance throughout the build cycle.  Thanks, Joe!

### Minimum Viable Product
- One moving element which crosses center crosshairs of screen
- Ability to shoot it
- Increment score

### Improvements on MVP
- CSS styling to improve UX
- Addition of friendly units
- Addition of limited fuel variable
- Crosshairs able to detect friendly vs enemy units

### Possible Future Improvements 
  1. Ablity to move UDLR to move target into crosshairs
  1. Ability to take damage from collision with element
  1. Ability to take weapon damage from element
  1. Addition of additional quantity of moving elements
  1. Ability to accelerate speed
  1. Additional rounds of increased difficulty
  1. Ability to track player stats over successive rounds
  1. Addition of minimap to show location

### Author
  [Franklin Brooks](http://www.franklinchristopherbrooks.com) 

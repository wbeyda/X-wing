# X-wing
X-Wing game in THREE.JS

BDD user stories but really just dev tasks

### Canvas detect

GIVEN HTML doc search dom for Canvas 

WHEN mouse is over canvas 

THEN click and return status


### Load THREEJS

GIVEN an HTML canvas

WHEN DOM is ready load THREEJS

THEN return THREE


### Set constant values for game objects

GIVEN a THREEJS object

WHEN THREE is ready

THEN instantiate game constants


### Initialize THREE

GIVEN document set size, camera, scene, background, models, touch display

WHEN init() method is called 

THEN render background and models in scene


### Set camera position

GIVEN initialized Three instance and calculated aspect ratio of screen display

WHEN camera is positioned

THEN set camera in z axis


### Set Scene and fog

GIVEN camera set scene object 

WHEN scene is init

THEN set scene fog


### Initialize background stars

GIVEN Initialized assets

WHEN background image is loaded

THEN render stars in random positions


### Light the scene

GIVEN scene and background is loaded

WHEN new THREE ambient, point and spotlights lights are added for distance and x-wing shadow 

THEN add lights to scene object season to taste


### Load trench model

GIVEN trench model create loader

WHEN loader is ready

THEN add model to scene and set positions


### Lasers

GIVEN THREE object

WHEN object is instantiated create red lasers

THEN add laser to scene and hide visibility


### Make Stars

GIVEN THREE vec3 geometry particle

WHEN particle is available loop through 100+ and randomize positions

THEN push particles to array and add particle texture to gemoetry mesh


### Set Stars position

GIVEN particle array 

WHEN create new THREE particleSystem

THEN set starts position and add to scene


### Create instruction menu

GIVEN new game instance

WHEN mouse or touch

THEN hide instructions and start game


### Create Game Over menu

GIVEN Game Over menu

WHEN game instance ends

THEN display Game Over menu


### Restart Game

GIVEN end of game and Game Over menu

WHEN Game over menu is displayed listen for mouse click

THEN Destroy Three instance from memory and instantiate a new instance 


### X-Wing Loaded

GIVEN X-Wing Model

WHEN Trench model is loaded

THEN load X-Wing Model to scene


### X-wing thrusters

GIVEN loaded Xwing Model

WHEN X-wing is visible add thruster sprites

THEN attach thrusters as child object of X-wing


### Spawn Trench obstacles

GIVEN Trench 

WHEN X-Wing is running

THEN Spawn obstacle from obstacle abstract factory 


### Trench Obstacle factory

GIVEN a pool obstacles generate random obstacles and positioning

WHEN obstacle is called from pool create, position and display obstacle  

THEN when obstacle is off camera destroy object


### Player controls

GIVEN a running game

WHEN up, down, left right is pressed X-wing moves in expected directions

THEN if right click is pressed X-wing manuvers sideways state


### Game Loop

GIVEN Game has started

WHEN instruction menu is hidden and all THREE objects are loaded

THEN X-wing starts in default position and trench position movement starts


### Game Loop collision

GIVEN a Running game 

WHEN X-wing collides with obstacle

THEN X-wing explodes player isDead and returns to menus


### Explosion

GIVEN explosion

WHEN set ship and thruster visibility to False, create particle array

THEN scale, position, rotate and alphablend particles, possibly shake camera

THEN reset explosion particles, set visibility to False and show game over menu


### Fire Lasers

GIVEN mouse down and running game

WHEN mouse is pressed during running game 

THEN lasers fire and blaster sound is played


### Laser factory

GIVEN fire clock is ready

WHEN lasers are ready play blaster sound, get position and rotation of X-Wing 

THEN make lasers visable and animate begining to end position callback on complete and remove visibility reset fire clock


### Win Game

GIVEN play clock has ran out a final obstacle is created (death star weakness)

WHEN death star weakness is observed and lasers are fired

THEN show cutscene video roll credits


Nice to haves:

    post-processing effects maybe some annoying lens flares for an Abrahms mode
    
    post-processing effects maybe some film grain for Lucas mode
    
    new life blink invincible
    
    play credits in classic star wars fonts
    


    

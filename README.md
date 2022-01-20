# Physics-library-for-Decentraland
How to add [Cannon-ES](https://github.com/pmndrs/cannon-es) library to SDK.



[Awesome Repository](https://github.com/decentraland-scenes/Awesome-Repository). - There are a few examples of using a physics engine in Decentraland. [Billiard Game](https://play.decentraland.org/?island=Ioixl&position=119%2C-26&realm=dg), [Shooting game 1](https://github.com/decentraland-scenes/shooting-range-advanced), [Shooting game 2](https://github.com/decentraland-scenes/coconut-shy), [Shooting game 3](https://github.com/decentraland-scenes/tin-can-alley),  [Car Scene](https://github.com/decentraland-scenes/cannon-car-example-scene), [Frisbee Throwing](https://github.com/decentraland-scenes/websocket-frisbee), [BasketBall](https://github.com/decentraland-scenes/websocket-basket). 

All these examples use [cannon.js](https://github.com/schteppe/cannon.js) library to implement physics on the scene, which is outdated and hasn’t maintance since 2016. There are a lot of bugs and shortcomings. 

[Cannon-ES](https://github.com/pmndrs/cannon-es) is the fork of “cannon.js”, with improvements and recently updated.  

So what do we need to add it to SDK? A few steps: 


1. **Install cannon-es**

Add to “package.json”, cannon-es as dependency to your project and run ```npm install```


2. **Add the source file to  “include” section of tsconfig.json**



3. **Import it with absolute path.**


 


**CORRECT:** 
```
import {World} from "./node_modules/cannon-es/dist/cannon-es";
```
**INCORRECT:**
```
import {World} from "cannon-es";
```

<img src="http://www.gesturekit.com/wp-content/uploads/2014/05/colash_largo.png" alt="GestureKit Technology">

# Gesture Action Take Selfie For RKT Launcher.

> An action for Android taking a picture with a gesture and storing it on the hdcard.

You can see the selfie working on RKT Launcher, check the [PLAY STORE](https://play.google.com/store/apps/details?id=com.roamtouch.gesturekit.rktlauncher).

## Setup

### Set the Action Gesture once GestureKit is loaded. 

Follow the [Andoid Addon Guide](http://www.gesturekit.com/learn/android-addon/) to set the GestureKit library running. 

With the setGestureKitListener interface you can listen to loaded method and set the action GestureActionTakeSelfie to take aselfie. 

```
	//Implement GestureAction Plugin for taking selfie.		
	this.gestureKit.setGestureKitListener(new GestureKitListener() {
		@Override
		public void onGestureKitLoaded() {
			GestureKitPlugins.getInstance().setAction(	
					new GestureActionTakeSelfie (mActivity), "Selfie"); 				
			};  			
	});	
```

## How it works


GestureActionTakeSelfie implements GKActionInterface that exposes the gesture name with getActionID(). 

Once a gesture is recognized if it matches the GKAction name in this case "Selfie", when the gesture is recognized with that given name the onGestureRecognized method is called.  

## Maintained by
- Jose Vigil
[Facebook](https://www.facebook.com/jose.vigil.1973) | [Twitter](https://twitter.com/JoseVigil) | [About](http://about.me/josevigil) | [LinkedIn](https://www.linkedin.com/in/josemanuelvigil) 

## Credits

<img src="http://www.roamtouch.com/wp-content/uploads/2014/06/logo.png" width="200" alt="RoamTouch logo">

[RoamTouch](http://roamtouch.com)

<img src="http://www.gesturekit.com/wp-content/uploads/2014/05/logogkblue.png" width="200" alt="RoamTouch logo">

[GestureKit](http://www.gesturekit.com)

## License
Licensed under Apache v2 License.

Copyright (c) 2014 [RoamTouch](http://github.com/RoamTouch). 

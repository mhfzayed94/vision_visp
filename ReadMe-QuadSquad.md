
# QR-Code Automatic finder and tracker
## steps to do:-
1. clone this Repo and add it as submodule to the project.
2. A branch called "quad-melodic" has been created for us to work on it and modfy it if needed.
3. switch to this branch within the submodule by navigate to the submodule and 
```bash
git checkout quad-melodic
```

## Usage
for starting the auto-tracker for the QR-code using your private camera:-
1. navigate to the submodule
```bash
cd vision_visp
```
2. launch the tracker file
```bash
roslaunch visp_auto_tracker/launch/tracklive_usb.launch 
```
3. trigger the camera with the attached QR-Code

## Important topics
### /visp_auto_tracker/status
this topic return the status of tracking.

* it's value is 3 if the camere can detect the qr-code and 1 if not.
* message type: std_msgs/Int8

### /visp_auto_tracker/object_position
* this topic gives the position and the pose off the qr-code
* message type: geometry_msgs/PoseStamped
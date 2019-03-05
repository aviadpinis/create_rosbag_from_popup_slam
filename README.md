# create_rosbag_from_popup_slam

## create rosvag for popup slam:
https://github.com/shichaoy/pop_up_slam

## it's possible create rosbag from images ot videos:
* Parameters:
1. path for images/video.
2. out file rosbag.
3. topic.
4. format for img.
5. id for msg image.

### example for images:
* Appears also in the notebook 
newRosBagName = "newName.bag"
  with rosbag.Bag(newRosBagName, 'w') as outbag:      createRosbagFromImages('../../src/data/Images/almostrectangle/almostrectangle_orginal/',outbag,'/rect_color_raw','bgr8','camera_rgb_optical_frame')    createRosbagFromImages('../../src/data/Images/almostrectangle/almostrectangle_segmentation/',outbag,'/cnn_label','mono8','openni_rgb_optical_frame')    
  
### example for video:
* Appears also in the notebook 
name = "../../src/rosbag2video/galaxy360.bag"
with rosbag.Bag(name, 'w') as outbag:
    CreateRosbagFromVideo('../../src/data/Video/galaxy360_rotate.avi',outbag,'/rect_color_raw','bgr8','camera_rgb_optical_frame')
    CreateRosbagFromVideo('../../src/data/Video/galaxy360_segmentation.avi',outbag,'/cnn_label','mono8','openni_rgb_optical_frame')    

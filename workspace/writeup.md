# Writeup: Track 3D-Objects Over Time

Please use this starter template to answer the following questions:

### 1. Write a short recap of the four tracking steps and what you implemented there (filter, track management, association, camera fusion). Which results did you achieve? Which part of the project was most difficult for you to complete, and why?

I implemented the Extended Kalman Filter with predict and update steps using jacobian for non-linear update and linear matrix H for lidar.

After that I wrote the track management module that initializes new tracks with measurements and deletes tracks as well.

Then I implemented the data association module that matches measurements to tracks.

and finally I added the non-linear camera measurement model.

I achieved to track multiple objects over time, and I could visualize it in real time. I think that is amazing!

I think data association is the most difficult part, because you have to be sure which measurement goes to each track, and be sure that is the correct measurement for that track.


### 2. Do you see any benefits in camera-lidar fusion compared to lidar-only tracking (in theory and in your concrete results)? 

Some of the RMSE's were lower with camera-lidar fusion, so I think it is better to use camera-lidar fusion instead of lidar-only tracking.

### 3. Which challenges will a sensor fusion system face in real-life scenarios? Did you see any of these challenges in the project?

Track losses because of object occlussion, light shafts and other media that can block tracking. 

I think that the camera was detecting multiple false positive objects (without being confirmed). That cluttered the scene.


### 4. Can you think of ways to improve your tracking results in the future?

Probably adding radar!
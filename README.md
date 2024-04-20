# sigverse_hsrb_utils

## 追加予定モジュール

- [ ] bringup.launch
- [ ] hsrb_model.launch

## Sigverseから出力されているトピック一覧(defaults)

```bash
/client_count
/connected_clients
/hsrb/arm_trajectory_controller/command
/hsrb/base_scan
/hsrb/command_velocity
/hsrb/gripper_controller/command
/hsrb/hand_camera/camera_info
/hsrb/hand_camera/image_raw
/hsrb/head_center_camera/camera_info
/hsrb/head_center_camera/image_raw
/hsrb/head_l_stereo_camera/camera_info
/hsrb/head_l_stereo_camera/image_rect_color
/hsrb/head_r_stereo_camera/camera_info
/hsrb/head_r_stereo_camera/image_rect_color
/hsrb/head_rgbd_sensor/depth_registered/camera_info
/hsrb/head_rgbd_sensor/depth_registered/image_raw
/hsrb/head_rgbd_sensor/rgb/camera_info
/hsrb/head_rgbd_sensor/rgb/image_raw
/hsrb/head_trajectory_controller/command
/hsrb/joint_states
/hsrb/omni_base_controller/command
/interactive_cleanup/message/to_moderator
/interactive_cleanup/message/to_robot
/rosout
/rosout_agg
/tf
/tf_static
```

## TF tree

![tf tree](./assets/frames_sigverse.png)
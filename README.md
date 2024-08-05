# Robot Repository for group 7 sd12.
This is for practise, version control, and daily progress

CODE SO FAR...

def vision_recognized_marker_letter_F(msg):
    gimbal_ctrl.yaw_ctrl(-90)
    time.sleep(3)
    gun_ctrl.fire_once()
    time.sleep(3)
    gimbal_ctrl.recenter()
    vision_ctrl.disable_detection(rm_define.vision_detection_marker)

def vision_recognized_marker_number_one(msg):
    vision_ctrl.disable_detection(rm_define.vision_detection_marker)
    chassis_ctrl.rotate_with_degree(rm_define.clockwise,360)
    gimbal_ctrl.yaw_ctrl(90)
    gimbal_ctrl.yaw_ctrl(-90)
    gimbal_ctrl.recenter()
    gimbal_ctrl.pitch_ctrl(25)
    gimbal_ctrl.pitch_ctrl(-15)
    gimbal_ctrl.recenter()
    
def vision_recognized_marker_letter_D(msg):
    gimbal_ctrl.yaw_ctrl(-90)
    time.sleep(3)
    gimbal_ctrl.recenter()
    vision_ctrl.disable_detection(rm_define.vision_detection_marker)

def start():
    robot_ctrl.set_mode(rm_define.robot_mode_free)
    chassis_ctrl.set_rotate_speed(125)
    chassis_ctrl.set_trans_speed(1)
    gimbal_ctrl.set_rotate_speed(350)
    chassis_ctrl.move_with_distance(0,4.77) #good as is
    chassis_ctrl.move_with_distance(0,1.) #good as is
    chassis_ctrl.move_with_distance(-90,0.81)
    chassis_ctrl.move_with_distance(0,0.42)
    chassis_ctrl.move_with_distance(88,1.65)
    chassis_ctrl.move_with_distance(0,0.4)
    chassis_ctrl.move_with_distance(-90,0.6)
    chassis_ctrl.move_with_distance(-47,1.54)
    chassis_ctrl.move_with_distance(0,0.45)
    chassis_ctrl.move_with_distance(90,0.84)
    chassis_ctrl.move_with_distance(0,0.42)
    time.sleep(5)                              #First reset point
    chassis_ctrl.move_with_distance(0,3.7)
    chassis_ctrl.move_with_distance(0,3)
    gimbal_ctrl.yaw_ctrl(-90)
    vision_ctrl.enable_detection(rm_define.vision_detection_marker)                   #First scan
    time.sleep(2)
    gimbal_ctrl.recenter()                      #Reset Arm
    chassis_ctrl.move_with_distance(0,4.9)
    time.sleep(5)
    chassis_ctrl.move_with_distance(0,4.1)
    gimbal_ctrl.yaw_ctrl(-90)                   #Second scan
    time.sleep(2)
    gimbal_ctrl.recenter()
    chassis_ctrl.move_with_distance(0,4.6)
    time.sleep(5)                               #Second reset point
    chassis_ctrl.move_with_distance(0,4.11)
    gimbal_ctrl.yaw_ctrl(-90)                   #Third scan
    time.sleep(2)
    gimbal_ctrl.recenter()   
    time.sleep(2)
    gimbal_ctrl.recenter()
    chassis_ctrl.move_with_distance(0,3.6)
    chassis_ctrl.move_with_distance(0,2)
    chassis_ctrl.rotate_with_degree(rm_define.clockwise,180)
    gimbal_ctrl.recenter()
    time.sleep(5)
    chassis_ctrl.move_with_distance(0,5)
    chassis_ctrl.move_with_distance(0,5)
    chassis_ctrl.move_with_distance(0,5)
    chassis_ctrl.move_with_distance(0,3.77)
    gimbal_ctrl.yaw_ctrl(90)
    time.sleep(1)
    led_ctrl.set_bottom_led(rm_define.armor_bottom_all, 32, 242, 0, rm_define.effect_always_on)
    led_ctrl.set_top_led(rm_define.armor_top_all, 32, 242, 0, rm_define.effect_always_on)
    gimbal_ctrl.yaw_ctrl(0)
    time.sleep(5)
    chassis_ctrl.move_with_distance(1,5)
    chassis_ctrl.move_with_distance(0,5)
    chassis_ctrl.move_with_distance(1,5)
    chassis_ctrl.move_with_distance(0,5)

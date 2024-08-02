# Robot Repository for group 7 sd12.
This is for practise, version control, and daily progress

CODE SO FAR...
def start():
    robot_ctrl.set_mode(rm_define.robot_mode_free)
    chassis_ctrl.set_trans_speed(1.)
    chassis_ctrl.move_with_distance(0,3.63) #good as is
    chassis_ctrl.move_with_distance(0,2.14) #good as is
    chassis_ctrl.move_with_distance(-90,0.81)
    chassis_ctrl.move_with_distance(0,0.42)
    chassis_ctrl.move_with_distance(88,1.65)
    chassis_ctrl.move_with_distance(0,0.42)
    chassis_ctrl.move_with_distance(-90,0.6)
    chassis_ctrl.move_with_distance(-47,1.54)
    chassis_ctrl.move_with_distance(0,0.45)
    chassis_ctrl.move_with_distance(90,0.84)
    chassis_ctrl.move_with_distance(0,0.42)
    time.sleep(5)                              #First reset point
    chassis_ctrl.move_with_distance(0,3.7)
    chassis_ctrl.move_with_distance(0,3)
    gimbal_ctrl.yaw_ctrl(-90)                   #First scan
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

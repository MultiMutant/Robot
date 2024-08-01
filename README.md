# Robot Repository for group 7 sd12.
This is for practise, version control, and daily progress

CODE SO FAR...

def start():
    robot_ctrl.set_mode(rm_define.robot_mode_free)
    chassis_ctrl.set_trans_speed(0.5)
    chassis_ctrl.move_with_distance(0,3.63) #good as is
    chassis_ctrl.move_with_distance(0,2.1) #good as is
    chassis_ctrl.move_with_distance(-90,0.8)
    chassis_ctrl.move_with_distance(0,0.41)
    chassis_ctrl.move_with_distance(88,1.65)
    chassis_ctrl.move_with_distance(0,0.42)
    chassis_ctrl.move_with_distance(-90,0.54)
    chassis_ctrl.move_with_distance(-47,1.55) #THE FIRST BIG SLANTED LINE!!

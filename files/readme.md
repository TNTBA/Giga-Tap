Be sure to make the following changes in you klipper file:

## stepper_y
You will lose 15mm on the Y axis so you make sure you change your klipper file accordingly
```
[stepper_y]
step_pin:PE3
dir_pin:PE2
enable_pin:!PE4
microsteps:16
rotation_distance: 59.8519
full_steps_per_rotation:200  #set to 400 for 0.9 degree stepper
gear_ratio: 50:20
endstop_pin:PC12
position_min: -7.0
position_endstop:790.0 # <--- see this
position_max:790.5 # <---- see this 
homing_speed:80
homing_retract_dist:10
second_homing_speed:10
homing_positive_dir:true
step_pulse_duration:0.000002
```

## probe

```
[probe]
pin:^mcu1:gpio11
x_offset: 0
y_offset: 0
z_offset: -1.740 # Set this to your z_offset after your run bed leveling - you will never need to change it after setting this (until you change your nozzle). 
speed: 5.0
samples: 2
samples_result: median
sample_retract_dist: 3.0
samples_tolerance: 0.05
samples_tolerance_retries:4
```


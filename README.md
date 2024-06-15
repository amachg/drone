# drone
Οι ρυθμίσεις στο λογισμικό πτήσης


diff all

# version
# INAV/MATEKF405TE_SD 7.1.0 Mar 27 2024 / 13:54:51 (59a6ee61)
# GCC-10.3.1 20210824 (release)

# start the command batch
batch start

# reset configuration to default settings
defaults noreboot

# resources

# Timer overrides

# Outputs [servo]

# safehome

# Fixed Wing Approach

# features
feature -BLACKBOX
feature GPS
feature PWM_OUTPUT_ENABLE

# beeper

# blackbox
blackbox -NAV_ACC
blackbox NAV_POS
blackbox NAV_PID
blackbox MAG
blackbox ACC
blackbox ATTI
blackbox RC_DATA
blackbox RC_COMMAND
blackbox MOTORS
blackbox -GYRO_RAW
blackbox -PEAKS_R
blackbox -PEAKS_P
blackbox -PEAKS_Y

# Receiver: Channel map

# Ports
serial 4 2 115200 115200 0 115200
serial 5 262144 115200 115200 0 115200

# LEDs

# LED color

# LED mode_color

# Modes [aux]
aux 0 0 0 1300 2100
aux 1 1 0 900 2100
aux 2 11 1 1700 2100
aux 3 3 1 1300 2100

# Adjustments [adjrange]

# Receiver rxrange

# temp_sensor

# Mission Control Waypoints [wp]
#wp 0 invalid

# OSD [osd_layout]

# Programming: logic

# Programming: global variables

# Programming: PID controllers

# OSD: custom elements

# master
set looptime = 500
set gyro_main_lpf_hz = 90
set gyro_main_lpf_type = PT1
set dynamic_gyro_notch_q = 250
set dynamic_gyro_notch_min_hz = 60
set dynamic_gyro_notch_mode = 3D
set setpoint_kalman_q = 200
set gyro_zero_x = 14
set gyro_zero_y = -9
set gyro_zero_z = 2
set ins_gravity_cmss =  981.941
set acc_hardware = ICM42605
set acczero_x = -1
set acczero_y = -8
set acczero_z = 5
set accgain_x = 4102
set accgain_y = 4101
set accgain_z = 4104
set align_mag = CW270FLIP
set mag_hardware = QMC5883
set magzero_x = -280
set magzero_y = -266
set magzero_z = 251
set maggain_x = 1063
set maggain_y = 1045
set maggain_z = 1079
set baro_hardware = SPL06
set serialrx_provider = IBUS
set blackbox_rate_denom = 2
set motor_pwm_protocol = DSHOT300
set vbat_meter_type = ESC
set current_meter_type = ESC
set applied_defaults = 5
set gps_provider = UBLOX7
set gps_sbas_mode = EGNOS
set gps_ublox_use_galileo = ON
set gps_ublox_use_beidou = ON
set gps_ublox_use_glonass = ON
set airmode_type = THROTTLE_THRESHOLD
set i2c_speed = 800KHZ
set tz_offset = 120
set tz_automatic_dst = EU

# mixer_profile
mixer_profile 1

set model_preview_type = 3

# Mixer: motor mixer

mmix reset

mmix 0  1.000 -1.000  1.000 -1.000
mmix 1  1.000 -1.000 -1.000  1.000
mmix 2  1.000  1.000  1.000  1.000
mmix 3  1.000  1.000 -1.000 -1.000

# Mixer: servo mixer

# mixer_profile
mixer_profile 2


# Mixer: motor mixer

# Mixer: servo mixer

# profile
profile 1

set mc_p_pitch = 90
set mc_i_pitch = 34
set mc_d_pitch = 54
set mc_cd_pitch = 100
set mc_p_roll = 90
set mc_i_roll = 34
set mc_d_roll = 54
set mc_cd_roll = 100
set mc_p_yaw = 70
set mc_i_yaw = 20
set mc_cd_yaw = 100
set dterm_lpf_hz = 80
set dterm_lpf_type = PT3
set mc_iterm_relax = RPY
set d_boost_min =  0.800
set d_boost_max =  1.200
set antigravity_gain =  2.000
set antigravity_accelerator =  5.000
set smith_predictor_delay =  1.500
set tpa_rate = 20
set tpa_breakpoint = 1200
set rc_expo = 75
set rc_yaw_expo = 75
set roll_rate = 70
set pitch_rate = 70
set yaw_rate = 60
set ez_filter_hz = 90

# profile
profile 2


# profile
profile 3


# battery_profile
battery_profile 1

set bat_cells = 4
set vbat_min_cell_voltage = 290
set vbat_warning_cell_voltage = 310
set battery_capacity = 4500
set battery_capacity_warning = 450
set battery_capacity_critical = 225
set throttle_scale =  0.500
set throttle_idle =  5.500

# battery_profile
battery_profile 2


# battery_profile
battery_profile 3


# restore original profile selection
mixer_profile 1
profile 1
battery_profile 1

# save configuration
save

# 

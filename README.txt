This folder contians

1. The opi screens used for the exercises and demos 

2. The db files for the SoftIOC used for the tank demos
The fish tank demo is based on Kay's contorl and tank example

To start the IOC
softIoc -m Num=1,user=demo -s -d fishtankDemo.db


3. The IOC for the motor examples is avaiable on github at
   https://github.com/dchabot/motorsim
   https://github.com/dchabot/adsim


== softioc-motorsim pv list ==
epics>
epics> dbl
XF:31IDA-OP{Tbl-Ax:X1}Mtr_able
XF:31IDA-OP{Tbl-Ax:X2}Mtr_able
XF:31IDA-OP{Tbl-Ax:X3}Mtr_able
XF:31IDA-OP{Tbl-Ax:X4}Mtr_able
XF:31IDA-OP{Tbl-Ax:X5}Mtr_able
XF:31IDA-OP{Tbl-Ax:X6}Mtr_able
XF:31IDA-BI{Dev:1}E-I
XF:31IDA-BI{Dev:2}E-I
XF:31IDA-BI{Dev:3}E-I
XF:31IDA-BI{Dev:4}E-I
XF:31IDA-BI{Dev:5}E-I
XF:31IDA-BI{Dev:6}E-I
XF:31IDA-OP{Tbl-Ax:X1}Mtr
XF:31IDA-OP{Tbl-Ax:X2}Mtr
XF:31IDA-OP{Tbl-Ax:X3}Mtr
XF:31IDA-OP{Tbl-Ax:X4}Mtr
XF:31IDA-OP{Tbl-Ax:X5}Mtr
XF:31IDA-OP{Tbl-Ax:X6}Mtr
XF:31IDA-OP{Tbl-Ax:X1}Mtr_ableput
XF:31IDA-OP{Tbl-Ax:X2}Mtr_ableput
XF:31IDA-OP{Tbl-Ax:X3}Mtr_ableput
XF:31IDA-OP{Tbl-Ax:X4}Mtr_ableput
XF:31IDA-OP{Tbl-Ax:X5}Mtr_ableput
XF:31IDA-OP{Tbl-Ax:X6}Mtr_ableput
XF:31IDA-OP{Tbl-Ax:X1}Mtr_twCh
XF:31IDA-OP{Tbl-Ax:X1}Mtr_vCh
XF:31IDA-OP{Tbl-Ax:X2}Mtr_twCh
XF:31IDA-OP{Tbl-Ax:X2}Mtr_vCh
XF:31IDA-OP{Tbl-Ax:X3}Mtr_twCh
XF:31IDA-OP{Tbl-Ax:X3}Mtr_vCh
XF:31IDA-OP{Tbl-Ax:X4}Mtr_twCh
XF:31IDA-OP{Tbl-Ax:X4}Mtr_vCh
XF:31IDA-OP{Tbl-Ax:X5}Mtr_twCh
XF:31IDA-OP{Tbl-Ax:X5}Mtr_vCh
XF:31IDA-OP{Tbl-Ax:X6}Mtr_twCh
XF:31IDA-OP{Tbl-Ax:X6}Mtr_vCh

The motor records are the pvs ending in “Mtr”, above.
The Motor Record has over 100 fields in addition to the usual suspects (dbCommon). 
The interesting ones are .VAL, .RBV, .STOP (setpoint, read back, stop).
Further reading - http://www.aps.anl.gov/bcda/synApps/motor/R6-8/motorRecord.html

The “E-I” records, above, simulate a 1-D, scaler-valued sensor.
They are linked to the similarly numbered motor record, and produce a gaussian peak over certain motor ranges.

You can safely ignore the rest of the crud above.


== softioc-adsim pv list (truncated, obviously) ==
XF:31IDA-BI{Cam:Tbl}cam1:Acquire            # start/stop
XF:31IDA-BI{Cam:Tbl}image1:ArrayData     # the 1-D waveform (image)
XF:31IDA-BI{Cam:Tbl}image1:ArrayRate_RBV
XF:31IDA-BI{Cam:Tbl}image1:ArrayCounter_RBV
XF:31IDA-BI{Cam:Tbl}image1:ArraySize0_RBV
XF:31IDA-BI{Cam:Tbl}image1:ArraySize1_RBV

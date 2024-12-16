# iTCLab Jupyter Heat Monitoring and Controlling System
A jupyter based application to explore different control techniques of a simple temperature plant

### Overview
This code was written to showcase an Arduino based Temperature Control Lab (https://apmonitor.com/pdc/index.php/Main/ArduinoTemperatureControl) for a Lecture on Advanced Control Techniques.

The iTCLab system is built with two temperature sensors and two heaters. A Matlab or Python interface is provided to read the temperature data from the board and control the heaters power output. Two classes were created, one that aims to control the Arduino System (**control_arduino.py**) and another one replacing the Arduino interface with a simulator (**control_demo.py**), so the app can be used without the real hardware, as a demonstration.

This project implements four different control techniques (Manual, On-Off, PID and MPC) so the user can test and visualize the differences between them.

There is also a configurations window that presents some parameters that can be adjusted for the whole simulation or for each control technique.

The interface was build using ipywidgets and bqplot. The dynamic plant simulation is done using scipy `odeint` function, whilst the MPC is implemented using the gekko library. For more information regarding the MPC options refer to the gekko documentation (https://gekko.readthedocs.io/en/latest/).

### Dependencies
- numpy
- scipy
- ipywidgets (https://github.com/jupyter-widgets/ipywidgets)
- bqplot==0.11.9 (https://github.com/bloomberg/bqplot)
- gekko (https://github.com/BYU-PRISM/GEKKO)
- tclab (only for the control_arduino.py)

### Documentation
Soon

### Error Report
Monitoring system on Jupyter Notebook not working with error message.

<img src="https://github.com/gredychristian/Mikrokontroller-A081_22081010195_Gredy-Christian-Hendrawan-Putra/blob/main/06-itclab_jupyter/1%20Jupyter%20Testing.png" height="500">
<img src="https://github.com/gredychristian/Mikrokontroller-A081_22081010195_Gredy-Christian-Hendrawan-Putra/blob/main/06-itclab_jupyter/2%20Error%20Message.png" height="500">

```
Exception in thread Thread-3 (_work_pid):
Traceback (most recent call last):
  File "C:\Users\lenovo\AppData\Local\Programs\Python\Python313\Lib\threading.py", line 1041, in _bootstrap_inner
    self.run()
    ~~~~~~~~^^
  File "C:\Users\lenovo\AppData\Roaming\Python\Python313\site-packages\ipykernel\ipkernel.py", line 766, in run_closure
    _threading_Thread_run(self)
    ~~~~~~~~~~~~~~~~~~~~~^^^^^^
  File "C:\Users\lenovo\AppData\Local\Programs\Python\Python313\Lib\threading.py", line 992, in run
    self._target(*self._args, **self._kwargs)
    ~~~~~~~~~~~~^^^^^^^^^^^^^^^^^^^^^^^^^^^^^
  File "D:\Campus\Project\Arduino\iTCLab\Mikrokontroller-A081_22081010195_Gredy-Christian-Hendrawan-Putra\06-itclab_jupyter\control_arduino.py", line 1210, in _work_pid
    a.T1 + 273.15,
    ^^^^
  File "D:\Campus\Project\Arduino\iTCLab\Mikrokontroller-A081_22081010195_Gredy-Christian-Hendrawan-Putra\06-itclab_jupyter\itclab.py", line 76, in T1
    self._T1 = float(self.read('T1'))
               ~~~~~^^^^^^^^^^^^^^^^^
ValueError: could not convert string to float: 'ets Jun  8 2016 00:22:57'
```
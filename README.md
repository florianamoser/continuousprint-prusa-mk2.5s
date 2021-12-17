# continuousprint-prusa-mk2.5s
Config to continously print with a Prusa Mk 2.5s and the Continuous-Print-Plugin in Octoprint. Using brass nozzle cleaning brush to pruge nozzle between prints. 
Might not work for your use. Test and test before you use it without supervision. What works for me does not necessarily work for you.

**Get:**
- Octoprint on a RPI
- https://plugins.octoprint.org/plugins/continuousprint/
- Brass 3D printer nozzle cleaning brush
- a piece of heatresistant double sided tape

**Limitations:**
- do not place parts further back on the build plate than ~Y150
- only print parts that are > Z40mm 

**Setup:**
- install octoprint continous print plugin, restart octoprint
- cut brass brush from handle (with sidecutter) 
- stick brass brush to headbed. ~80mm from back, 5mm from right side.
![IMG_5715](https://user-images.githubusercontent.com/22799018/146578702-d89e8c8a-1591-4d88-aa19-a6dd3a89d3bb.JPG)
- check brush position by sending "G80" (Meshbedleveling) commmand in octoprint terminal. printhead should not touch brush and move around it when meshleveling.
- in octoprint settings > continuous print add code from bedclearing-nozzlepurge.gcode

<img width="1403" alt="Screenshot 2021-12-17 at 17 38 34" src="https://user-images.githubusercontent.com/22799018/146579305-d58054fc-7685-4ee5-996a-28d5608d2283.png">

- after slicing file in prusaslicer, remove the following lines (purge line front left)

![Screenshot 2021-12-17 at 17 46 24](https://user-images.githubusercontent.com/22799018/146580275-6e255ae9-5b21-4bcf-964d-88e7de47844c.png)

- add a piece of cartboard to the front side of the printbed. (Otherwise the finished print will drop between the screen and the bed and block the printer). 

![IMG_5719 copy](https://user-images.githubusercontent.com/22799018/146579981-c8cd66f9-323c-4250-8653-717356c3bc56.jpg)

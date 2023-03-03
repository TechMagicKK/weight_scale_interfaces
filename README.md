# weight_scale_interfaces

## install
```.sh
cd ~/dev_ws
colcon build --cmake-clean-first --symlink-install --packages-select weight_scale_interfaces
. install/local_setup.zsh
```
## msg.Weight
| type | name | explanation |
|:---|:---|:---|
| builtin_interfaces/Time | stamp | Measurement time |
| bool | stable | State of the scale (for example measurement is stable or fluctuating) |
| float64 | weight | weight |
| string | unit | kg, g, oz, ... |

## action.SetZero
| type | name | explanation |
|:---|:---|:---|
|\2> Goal |
| float64 | timeout | timeout(sec) |
|\2> Result |
| bool | success | True/False |
| string | message | |
|\2> Feedback |
| weight_scale_interfaces/Weight | weight | |

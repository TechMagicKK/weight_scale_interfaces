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
| Goal ||
| float64 | timeout | timeout(sec) |
| Result ||
| bool | success | True/False |
| string | message | |
| Feedback ||
| weight_scale_interfaces/Weight | weight | |

## action.GetWeight
| type | name | explanation |
|:---|:---|:---|
| Goal ||
| float64 | timeout | timeout(sec) |
| Result ||
| weight_scale_interfaces/Weight | weight |
| bool | success | succeeded in obtaining a stable weight |
| string | message ||
| Feedback ||
| weight_scale_interfaces/Weight | weight ||

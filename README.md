Completely based on DominiLux amdgpu-pro-fans.sh https://github.com/DominiLux/amdgpu-pro-fans .

This script adjust the fan speed for all amdgpu-pro GPU's on the system, the script will increase or decrease the fan speed for each GPU until that GPU hits the target temperature (-T).

A low update time (under 3) will cause spikes and drops in fan speed during start/stop of jobs, but will adjust speeds smoothly during normal load.

## Requires: python2.7, python-numpy, python-future

See head of amdgpu-pro-fans-target.py file if any python module errors to verify you have the necessary modules installed.

## Install:
git clone https://github.com/kovaxalive/amdgpu-pro-fans-target

cd amdgpu-pro-fans-target/

sudo chmod +x amdgpu-pro-fans-target.py

## Execute
`sudo ./amdgpu-pro-fans-target.py`


See optional arguments with -h flag:
```
./amdgpu-pro-fans-target.py -h

```

### Notes
If using the curses display, exit pressing 'Q', dont Ctrl+C if you dont want to fuck up your terminal.

This script has been based on amdgpu-pro 17.10, the file possible_fan_speeds.txt has been created to see what the actual speed becomes when a specific speed is set in the driver file.
It is very likely that if you have a different driver version this script will not work as it is supposed to.



Completely based on DominiLux amdgpu-pro-fans.sh https://github.com/DominiLux/amdgpu-pro-fans .

This script adjust the fan speed for all amdgpu-pro GPU's on the system, the script will increase or decrease the fan speed for each GPU until that GPU hits the target temperature (-T).

A low update time (under 3) will cause spikes and drops in fan speed during start/stop of jobs.

# Requires: python2.7, python-numpy, python-future

See head of amdgpu-pro-fans-target.py file if any python module errors to verify you have the necessary modules installed.

# Install:
git clone https://github.com/kovaxalive/amdgpu-pro-fans-target

cd amdgpu-pro-fans-target/

sudo chmod +x amdgpu-pro-fans-target.py

# Execute
`sudo ./amdgpu-pro-fans-target.py`


See optional arguments with -h flag:
```sh
$ sudo ./amdgpu-pro-fans-target.py -h
[sudo] password for r: 
usage: amdgpu-pro-fans-target.py [-h] [-u UPDATE_TIME] [-T TARGET_TEMP]
                                 [-m MIN_SPEED]

optional arguments:
  -h, --help            show this help message and exit
  -u UPDATE_TIME, --update-time UPDATE_TIME
                        Time between fan adjustments/checks in seconds
                        (default: 1)
  -T TARGET_TEMP, --target-temp TARGET_TEMP
                        Target temperature in degrees Celsius (default: 60)
  -m MIN_SPEED, --min-speed MIN_SPEED
                        Minimum fan speed of GPU in %. Warning: imprecise
                        (default: 40)
```

# Exit: Hit 'Q'. 
Dont Ctrl+C if you dont want to fuck up your terminal.

### Note
This script has been based on amdgpu-pro 17.10, the file possible_fan_speeds.txt has been created to see what the actual speed becomes when a specific speed is set in the driver file.
It is very likely that if you have a different driver version this script will not work as it is supposed to.



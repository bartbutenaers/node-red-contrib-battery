# node-red-contrib-battery
A Node Red node to get information about the battery

## Install
Run the following npm command in your Node-RED user directory (typically ~/.node-red):
```
npm install node-red-contrib-battery
```

## Node Usage
Get information about the battery by injecting a random message into this node:

![Flow](https://raw.githubusercontent.com/bartbutenaers/node-red-contrib-battery/master/images/battery_flow.png)

The `msg.payload` of the output message contains a lot of data about the battery:
+ **hasbattery**: indicates presence of battery.
+ **cyclecount**: numbers of recharges.
+ **ischarging**: indicates if battery is charging.
+ **maxcapacity**: max capacity of battery.
+ **currentcapacity**: current capacity of battery.
+ **percent**: charging level in percent.
+ **timeremaining**: minutes left (if discharging).
+ **acconnected**: AC connected.
+ **type**: battery type.
+ **model**: model.
+ **manufacturer**: manufacturer.
+ **serial**: battery serial.

## Limitation

This node can be run on a number of operating systems, but check this [table](https://github.com/sebhildebrandt/systeminformation#3-cpu-memory-disks-battery-graphics) to make sure the required information is accessible on your platform!  

Most systems running Node-RED wil not contain a battery.  For example on Raspberry Pi, the `msg.payload.hasbattery` field will contain `false` and all other fields will contain no data ...

# 2021_usu_rover
> Short blurb about what your product does.

<!-- [![NPM Version][npm-image]][npm-url] -->
<!-- [![Build Status][travis-image]][travis-url] -->
<!-- [![Downloads Stats][npm-downloads]][npm-url] -->

One to two paragraph statement about your product and what it does.

![](header.png)

## Installation

>Prerequisites:  
* OS X & Linux: Ubuntu 18.04
* ROS Melodic
* //TODO CUDA enabled  
* //TODO Opencv maybe



Clone the repo from GitHub

HTTPS
```sh
git clone https://github.com/Zenif-NIght/2021_usu_rover.git
```

SSH
```sh
git clone git@github.com:Zenif-NIght/2021_usu_rover.git
```

## Running The Robot

@Chrisotpher Add more docs( A few motivating and useful examples of how your product can be used. Spice this up with code blocks and potentially more screenshots.)

cd to the catkin workspace
```
cd catkin_ws/
catkin_make
```

_For more examples and usage, please refer to the [Wiki][wiki]._
## Running Sub-Modules 
### GPS set up 
>@ David Allen -> could you add your pictures of the GPS setup

CLick [HERE](https://github.com/Combinacijus/Samana-Autonomous-Robot/tree/d902287d01b96e2dc39b350da39b125db051c57d/Arduino) to see a good example Repo

This [LINK](https://github.com/Combinacijus/Samana-Autonomous-Robot/blob/d902287d01b96e2dc39b350da39b125db051c57d/Arduino/gps_odom_node/gps_odom_node.ino) was the most helpful 

The port could change from "/dev/ttyACM0" or "/dev/ttyACM1"
```
rosrun rosserial_python serial_node.py /dev/ttyACM0
```
Output:
```
[INFO] [1611433791.190899]: ROS Serial Python Node
[INFO] [1611433791.209801]: Connecting to /dev/ttyACM0 at 57600 baud
[INFO] [1611433793.324585]: Requesting topics...
[INFO] [1611433793.603750]: Note: publish buffer size is 150 bytes
[INFO] [1611433793.613011]: Setup publisher on fix [sensor_msgs/NavSatFix]

```

TO check if the output is working open  new terminal tab, and check the topic "fix" as it was the one we published on the arduino node
```
rostopic echo fix
```
Output:
```
---
header: 
  seq: 3
  stamp: 
    secs: 1611434083
    nsecs:  88293024
  frame_id: "gps"
status: 
  status: -1
  service: 1
latitude: 1000.0
longitude: 1000.0
altitude: 1000000.0
position_covariance: [4.150517416584649e+19, 0.0, 0.0, 0.0, 4.150517416584649e+19, 0.0, 0.0, 0.0, 4.150517416584649e+19]
position_covariance_type: 1
---

https://lastminuteengineers.com/neo6m-gps-arduino-tutorial/

```


## Development setup

Describe how to install all development dependencies and how to run an automated test-suite of some kind. Potentially do this for multiple platforms.

<!-- ```sh
make install
npm test
``` -->

## Release History

<!-- * 0.2.1
    * CHANGE: Update docs (module code remains unchanged)
* 0.2.0
    * CHANGE: Remove `setDefaultXYZ()`
    * ADD: Add `init()`
* 0.1.1
    * FIX: Crash when calling `baz()` (Thanks @GenerousContributorName!)
* 0.1.0
    * The first proper release
    * CHANGE: Rename `foo()` to `bar()` -->
* 0.0.1
    * Work in progress

## Meta

Your Name – [@YourTwitter](https://twitter.com/dbader_org) – YourEmail@example.com

Distributed under the XYZ license. See ``LICENSE`` for more information.

[https://github.com/yourname/github-link](https://github.com/dbader/)

## Contributing

1. Fork it (<https://github.com/yourname/yourproject/fork>)
2. Create your feature branch (`git checkout -b feature/fooBar`)
3. Commit your changes (`git commit -am 'Add some fooBar'`)
4. Push to the branch (`git push origin feature/fooBar`)
5. Create a new Pull Request

<!-- Markdown link & img dfn's -->
[npm-image]: https://img.shields.io/npm/v/datadog-metrics.svg?style=flat-square
[npm-url]: https://npmjs.org/package/datadog-metrics
[npm-downloads]: https://img.shields.io/npm/dm/datadog-metrics.svg?style=flat-square
[travis-image]: https://img.shields.io/travis/dbader/node-datadog-metrics/master.svg?style=flat-square
[travis-url]: https://travis-ci.org/dbader/node-datadog-metrics
[wiki]: https://github.com/yourname/yourproject/wiki

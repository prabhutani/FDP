# Flightplan Demo Platform (FDP)
## Introduction
A portable platform that builds on existing tooling to enable end-to-end experimentation and zero-effort in-browser interactive visualization, to benefit the teaching of P4-based SDN and research demonstration.
For More Information please visit our website: [FDP](https://flightplan.cis.upenn.edu/)


Dillinger is a cloud-enabled, mobile-ready, offline-storage compatible,
AngularJS-powered HTML5 Markdown editor.

## Backend System
1. Download the `FDP` and `traffic.sh` from github and place them on the web server on which you are are going to host the FDP.
2. Download the `Topology.yml` and `Config.yml` from github containing template for the topology and configuration files respectively.
3. Create the experiment and generate the `pcap` files for the each node along the path of a packet from source host node to destination host node.
4. Create graph log files and place them in a directory, if required to show run time graph in the animation.
5. Place the images in a directory, if required to show them in the animation.
6. Update the `Topology.yml` file based upon the experiment.
7. Update the `Config.yml` file to customize the animation. If you are using graphs or images for the animation please provide this information too in the `Config.yml` file.

##### _Creating The Experiment_
Execute the following command to generate the data readable to FDP:
```sh
./traffic -create <Streaming Asset Directory> <Name of Experiment> <Topology File> <pcap directory> <Configuration File> <Graph Directory> <Image Directory>
```
Where,
| Parameter | Description | Value Type |
| ------ | ------ | ------ |
| <Streaming Asset Directory> | Path of the directory `FDP/StreamingAssets` | String |
| <Name of Experiment> | Name of Experiment | `_` Saparated string  |
| <Topology File> | Path of `Topology.yml` file | String |
| <pcap directory> | Path of the directory where `pcap` files are | String |
| <Configuration File> | Path of the `Config.yml` file | String |
| <Graph Directory> | `Graph` directory path  | String/None |
| <Image Directory> | Path of the directory | String/None |

##### _Removing The Experiment_
Execute the following command to remove the existing experiment from the FDP experiment list:
```sh
./traffic -remove <Streaming Asset Directory> <Name of Experiment>
```
Where,
| Parameter | Description | Value Type |
| ------ | ------ | ------ |
| <Streaming Asset Directory> | Path of the directory `FDP/StreamingAssets` | String |
| <Name of Experiment> | Name of Experiment | `_` Saparated string  |

## Frontend System
1. Open the web browser (`Chrome` / `Firefox` / `Safari` / `MS Edge`).
2. Go to the FDP hosted website.
3. Choose the experiment from the drop down menu.
4. _There you have a rich interactive 3D network._

## TODO
1. Animation time calculation
2. Place all the parameters as options in traffic.sh.

## License

TODO

**Free Software, Hell Yeah!**
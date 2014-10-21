PingHost
========

An object with advanced capabilities for pinging hosts. 

## Features

- [x] Can configure up to 10 hosts to monitor
- [x] Alarms for each individual host
- [x] Configurable ping frequency
- [ ] Statistics
- [ ] Better graphics
- [ ] Auto detect all platforms as part of Galaxy
- [ ] Auto detect all DI nodes (PLCs)
 
## Setup Instructions

1. Set some good defaults in the Cfg UDAs
	- *AlarmMessage*: as you can see in INIT, this UDA can include two variables &lt;HOST&gt; and &lt;PINGS&gt;
	- *MaxFailedPings*: number of pings to miss before setting the alarms
	- *Hosts*: set the hosts (either using IP or host name) that you'd like to monitor
	- *HostsEnabled*: turn ON for each host that coorresponds to the Hosts array that you'd like to ping
	- *PingFrequency*: set to any value higher than 00:00:01.0000000 for the frequency at which you'd like to initiate pings
	- *Timeout*: the timeout in milliseconds that the system ping will use for trying to reach the node. Default set to 10 seconds (10000 ms).

2. Deploy to engine

3. If you'd liked to use the included graphic, pop it into InTouch. Hopefully will have some improvements to this in the future.

## Author

Complaints, compliments, questions: [Eliot Landrum](elandrum@stonetek.com)

## License

MIT License

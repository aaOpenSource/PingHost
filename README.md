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
 
## Platform Compatibility

Object built in System Platform 2014. Can back-port manually if you take out the [Try/Catch block](https://github.com/aaOpenSource/PingHost/blob/master/export/Scripts/PingHosts.xml#L49). 
However, will need to capture exception when a hostname can't be resolved. I noticed that Ping.Send(host, timeout)
just throws an exception when it can't resolve host.
 
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

## Contributors

* [Eliot Landrum](mailto:elandrum@stonetek.com), MES Analyst with [Stone Technologies](http://stonetek.com).

## License

MIT License. See the [LICENSE file](/LICENSE) for details.

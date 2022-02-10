\#arduino #iot 
[ESP Commands](http://fab.cba.mit.edu/classes/865.15/people/dan.chen/esp8266/)

[Working Source Code from contractwolf](https://github.com/contractorwolf/ESP8266/blob/master/ESP8266.ino)

[Basic Tutorial](https://contractorwolf.com/esp8266-wifi-arduino-micro/)

![](esp8266%20wiring.jpg)

![](esp8266%20pins.jpg)

|Commands|Description|Set/Execute|Parameters|
|:-------|:----------|:----------|----------|
|AT+RST|restart the module|–|–|
|AT+CWMODE|wifi mode|AT+CWMODE=<mode>|1= Sta, 2= AP, 3=both|
|AT+CWJAP|join the AP|AT+ CWJAP =<ssid>,\< pwd >|ssid = ssid, pwd = wifi password|
|AT+CWLAP|list the AP|AT+CWLAP||
|AT+CWQAP|quit the AP|AT+CWQAP||
|AT+ CWSAP|set the parameters of AP|AT+ CWSAP= <ssid>,<pwd>,<chl>, <ecn>|ssid, pwd, chl = channel, ecn = encryption|
|AT+ CIPSTATUS|get the connection status|AT+ CIPSTATUS||
|AT+CIPSTART|set up TCP or UDP connection|1)single connection (+CIPMUX=0) AT+CIPSTART= <type>,<addr>,<port>; 2) multiple connection (+CIPMUX=1) AT+CIPSTART= <id><type>,<addr>, <port>|id = 0-4, type = TCP/UDP, addr = IP address, port= port|
|AT+CIPSEND|send data|1)single connection(+CIPMUX=0) AT+CIPSEND=<length>; 2) multiple connection (+CIPMUX=1) AT+CIPSEND= <id>,<length>||
|AT+CIPCLOSE|close TCP or UDP connection|AT+CIPCLOSE=<id> or AT+CIPCLOSE||
|AT+CIFSR|Get IP address|AT+CIFSR||
|AT+ CIPMUX|set mutiple connection|AT+ CIPMUX=<mode>|0 for single connection 1 for mutiple connection|
|AT+ CIPSERVER|set as server|AT+ CIPSERVER= <mode>\[,<port> \]|mode 0 to close server mode, mode 1 to open; port = port|
|+IPD|received data|||
|||||

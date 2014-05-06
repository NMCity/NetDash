NetDash v1.4.4
=======

Small web-based monitoring dashboard for windows in C# and MVC

A small web-based monitoring dashboard for your Windows pc/server writen in C# and MVC + Chart.js.
	The dashboard is built using only C# libraries available in the main C# distribution, trying to create a small list of dependencies without the need of installing many packages or libraries.

Current dependencies:
	== Net Framework 4
	== C# MVC 4
	== AttributeRouting

View Demo

user: admin
pass: admin123

Installation
	Installing NetDash

Settings
	NetDash settings
	The only settings currently available which you can modify are the refresh rates for the different data tables. There are 3 different refresh settings under netdash/App_data/Setting.ini and values are in miliseconds:

	TIME_JS_REFRESH = 30000			#30 seconds
	TIME_JS_REFRESH_LONG = 120000	#120 seconds
	TIME_JS_REFRESH_NET = 2000		#2 seconds
	You can modify any of the values to whatever you would like the new refresh rate to be. Restart the webserver after each update to the Setting.ini file.

	The tables and the refresh settings are as follows:

	Memory Usage - TIME_JS_REFRESH
	Load Average - TIME_JS_REFRESH
	CPU Usage - TIME_JS_REFRESH
	Traffic Usage - TIME_JS_REFRESH_NET
	Disk Reads/Writes - TIME_JS_REFRESH_NET
	Uptime - TIME_JS_REFRESH_LONG
	Disk Usage - TIME_JS_REFRESH_LONG
	Online Users - TIME_JS_REFRESH_LONG
	Processes - TIME_JS_REFRESH_LONG
	Netstat - TIME_JS_REFRESH_LONG


Remote data retrieval
	NetDash remote data retrieval

	NetDash will allow you to retrieve data remotely if needed. This can be useful if you want to store any of the data in a database or another application.

	/info/uptime/				- Uptime
	/info/platform/hostname/	- Hostname
	/info/platform/osname/		- OS Name
	/info/platform/kernel/		- Kernel
	/info/getcpus/cpucount/		- Number of CPU cores
	/info/getcpus/cputype/		- Type/Name of CPU
	/info/memory/				- Memory Usage
	/info/cpuusage/				- CPU Usage in percentage(%), free and used
	/info/getdisk/				- Disk Usage
	/info/getusers/				- Online Users
	/info/getips/				- IP Addresses
	/info/gettraffic/			- Internet Traffic
	/info/getdiskio/			- Disk Reads/Writes
	/info/proc/					- Running Processes
	/info/loadaverage/			- Load Average
	/info/getnetstat/			- Netstat

	To see the format of the JSON returned datasets or data you can access any of the URLs from your browser ex. http://domain.com/info/uptime/ 

OS Support
	NetDash was tested and runs under the following OSs:

Windows Server
	Might work under others, but didn't get to test any other OSs just yet.

License
	MIT

Credits
	Dashboard Template, Bootstrap, Font Awesome

Changelog




LICENSE

	The MIT License (MIT)

	Copyright (c) 2014 Yasin Kuyu - https://twitter.com/yasinkuyu - https://github.com/yasinkuyu/

	Permission is hereby granted, free of charge, to any person obtaining a copy
	of this software and associated documentation files (the "Software"), to deal
	in the Software without restriction, including without limitation the rights
	to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
	copies of the Software, and to permit persons to whom the Software is
	furnished to do so, subject to the following conditions:

	The above copyright notice and this permission notice shall be included in all
	copies or substantial portions of the Software.

	THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
	IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
	FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
	AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
	LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
	OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
	SOFTWARE.
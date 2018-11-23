# node-red-keenetic

Simple flow to show how to use Keenetic API from Node-RED. http://forum.keenetic.com for API questions.
See flow.jpg for visual representation.

In this flow modern (2.13+ firmware) supported and secured method for authentification is used to minimize router overhead. Every 5-sec request polling usually have low effect on router cpu load by my experience. 

APIs demoed:
1) WIFI devices connected
2) Traffic on selected interface

Remark: See Keenetic documentation for more commands or just look at developer console in Crome during navigation thought Keenetic Dashboard interface. Almost everything is available. Actional commands will need POST http request, not covered here yet. 

Before importing flow please add folowing code to 
functionGlobalContext: {} of settings.js file of NODE-RED to enable required functions for hash calculation:

md5:require('md5'),

sha256:require('sha256')

and install them using npm install:

npm install md5

npm install sha256

In some cases it may be required to instal them globally:

npm install -g md5

npm install -g sha256

Reboot Node-Red before continue.

After that you can import the flow from flow.txt. Then change username and password to your router in "Put your router login/pass here".
Please take into acccount tha this is sample flow, you need to tune it up according to your smarthome solution.

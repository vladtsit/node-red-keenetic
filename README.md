# node-red-keenetic
Simple flow to show how to use Keenetic API from Node-RED

APIs demoed:
1) WIFI devices connected
2) Traffic on selected interface

Remark: See Keenetic documementation for more commands or just look at developer console in Crome during navigation thought Keenetic Dashboard interface. Almost everything is available. Actional commands will need POST http request, not covered here yet. 


Then you can pass data to Smart Home system of your choice - Domoticz, Majordomo, etc.

Before importing flow please add folowing code to 
functionGlobalContext: {} of settings.js file of NODE-RED to enable required functions fo hash calculation:

md5:require('md5'),
sha256:require('sha256')

and install them using npm install:

npm install md5
npm install sha256

in some cases it may be required to instal them globally
npm install -g md5
npm install -g sha256

Reboot Node-Red before continue.

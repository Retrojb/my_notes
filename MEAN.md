# Loopback Notes:
	Install: 
		use `npm`
	Build: 
		`lb` builds a base project
			* Set the datasource `lb datasource`
				* set host and port to local host for dev
				@TODO create an enum for environments
	Model:
		`lb model <MODEL_NAME>` **CAPITALIZE[0]**
		Add Properties, make sure to not add arrays of relationships add those in 		the json file. 
	Run Server: 
		`node .`
		**RESTART SERVER UPON UPDATES** 😧
# Angular Notes:
	Implementing Loopback:
		Install `npm install --save @mean-expert/loopback-sdk-builder`
	Service Generation:
		from the root of the client application run:
		`./node_modules/.bin/lb-sdk ../roommate-server/server/server.js src/sdk`
			1.  check that the .exec is in the node_mod bin folder
			1. the directory to the node server
			1. Where the SDK (created services are stored)

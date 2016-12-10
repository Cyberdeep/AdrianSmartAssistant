
# AdrianSmartAssistant

/************************************************************************
Copyright [2016] [Gergely Hajcsak & Jamie Deakin - The Adrian Team]
Webiste : www.theadrianproject.com
Email : team@theadrianproject.com
Licence : Licensed under the Apache License, Version 2.0
************************************************************************/


Introducing Adrian, your advanced open source Home Smart Assistant. Bringing simplicity to your home through voice automation. 
Get a morning news update, stream music, control your smart devices & ask just about anything. 


Hot to configire 
--------------------------------------------------------------------------

to start Planign with adrian the core modules need to be configured
it has 2 core modules 

	1.	Google Speech to Text Service Module
	2.	Ivona Text to Speech Module

	3.  Start Application
	4.  Stop Appilication

	5. 	Online Update Adrian

--------------------------------------------------------------------------
All module configuration chnage can be done in the constants.js file
--------------------------------------------------------------------------

1. Configuring Google Speech to Text Service Module
--------------------------------------------------------------------------

All users need a Google Speech Service Account which can be obtained
online. If you don't have one yet get it from https://cloud.google.com/speech
Google Speech Service is free up to a certain montly limit. 

Once you registered you will have a 
	project_id 
	google application credential file

This file can be downloaded at https://console.developers.google.com/project/_/apis/credentials
Once you have google application credential file copy it to /Library/googleSpeech/Account/ folder
And set it up int the constants.js file 

Change the constants.js repacling the values

	define("GOOGLE_APPLICATION_CREDENTIALS", __dirname  + "/Library/googleSpeech/Account/YOUR_PROJECT_FILE_NAME_COMES_HERE")
	define("GCLOUD_PROJECT", "YOUR_PROJECTN_NAME_COMES_HERE")


2. Configuring Ivona Text to Speech Module
--------------------------------------------------------------------------

All users also need a Ivona account.  If you dont have one get it at  https://www.ivona.com 
Its is a very easy process pick the free plan option and register.
Once you have your Ivona credentials 

Change the constants.js repacling the values

	define("IVONA_ACCESSKEY", "YOUR_IVONA_ACCESSKEY_COMES_HERE");
	define("IVONA_SECRETKEY", "YOUR_IVONA_SECRETKEY_COMES_HERE");


3.  Start Application
--------------------------------------------------------------------------

	./adrian.sh

4.  Stop Appilication
--------------------------------------------------------------------------

The application can be stopped any time pressing CTRL+C
Clearing memory/killing all depedencies after Adrian can be done

	./stop


5. 	Online Update Adrian
--------------------------------------------------------------------------

in the AdrianSmartAssistant folder (it doesnt delete any local config changes)

	git reset --hard origin/master


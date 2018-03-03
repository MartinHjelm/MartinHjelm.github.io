---
layout: post
title: Useful Matlab Commands
---

There are number of useful commands that will help you keep sanity in Matlab.

If you want to run Matlab in terminal mode to avoid the very resource and memory taxing Java interface. 

		matlab -nodesktop

Then if you want add all paths in the current and subfolders 

    addpath(genpath(pwd))

    
And maybe displays all available variables
    
		who
		
Sometimes the printing of information will not happen because resources are going somewhere else you can force the printing just like the `flush` command in C++. To flush the output you can do this, however, the command probably only is relevant for the Java interface.

    drawnow(update);
		
Sometimes or most of the time you need to debug the code. You can then give Matlab the command to stop where the error occurred with all the variables in the scope available for inspection. It will make your life 100% easier if not 200%. 

    dbstop on error
		
To turn of this functionality you can use this command,

    dbclear all
		


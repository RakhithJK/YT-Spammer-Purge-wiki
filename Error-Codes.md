#### About The Error Codes
- The error codes should be mostly self-documenting in the program, so this page is just for the sake of full documentation. 
- They are mostly just an easy way for users to point the the exact place they encounter an issue when submitting an problem, in case they forget to include the full traceback.


***

	U = Update
	C = Config
	X = Critical / Urgent
	F = File
	R = Recovery
	G = GUI
	A = Authentication / API
	Z = Unknown Error / Exception
	
	
	• U-1 : Manually Checking for updates
	• U-2 : Python version not high enough
	• U-3 : Auto Checking Updates -- L = List Update
	• U-4 : Rate Limit reached while checking for update  -- L = List Update
	• U-5 : Checking for list updates
	
	• X-1 : Comments chosen to be excluded were not actually removed from dictionary
	• X-2 : Variable referenced before assignment, requires patching
	• X-3 : Crash caused by KeyError referencing config
	• X-4 : Unknown KeyError (missing reference in dictionary probably)
	
	• Z-1 : Unknown HttpError caught
	• Z-2 : Unknown UnboundLocalError caught
	• Z-3 : Unknown exception
	• Z-4 : 
	
	• F-1 : Problem deleting existing config file
	• F-2 : Problem reading default config file
	• F-3 : Problem creating config file
	• F-4 : Config file found but problem loading it
	• F-5 : Recovering, found log file but problem reading it
	• F-6 : Problem deleting existing exe file
	
	• R-1 : In recovery mode, no comment IDs detected when loading file or after taking input
	
	
	• G-1 : While trying to run or during running of GUI input component, user closed window or problem with input
	
	
	• A-1 : Exception when running authentication first time
	• A-2 : General error catch for HttpError exceptions
	
	• C-1 : Invalid use_this_config setting
	• C-2 : Invalid value for 'enable_logging'
	• C-3 : Invalid value skip_deletion
	• C-4 : Invalid value for 'removal_type'
	• C-5 : 'delete_without_reviewing' is set to 'True', but using non-allowed filter mode
	• C-6 : 'delete_without_reviewing' is set to 'True', but removal_type not set to allowed value
	• C-7 : Invalid value for delete_without_reviewing
	• C-8 : 'enable_ban' is set to 'True' in config file (not allowed)
	• C-9 : Invalid value for 'enable_ban'
	• C-10: Not user's channel, and delete_without_renewing = True, but removal_type is not 'ReportSpam'
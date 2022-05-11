# Backup-Utility
I created this tool to help our field service techs get proper backups.
Everything has been developed by myself aside from the JetControl.cs class(this is just a class that easily allows me to use the library provided by our PLC manufacturer)
The backup utility has error handling at all aspects as i know the people using the software are not tech-savy people. 
I coded quite a bit of auto-fill for the PLC settings as our techs do not know what PLC type nor do they know the IP address off hand. 
The program uses robocopy to create zip files of important backup files to restore the machine if a critical failure were to happen.
additionally, I am able to reach back into the PLC and pull a register backup all at the click of a button. 

I used asynchronous threading as I ran into the problem that the program was trying to zip-up the folder as I was pulling the register backup. The delay during the backup is a workaround I had to use as the backup finished event gets fired off early from the PLC(something I cannot control). So a small delay solved my problem.

thanks for reviewing and I am open to any suggestions

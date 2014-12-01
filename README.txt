
HOWTO Set this thing up with a streaming media server....
============================================================
In your buildout, add a flash entry in your parts section like so,
>>> parts =
>>>    plone
>>> #    zope2
>>>    productdistros
>>>     instance
>>>     zopepy
>>>     zopeskel
>>>     precompile
>>>     chown
>>>     unifiedinstaller
>>> 		roadrunner
>>> 		flash

Next add a flash section with something like the following...
>>> [flash]
>>> recipe = uwosh.recipe.flash
>>> server_address = rtmp://myflashserver/vod
>>> ftp_address = myftptomyflashserver
>>> ftp_user = ftpuser
>>> ftp_password = ftppassword
>>> ftp_media_directory = /path/to/where/flash/files/are/stored
		
Can also set passive mode by doing this,
>>> ftp_use_passive_mode = False
It defaults to True
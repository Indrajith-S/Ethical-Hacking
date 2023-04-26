- Upon trying to run msfconsole on the remote host using auxiliary/scanner/smb/smb_version module we fail but get very valuable information about its version

- Moving on, trying to connect to the smb share brought us to a dead end:
	`smbclient -L \\\\<ip>\\ (-L to list all the files and \\\\ for character escaping)``
	- This ended in us being denied.


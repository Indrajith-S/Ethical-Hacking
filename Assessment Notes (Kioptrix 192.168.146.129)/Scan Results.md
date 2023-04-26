- Documentation of scanning and enumeration performed on kioptrix - This scan result is in order of attack basis.

- NMAP - 
	80/443 - 192.168.146.129 -- 6.40pm
	Default webpage  - Apache running PHP

- Information Disclosure - Server header disclosed version infromation
- Information Disclosure - 404 page upon clicking on "Documentroot"

+ Server: Apache/1.3.20 (Unix)  (Red-Hat/Linux) mod_ssl/2.8.4 OpenSSL/0.9.6b

- NIKTO - 
	+ mod_ssl/2.8.4 appears to be outdated (current is at least 2.8.31) (may depend on server version)
	+ OSVDB-27487: Apache is vulnerable to XSS via the Expect header
	+ OSVDB-838: Apache/1.3.20 - Apache 1.x up 1.2.34 are vulnerable to a remote DoS and possible code execution. CAN-2002-0392.
	+ OSVDB-4552: Apache/1.3.20 - Apache 1.3 below 1.3.27 are vulnerable to a local buffer overflow which allows attackers to kill any process on the system. CAN-2002-0839.
	+ OSVDB-2733: Apache/1.3.20 - Apache 1.3 below 1.3.29 are vulnerable to overflows in mod_rewrite and mod_cgi. CAN-2003-0542.
	
	+ mod_ssl/2.8.4 - mod_ssl 2.8.7 and lower are vulnerable to a remote buffer overflow which may allow a remote shell. http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2002-0082, OSVDB-756.
	
	+ Allowed HTTP Methods: GET, HEAD, OPTIONS, TRACE 
	+ OSVDB-877: HTTP TRACE method is active, suggesting the host is vulnerable to XST
	+ ///etc/hosts: The server install allows reading of any system file by adding an extra '/' to the URL.
	+ OSVDB-682: /usage/: Webalizer may be installed. Versions lower than 2.01-09 vulnerable to Cross Site Scripting (XSS).
	+ OSVDB-3268: /manual/: Directory indexing found.
	+ OSVDB-3092: /manual/: Web server manual found.
	+ OSVDB-3268: /icons/: Directory indexing found.
	+ OSVDB-3233: /icons/README: Apache default file found.
	+ OSVDB-3092: /test.php: This might be interesting...
	+ /wp-content/themes/twentyeleven/images/headers/server.php?filesrc=/etc/hosts: A PHP backdoor file manager was found.
	+ /wordpresswp-content/themes/twentyeleven/images/headers/server.php?filesrc=/etc/hosts: A PHP backdoor file manager was found.
	+ /wp-includes/Requests/Utility/content-post.php?filesrc=/etc/hosts: A PHP backdoor file manager was found.
	+ /wordpresswp-includes/Requests/Utility/content-post.php?filesrc=/etc/hosts: A PHP backdoor file manager was found.
	+ /wp-includes/js/tinymce/themes/modern/Meuhy.php?filesrc=/etc/hosts: A PHP backdoor file manager was found.
	+ /wordpresswp-includes/js/tinymce/themes/modern/Meuhy.php?filesrc=/etc/hosts: A PHP backdoor file manager was found.
	+ /assets/mobirise/css/meta.php?filesrc=: A PHP backdoor file manager was found.
	+ /login.cgi?cli=aa%20aa%27cat%20/etc/hosts: Some D-Link router remote command execution.
	+ /shell?cat+/etc/hosts: A backdoor was identified.

- SMB - Unix (Samba 2.2.1a)

- Webalizer version 2.01 - http://192.168.146.129/usage/usage_200909.html

- SSH - OpenSSH 2.9p2




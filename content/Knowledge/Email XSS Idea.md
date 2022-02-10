# Email XSS Idea

* Register account with target email
  * If target main mail is already registered, try second
* Set name or similar to your XSS code
* Server will send email to target
  * *"Hello \[NAME\] ..."*
* Programmers won't necessarily think to protect against XSS
  * *"It's just email"*
* Especially PHP will be vulnerable, as mail content is often built & sent directly from PHP
  ````php
  // ...
  $name = ''
  $email = 'Hello ' . $name . ', ...';
  
  // PHP makes sending mail rather easy
  sendmail('...', $email);
  ````

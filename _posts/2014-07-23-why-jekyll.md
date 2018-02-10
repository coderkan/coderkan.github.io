---
layout: post
title: "Why Jekyll?"
description: 
headline: 
modified: 2014-07-23
category: webdevelopment
tags: [jekyll]
imagefeature: 
mathjax: 
chart: 
comments: true
featured: true
---

Well, I guess it's quite obvious that I really enjoy working with Jekyll — with good reasons — so let me just briefly suggest some of the benefits of using a static site generator in favor of a heavy dynamic, database driven content management system.

- **Speed**: Static HTML pages are small, lightweight and perform blazingly fast. You’ll notice the difference.

- **Version Control**: Contents and files remain on your computer. Perform backups or keep track of changes via GIT or SVN — *it’s quite easy without a database.*

- **Flexibility**: Ruby and Liquid — *Jekyll’s foundation* — empower you to easily extend its functionality. Or just use one of [many plugins](http://jekyllrb.com/docs/plugins/) created by a striving community.

- **Security**: Anything you’ll ever put on your server are static files — chances are good that *you’ll never need to worry* about security concerns anymore.


```html
<form role="form" action="sendmail.php" method="post" style="text-align:center;margin-top:50px;" >
	<div>
		<input id='email' type="email" name="_mail"  placeholder="E-mail">
	</div>
	<br>
	<div>
		<input id = 'subject' type="text" name="_subject" placeholder="Subject">
	</div>
	<br>
	<textarea id='mailBody' name="_body" rows="12"></textarea>
	<br>
	<button  type="submit" name="submit" >Send E-mail</button>
</form>
```

This code will show you like below image. 


 <p align="center">
    <img src="img/form_preview.png">
</p>


Then we create a file called **sendmail.php** in project folders. Then we type this code.

```php
<?php

/**
 * This example shows settings to use when sending via Google's Gmail servers.
 * This uses traditional id & password authentication - look at the gmail_xoauth.phps
 * example to see how to use XOAUTH2.
 * The IMAP section shows how to save this message to the 'Sent Mail' folder using IMAP commands.
 */
//Import PHPMailer classes into the global namespace
use PHPMailer\PHPMailer\PHPMailer;
use PHPMailer\PHPMailer\Exception;

require 'PHPMailer-6.0.3/src/Exception.php';
require 'PHPMailer-6.0.3/src/PHPMailer.php';
require 'PHPMailer-6.0.3/src/SMTP.php';

if(isset($_POST['submit'])){

	$_subject =  $_POST['_subject'];
	$_mail =  $_POST['_mail'];
	$_body =  $_POST['_body'];

    $mail = new PHPMailer;
    
	//Tell PHPMailer to use SMTP
	$mail->isSMTP();

	$mail->CharSet = 'UTF-8';
	//Enable SMTP debugging
	// 0 = off (for production use)
	// 1 = client messages
	// 2 = client and server messages
	$mail->SMTPDebug = 0;
	//Set the hostname of the mail server
	$mail->Host = 'smtp.gmail.com';
	// use
	// $mail->Host = gethostbyname('smtp.gmail.com');
	// if your network does not support SMTP over IPv6
	//Set the SMTP port number - 587 for authenticated TLS, a.k.a. RFC4409 SMTP submission
	$mail->Port = 587;
	//Set the encryption system to use - ssl (deprecated) or tls
	$mail->SMTPSecure = 'tls';
	//Whether to use SMTP authentication
	$mail->SMTPAuth = true;
	//Username to use for SMTP authentication - use full email address for gmail
	$mail->Username = "yourmailadresorusername";
	//Password to use for SMTP authentication
	$mail->Password = "yoursecretpassword";
	//Set who the message is to be sent from
	$mail->setFrom('yourmailadress', 'Info');
	//Set an alternative reply-to address
	//$mail->addReplyTo('replyto@example.com', 'First Last');
	//Set who the message is to be sent to
	$mail->addAddress($_mail, 'Sent Name');
	//Set the subject line
	$mail->Subject = $_subject; //'PHPMailer GMail SMTP test';
	//Read an HTML message body from an external file, convert referenced images to embedded,
	//convert HTML into a basic plain-text alternative body
	//$mail->msgHTML(file_get_contents('contents.html'), __DIR__);

	$msgValue = $_body; 
	$mail->msgHTML($msgValue);
	//Replace the plain text body with one created manually
	//$mail->AltBody = 'This is a plain-text message body';
	//Attach an image file
	//$mail->addAttachment('images/phpmailer_mini.png');
	//send the message, check for errors
	if (!$mail->send()) {
        echo 'Send e-mail failure';
	    echo "Mailer Error: " . $mail->ErrorInfo;
	} else {
        // Send Successfully
        echo 'Send e-mail successfully';
	    //Section 2: IMAP
	    //Uncomment these to save your message in the 'Sent Mail' folder.
	    #if (save_mail($mail)) {
	    #    echo "Message saved!";
	    #}
	}
}else {
	//echo "Not Post";
}
?>
```


If that still doesn’t convince you to at least give it a try, I’d like to encourage you to head over to the Jekyll website and see it for yourself.

**Heck, it’s that good** — I even wrote all of the guides for the theme documentation with it!

Enjoy!
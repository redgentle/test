# 이메일 수집 PHP파일

Your include statement would look like

  <?php include('includes/contact_form.php'); ?>


------------------------------------------
-------- PHP Simple Contact Form ---------
------------------------------------------

-------- Version - 2.1 ------------------
-------- Author - Jigowatt Ltd -----------
-------- URL - www.jigowatt.co.uk --------



-------- Description ---------------------


A self-contained PHP contact form, easily integrated with already formed pages.


- File List

- /assets
--- error.gif
--- success.gif

- contact_form.php
- stylesheet.css



-------- Installation --------------------


Below you will find documentation for install or inclusion into your website.



- Step 1

Unzip the files, be sure to check it's contents against the above file list.


-- BACKUP BACKUP BACKUP --

It is important you keep a fresh copy of the script files incause of corruption, we do not offer
ongoing support for this script.


- Step 2

For simple inclusion of the contact form, page paste the following code in your existing PHP page.


<?php include('contact_form.php'); ?>


Note: You must make sure you include relative to the file you are including from.
	  e.g. If contact_form.php is located in a folder called 'includes' and you are including from a base
	  directory file such as index.php

	  Your include statement would look like

	  <?php include('includes/contact_form.php'); ?>


- Step 3

In the header of your website be sure to include the contact form style.


<link href="stylesheet.css" rel="stylesheet" type="text/css" />


Suggestion: Instead of this piece of code, why not copy the style for the contact page into your
existing stylesheet, merging any conflicts i.e. body or html tags?


- Step 4

Line 81:

$address = "example@themeforest.net";

Edit this to contain the email address that you want the form information sent to, this is the
only important confirguration option.


- Step 5

Note: If your page already has a HTML header you will receive a headers already sent error
after inserting the above, you must remove the following from the file contact_form.php if this is the
case.

Line 1:

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
"http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd"> <html
xmlns="http://www.w3.org/1999/xhtml">

<head> <meta http-equiv="content-type" content="text/html; charset=windows-1250">
<title>Simple PHP Contact Form</title> <link href="stylesheet.css" rel="stylesheet" type="text/css" /> </head>

<body>


And remove the end tags.

Lines 183-184:

</body>
</html>


- Step 6

Upload the changed and configured files to your server.

- Step 7 (Optional)

To enable the optional Phone Number validated field,

Uncomment the following (remove // from beginning of the lines)

Line 27:   $phone	= '';

Line 36:   $phone	= $_POST['phone'];

Line 53:   } else if(!is_numeric($phone)) {
				$error = '<div class="error_message">Attention! Phone number can only contain digits.</div>';


Swap comment tags or delete the appropriate.

Line 101:   $e_reply = "You can contact $name via email, $email or via phone $phone";
Line 102   $e_reply = "You can contact $name via email, $email";

Uncomment HTML code (Remove <!-- and --> tags from around the code)

Line 143:  <label for=phone accesskey=P><span class="required">*</span> Phone</label>
                 <input name="phone" type="text" id="phone" size="30" value="<?php echo $phone; ?>" />

		 <br />

- Finished.

Note: Send a test email using the form to test the installation. Enjoy the script.

-------- CHANGE LOG ----------------------

31/10/2011 - Fixed deprecated PHP code, added error mail checking
24/06/2009 - Updated readme.txt for phone number validation.
24/06/2009 - Added support for phone number and digit validation.

-------- FAQ -----------------------------

There are several other configuration options in contact_form.php these are highlighted and described
near each line similar to the following.

// Configuration option.
// Description and example of the configured option.

Feel free to change these options but be sure to BACKUP before you edit the script files.



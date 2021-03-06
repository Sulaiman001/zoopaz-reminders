zoopaz-reminders
================

A simple webapp that interfaces with the UNIX at command to send simple email notifications. Use a carrier email address for text messages.

Setup
=====

1
-

Add similar lines to `/etc/sudoers` so that your webserver user can execute the `at`, `atq` and `atrm` commands.

    ALL ALL=NOPASSWD: /usr/bin/at
    ALL ALL=NOPASSWD: /usr/bin/atq
    ALL ALL=NOPASSWD: /usr/bin/atrm
    
Future versions will use `/etc/at.allow`.

2
-

Copy `example.config.php` to `config.php`.

1. Add all of the email address for which you want to receive notifications to the `$emails` array.

If you use a carrier email to text address you can send text messages easily. Here's a large list of carriers and the format.

2. Update `$timezone` to one of the accepted values at [http://us3.php.net/manual/en/timezones.php](http://us3.php.net/manual/en/timezones.php).

3. Set `$msgType` to indicate if you want the reminder message to appear in the email subject, body or both.

[http://www.emailtextmessages.com/](http://www.emailtextmessages.com/)

Screenshot
==========

Click thumbnail for full-size screenshot.

<a target="_blank" href="img/zoopaz-reminders.png"><img style="max-width:100%;" src="img/small.zoopaz-reminders.png" alt="zoopaz-reminders.png" /></a>

=== Plugin Name ===
Contributors: jeff@pyebrook.com
Donate link: https://www.paypal.com/cgi-bin/webscr?cmd=_s-xclick&hosted_button_id=JQ8L23G6D3ANJ
Tags: throttle,queue,spam,uce,gmail,smtp,non-delivery,ndr,pop,pop3,phpmail,wp-mail,wp_mail,email,notification,notify,subscribe,subscription
Requires at least: 3.0
Tested up to: 3.1.1
Stable tag: trunk

Queue, Throttle, Send SMTP emil through multiple providers.  Automatic resend when non-delivery detected.

== Description ==

Send mail using SMTP without exceeding the the rate allowed by your mail provider(s). Mail can be sent using multiple 
user logins/passwords to give fault tolerance and make each mail message somewhat unique so that it is less likely to 
be flagged as SPAM/UCE by either your or the downstream mail providers.  Messages can be automatically reset when 
the plugin detects Non-delivery messages (NDRs) returned from mail sent by the plugin.

Email can be throttled per outbound SMTP account.  Limits can be set for maximum number of recipients per hour and per day.


== Arbitrary section ==

= Non-Delivery Processing =

Non-Delivery (NDR) messaging processing note: plugin should recognize common non-delivery formats.  But, because non-deliveries are free form, and can be highly customized or specifically localized the plugin may not recognize the message.  If you provide a sample non-delivery message we can make the plug-in a little smarter.
 
= Feature List =

Key Features:

1. Sends mail via SMTP 
1. Send mail no faster than the configured number of recipients per hour/day.  Keeps you in complience with your providers email sending limits.
1. Configure multiple SMTP accounts to use for sending messages (Gmail, MSN, Go-daddy, etc)
1. Process non-delivery messages and automatically resend messages
1. Keep record of sent mail messages so that you can prove to your provider you didn't send SPAM
1. Automatically stops sending email when errors encountered, auotmatically restarts after configured period of time 
1. Dashboard display of mail sending statistics

Benefits:

* Using multiple email accounts makes it less likely that your email will be incorrectly flagged as SPAM by downstream providers 
* Use in combination with other email newsletter, sending and formatting WordPress plug-ins 
* Reduces non-delivered mail due to invalid SPAM flagging or exceeding near or downstream provider sending/recieving limits  



== Installation ==


1. Upload the files to the /wp-content/plugins/tumblr-importer/ directory.
2. Activate the plugin through the 'Plugins' menu in WordPress.
3. Using the Mail Queues->Settings menu configure Message Header Options
4. Using the Mail Queues->Settings menu configure Non-Delivery Report (NDR) Processing options
5. Using the Mail Queues->Setup Queues menu define one or more message sned queues (accounts)
6. Using the Mail Queues->Test Mail Queueing menu send a test message to be sure everything is working 
 

== Frequently Asked Questions ==

= How are non-delivery messages retrieved? =
Configure a single mailbox to collect non-delivery messages.  Setup each sending mailbox to forward any messages received to that single mailbox.  The plug-in accesses that mailbox using the POP3 protocol.  User name a password for the POP3 mailbox are configured in the settings page.

= How many queues can the plugin support? =
No limit really, tested in excess of 20 simultanious SMTP queues 


= Does the plugin work with gmail? =
Yes. also it has been tested with MSN, Dreamhost, Go Daddy, and self hosted SMTP servers

== Screenshots ==

1. Message Queues Status Display
2. Message Queues Enable/Disable, Header Options
3. Queueing and Dequeing Options, Non-Delivery Processing Options
4. Non-Delivery Processing Options, Debugging and Testing Options
5. Stalled Mail Display
6. Message Queue Test Message Generation
7. Setup new SMTP mail Queue

== Changelog ==

= 1.0 =
* Initial public release version

== Upgrade Notice ==

= 1.0 =
Initial release



A very simple shell script to replace sendmail on single-user systems when only local mail is needed (i.e. for crond reports, etc.).  The script replaces the sendmail binary in /usr/sbin and deposits all mail messages into the local mail box of a single user.
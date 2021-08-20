# Email

A short [intended to be] distro agnostic script, meant to setup postfix and mailutils(debian) respectively mailx(suse/fedora) from scratch.

The script is specially constructed to receive a set of parameters, that when correctly given, allow the script to configure postfix with an email relay host.

The parameters can be given on one line, following the script name. 

The script should be run as root as such: - note the second parameter, which is the smtp port, can vary. 465 is used as an example, as it works with smtp.gmail.com and outlook.office365.com 


sudo ./setmail mail.example.com 465 username password

The script parameters are injected into the postfix/main.cf file as well as the postfix/sasl_passwd reference file.

Note that for suse, you will have to manually specify the "smtp_tls_CAfile ="  location after you have created/imported a valid one, otherwise your emails will go directly to SPAM. On pure fedora and debian systems and their derivatives, this problem does not exist.

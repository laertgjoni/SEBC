[root@ip-172-31-18-79 security]# kinit test
Password for test@EXAMPLE.COM:
[root@ip-172-31-18-79 security]# klist -f
Ticket cache: FILE:/tmp/krb5cc_0
Default principal: test@EXAMPLE.COM

Valid starting     Expires            Service principal
10/19/17 12:59:18  10/20/17 12:59:18  krbtgt/EXAMPLE.COM@EXAMPLE.COM
        renew until 10/19/17 12:59:18, Flags: FRI
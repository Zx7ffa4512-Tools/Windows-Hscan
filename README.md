Windows-Hscan
=============

Hscan
<Usage>:  hscan.exe -h <startIP> [<endIP>] <options> [others]
          hscan.exe -f <hostlist_filename> <options> [others]
          hscan.exe -report -h <startIP> [<endIP>]
          hscan.exe -report -f <hostlist_filename>
<Options>:
          -name    --  check hostname of target
          -port    --  check default common ports
          -ftp     --  check FTP weak accounts
          -ssh     --  check SSH vulnerability
          -telnet  --  check TELNET vulnerability
          -smtp    --  check SMTP vulnerability
          -finger  --  check FINGER vulnerability
          -iis     --  check IIS vulnerability
          -cgi     --  check HTTP vulnerability
          -pop     --  check POP3 weak accounts
          -rpc     --  check RPC vulnerability
          -ipc     --  check NT weak accounts
          -imap    --  check IMAP weak accounts
          -mssql   --  check MSSQL weak accounts
          -mysql   --  check MYSQL weak accounts
          -cisco   --  check CISCO weak password
          -plugin  --  check PLUGIN vulnerability
          -all     --  check all the options
<Others>:
          -max <thread,host> special max thread and host,default is 120,40
          -time <timedout> special connect timed out ms,default is 10000
          -sleep <sleeptime> sleeptime of ftp/pop/imap brute,deafult is 200
          -ping    ping host before scan
          -report  this option is use to make report
<Example>:
          hscan.exe -h www.target.com -all -ping
          hscan.exe -h 192.168.0.1 192.168.0.254 -port -ftp -max 200,100
          hscan.exe -f hosts.txt -port -ipc -pop -max 300,50 -time 10000
<Notice>:
          if you wanna stop current scan,please press "F8"

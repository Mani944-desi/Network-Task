# Network-Task


To find the IP of Guvi.com


vagrant@ubuntu-bionic:~$ nslookup guvi.com
Server:         127.0.0.53
Address:        127.0.0.53#53

Non-authoritative answer:
Name:   guvi.com
Address: 104.21.79.166
Name:   guvi.com
Address: 172.67.146.154
Name:   guvi.com
Address: 2606:4700:3031::6815:4fa6
Name:   guvi.com
Address: 2606:4700:3037::ac43:929a

vagrant@ubuntu-bionic:~$ dig guvi.com

; <<>> DiG 9.11.3-1ubuntu1.18-Ubuntu <<>> guvi.com
;; global options: +cmd
;; Got answer:
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 25134
;; flags: qr rd ra; QUERY: 1, ANSWER: 2, AUTHORITY: 0, ADDITIONAL: 1

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 65494
;; QUESTION SECTION:
;guvi.com.                      IN      A

;; ANSWER SECTION:
guvi.com.               667     IN      A       104.21.79.166
guvi.com.               667     IN      A       172.67.146.154

;; Query time: 1 msec
;; SERVER: 127.0.0.53#53(127.0.0.53)
;; WHEN: Sat Jun 07 19:46:49 UTC 2025
;; MSG SIZE  rcvd: 69

######################################################################################################################################################

How do I find my CPU/memory usage of my server?.

vagrant@ubuntu-bionic:~$ top
top - 19:52:05 up  2:57,  1 user,  load average: 0.00, 0.00, 0.00
Tasks:  96 total,   1 running,  52 sleeping,   0 stopped,   0 zombie
%Cpu(s):  0.0 us,  0.0 sy,  0.0 ni,100.0 id,  0.0 wa,  0.0 hi,  0.0 si,  0.0 st
KiB Mem :  1008516 total,   245592 free,    96492 used,   666432 buff/cache
KiB Swap:        0 total,        0 free,        0 used.   761004 avail Mem

  PID USER      PR  NI    VIRT    RES    SHR S  %CPU %MEM     TIME+ COMMAND
 1926 vagrant   20   0  108348   5184   4024 S   0.3  0.5   0:00.98 sshd
14068 root      20   0       0      0      0 I   0.3  0.0   0:09.32 kworker/1:0
19350 vagrant   20   0   42244   3856   3264 R   0.3  0.4   0:00.01 top
    1 root      20   0  159868   9204   6760 S   0.0  0.9   0:02.32 systemd
    2 root      20   0       0      0      0 S   0.0  0.0   0:00.41 kthreadd
    4 root       0 -20       0      0      0 I   0.0  0.0   0:00.00 kworker/0:0H
    6 root       0 -20       0      0      0 I   0.0  0.0   0:00.00 mm_percpu_wq
    7 root      20   0       0      0      0 S   0.0  0.0   0:00.39 ksoftirqd/0
    8 root      20   0       0      0      0 I   0.0  0.0   0:01.08 rcu_sched
    9 root      20   0       0      0      0 I   0.0  0.0   0:00.00 rcu_bh
   10 root      rt   0       0      0      0 S   0.0  0.0   0:00.00 migration/0
   11 root      rt   0       0      0      0 S   0.0  0.0   0:00.33 watchdog/0
   12 root      20   0       0      0      0 S   0.0  0.0   0:00.00 cpuhp/0
   13 root      20   0       0      0      0 S   0.0  0.0   0:00.00 cpuhp/1
   14 root      rt   0       0      0      0 S   0.0  0.0   0:00.31 watchdog/1
   15 root      rt   0       0      0      0 S   0.0  0.0   0:00.24 migration/1
   16 root      20   0       0      0      0 S   0.0  0.0   0:00.16 ksoftirqd/1
   18 root       0 -20       0      0      0 I   0.0  0.0   0:00.00 kworker/1:0H
   19 root      20   0       0      0      0 S   0.0  0.0   0:00.01 kdevtmpfs
   20 root       0 -20       0      0      0 I   0.0  0.0   0:00.00 netns
   21 root      20   0       0      0      0 S   0.0  0.0   0:00.00 rcu_tasks_kthre
   22 root      20   0       0      0      0 S   0.0  0.0   0:00.00 kauditd
   24 root      20   0       0      0      0 S   0.0  0.0   0:00.01 khungtaskd
   25 root      20   0       0      0      0 S   0.0  0.0   0:00.00 oom_reaper
   26 root       0 -20       0      0      0 I   0.0  0.0   0:00.00 writeback
   27 root      20   0       0      0      0 S   0.0  0.0   0:00.00 kcompactd0
   28 root      25   5       0      0      0 S   0.0  0.0   0:00.00 ksmd
   29 root      39  19       0      0      0 S   0.0  0.0   0:00.00 khugepaged
   30 root       0 -20       0      0      0 I   0.0  0.0   0:00.00 crypto
   31 root       0 -20       0      0      0 I   0.0  0.0   0:00.00 kintegrityd
   32 root       0 -20       0      0      0 I   0.0  0.0   0:00.00 kblockd
   33 root       0 -20       0      0      0 I   0.0  0.0   0:00.00 ata_sff
   34 root       0 -20       0      0      0 I   0.0  0.0   0:00.00 md
   35 root       0 -20       0      0      0 I   0.0  0.0   0:00.00 edac-poller
vagrant@ubuntu-bionic:~$ free -h
              total        used        free      shared  buff/cache   available
Mem:           984M         94M        239M        636K        650M        743M
Swap:            0B          0B          0B
vagrant@ubuntu-bionic:~$ mpstat
Linux 4.15.0-213-generic (ubuntu-bionic)        06/07/25        _x86_64_        (2 CPU)

19:52:22     CPU    %usr   %nice    %sys %iowait    %irq   %soft  %steal  %guest  %gnice   %idle
19:52:22     all    0.07    0.00    0.28    0.04    0.00    0.03    0.00    0.00    0.00   99.57

###########################################################################################################################################################################

Test the connectivity between 2 nodes?

vagrant@ubuntu-bionic:~$ ping guvi.com
PING guvi.com (104.21.79.166) 56(84) bytes of data.
64 bytes from 104.21.79.166 (104.21.79.166): icmp_seq=2 ttl=56 time=19.4 ms
64 bytes from 104.21.79.166 (104.21.79.166): icmp_seq=4 ttl=56 time=19.4 ms
64 bytes from 104.21.79.166 (104.21.79.166): icmp_seq=6 ttl=56 time=16.8 ms
64 bytes from 104.21.79.166 (104.21.79.166): icmp_seq=7 ttl=56 time=17.7 ms
64 bytes from 104.21.79.166 (104.21.79.166): icmp_seq=8 ttl=56 time=17.3 ms
64 bytes from 104.21.79.166 (104.21.79.166): icmp_seq=9 ttl=56 time=18.2 ms
64 bytes from 104.21.79.166 (104.21.79.166): icmp_seq=10 ttl=56 time=18.6 ms
64 bytes from 104.21.79.166 (104.21.79.166): icmp_seq=11 ttl=56 time=18.1 ms
64 bytes from 104.21.79.166 (104.21.79.166): icmp_seq=12 ttl=56 time=18.0 ms
64 bytes from 104.21.79.166 (104.21.79.166): icmp_seq=13 ttl=56 time=18.0 ms
^C
--- guvi.com ping statistics ---
13 packets transmitted, 10 received, 23% packet loss, time 12094ms
rtt min/avg/max/mdev = 16.844/18.218/19.494/0.797 ms
vagrant@ubuntu-bionic:~$ tracert guvi.com

Command 'tracert' not found, did you mean:

  command 'tracert6' from deb ndisc6
  command 'tracer' from deb pvm-dev

Try: apt install <deb name>

vagrant@ubuntu-bionic:~$ traceroute guvi.com
traceroute to guvi.com (104.21.79.166), 30 hops max, 60 byte packets
 1  _gateway (192.168.0.1)  1.819 ms  2.000 ms  1.950 ms
 2  100.79.0.1 (100.79.0.1)  5.240 ms  5.475 ms  5.427 ms
 3  * * *
 4  * * *
 5  * * *
 6  * * *
 7  * * *
 8  172.31.22.76 (172.31.22.76)  15.926 ms  16.610 ms  16.773 ms
 9  * * *
10  162.158.226.89 (162.158.226.89)  26.314 ms 162.158.226.17 (162.158.226.17)  17.629 ms 162.158.226.83 (162.158.226.83)  17.599 ms
11  104.21.79.166 (104.21.79.

####################################################################################################################################################################################################

I have deployed an application in guvi.com:9000, and logs show my app is running, but I’m unable to view the page. Check whether my port is open or not ?

raceroute to guvi.com (104.21.79.166), 30 hops max, 60 byte packets
 1  _gateway (192.168.0.1)  1.819 ms  2.000 ms  1.950 ms
 2  100.79.0.1 (100.79.0.1)  5.240 ms  5.475 ms  5.427 ms
 3  * * *
 4  * * *
 5  * * *
 6  * * *
 7  * * *
 8  172.31.22.76 (172.31.22.76)  15.926 ms  16.610 ms  16.773 ms
 9  * * *
10  162.158.226.89 (162.158.226.89)  26.314 ms 162.158.226.17 (162.158.226.17)  17.629 ms 162.158.226.83 (162.158.226.83)  17.599 ms
11  104.21.79.166 (104.21.79.166)  16.713 ms  18.082 ms  17.751 ms
vagrant@ubuntu-bionic:~$ tenet guvi.com 9000

Command 'tenet' not found, did you mean:

  command 'telnet' from deb telnet
  command 'telnet' from deb inetutils-telnet
  command 'telnet' from deb telnet-ssl

Try: apt install <deb name>

vagrant@ubuntu-bionic:~$ telnet guvi.com 9000
Trying 172.67.146.154...



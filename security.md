##### clamav 文件病毒查杀
1. 更新病毒库数据。
```
[root@bigdata03 clamav]# freshclam 
ClamAV update process started at Tue Aug 31 23:48:06 2021
daily database available for update (local version: 26279, remote version: 26280)
Current database is 1 version behind.
Downloading database patch # 26280...
Time:    0.9s, ETA:    0.0s [========================>]   24.08KiB/24.08KiB
Testing database: '/var/lib/clamav/tmp.9a20cce19b/clamav-719a3dd22ca3498ece0af71967bb1981.tmp-daily.cld' ...
Database test passed.
daily.cld updated (version: 26280, sigs: 1969710, f-level: 90, builder: raynman)
main.cvd database is up-to-date (version: 61, sigs: 6607162, f-level: 90, builder: sigmgr)
bytecode.cvd database is up-to-date (version: 333, sigs: 92, f-level: 63, builder: awillia2)
```

2. 扫描代码库。查看代码中是否存在病毒
```
[root@bigdata03 SkybilityHA]# clamscan --infected --recursive .

----------- SCAN SUMMARY -----------
Known viruses: 8561636
Engine version: 0.103.3
Scanned directories: 669
Scanned files: 4295
Infected files: 0
Data scanned: 138.80 MB
Data read: 67.28 MB (ratio 2.06:1)
Time: 71.543 sec (1 m 11 s)
Start Date: 2021:09:01 12:27:57
End Date:   2021:09:01 12:29:09
```

##### nessus essentials
安装，使用rpm


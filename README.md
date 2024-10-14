  1 #!/bin/bash
  2 for x in {1..10}
  3 do
  4 date +"%H:%M:%S"
  5 ps -ef | wc -l
  6 sleep 2 #sleep 5
  7 done
  8 cat /proc/cpuinfo > proc.txt
  9 #name=$(grep 'NAME=' /etc/os-release)
 10 @echo "$name" > proc.txt
 11 grep "^NAME=" /etc/os-release | awk -F= '{print $2}' >> proc.txt
 12 touch file{50..100}.txt

PiHole List
Black list from blacklist.source file, after injected to gravity.db, then requery with distinct, exported to blacklist.txt

White list created as daily family need (insert to gravity.db)

$ sqlite3 gravity.db
sqlite> .headers off
sqlite> .mode list
sqlite> .output blacklist.txt
sqlite> select distinct domain from gravity order by domain;
sqlite> .quit

https://raw.githubusercontent.com/djykstra/PiHole/main/blacklist-1.txt
https://raw.githubusercontent.com/djykstra/PiHole/main/blacklist-2.txt
https://raw.githubusercontent.com/djykstra/PiHole/main/blacklist-3.txt
https://raw.githubusercontent.com/djykstra/PiHole/main/blacklist-4.txt




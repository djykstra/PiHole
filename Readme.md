PiHole List
Black list from blacklist.source file, after injected to gravity.db, then requery with distinct, removed from basic life list then exported to blacklist.txt

Basic life list services (desktop and mobile device)
- google browser
- google mail
- google classroom
- youtube

White list created as daily family need (insert to gravity.db)


$ sqlite3 gravity.db
sqlite> .headers off
sqlite> .mode list
sqlite> .output blacklist.txt
sqlite> select distinct domain from gravity order by domain;
sqlite> .quit




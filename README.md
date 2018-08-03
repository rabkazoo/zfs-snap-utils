# zfs-snap-utils
yet another snapshot util set :)
a "snap" cmd front for zfs and some utils. Specifically for freebsd zfs root.
I keep hourly and 3 day snapshots.
The "snap" command I use shows relative path entries and can do ls/get(cp))/diff/create/destroy
works only on the zfs root usr/home for now! which is all I need it for.
eg:
snap -h # show help
snap ls # show snapshots
snap ls -l 1: show contents of current dir 1 hour ago
snap diff 1:foo 
snap get 1:foo
snap get 2_days_ago:foo

"snapnhours" create/keep the last N (10 default) hours of snapshots
"snapdaily" ditto for 3 days
example crontab enry for the above.


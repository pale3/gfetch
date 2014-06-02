gfetch is GMAIL retriver, usefull for tiling WM while combining it with conky or dzen.

NOTE: if you are using conky then append "${if_running gfetch}" to your conkyrc file. 
This way you are sure that you won't get prefixed MAIL count if you have one defined in 
your conkyrc while we dont have net access.

Also gfetch can determine if we have net acees or not. Here issex .of conkyrc:
     
	${if_running gfetch}MAIL: ${execi 5 cat /tmp/gfetch/mcount}${endif} 

after emerging gfetch, copy gfetchrc from /usr/share/gfetch/ to your $HOME prefixed with dot.

	cp /usr/share/gfetch/gfetchrc $HOME/.gfetchrc
        

gfetch is ment to be started as daemon. Use "-D" switch for that purpose.

	ex: gfetch -D

it is possible to kill daemon with "-k" switch

	ex: gfetch -k

while daemon is running you can force check mails with "c" or "check" switch otherwise nasty err will happend

	ex: gfetch c

if you missed notification, or you just wana see subjects of mails, then you can use "l" or "list" swicth

	ex: gfetch list


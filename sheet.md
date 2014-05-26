        $ emerge -avDu @world
                -a: ask the user about the emerge
                -v: verbose
                -D: Deep dependency resolving
                -u: update

                Also usefull: --newuse: emerge those pkgs with changed flags
                -q: for quiet output 

        $ emerge -C <pkgname>
Removes the pkg. Be carefull or you may uninstall a critical package

        $ genlop -tc
  -c: display the currently compiling packages
  -t: calculate merge time for the specific package

Also usefull:
  -i: extra infos for the selected package
  -l: show full merge history

#tail -f /var/log/emerge-fetch.log
  Shows the package fetch progress

#emerge --sync
  Update emerge db

#eix-update
  Run after `emerge --sync` to update eix db

#cat /var/lib/portage/world
  See contents of world file

#less /usr/portage/profiles/use.desc
  See description of each useflag

#eselect
  Usefull tool to help you select current versions and also read Gentoo news (with eselect news list/read)

General Linux Commands
----------------------
        $ du -hsx * | sort -rh | head -10
Show the 10 biggest folders in . in sorted order
        find . -type f -size +50000k -exec ls -lh {} \; | awk '{ print $9 ":" $5 }'
Find for files more than 50000kb. (change it according to your needs)

# WeeChat scripts by FiXato
******************************************************************************

My personal repository of scripts for the WeeChat chat client, www.weechat.org

Scripts I've written to add features to WeeChat I felt were missing.

## Overview

* clone_scanner.py

    A Clone Scanner that can manually scan channels and automatically scans 
    joins for users on the channel with multiple nicknames from the same host.

* listbuffer.py (for now still developed in its own repository)

    Show /list results in a common buffer and interact with them.

* buffer_swap.py

    Swap two buffers' positions. A feature requested by Kakazza in #weechat. 
    `/swap [buffer] <buffer to swap with>`

    Example: 
    `/swap #weechat #weechat-fr`

## Script ideas
* Task https://savannah.nongnu.org/task/index.php?11351
    "Allow buffer names for irc.msgbuffer"

    (Custom (s)notices buffer)

* buffer_stats:

    Output stats about the number of different buffers. Something like:

        Total of 55 buffers: 1 core, 6 server buffers, 43 channel buffers, 
        3 queries, 2 plugin buffers; 10 of them are merged.

* advanced highlights manager: 

    Assign target buffers & colours to highlights. Dynamically create target 
    buffer if necessary
    
    Example: `/highlight add /(lol|nyan-?)cat/ nyancats`
    
    When the highlight would get triggered, it will create a new buffer,
    `python.nyancats`, —should the buffer not already exist— and display the
    message (+source buffer) in it.

## Installation instructions
******************************************************************************

* `mkdir -p ~/src/github/FiXato && cd ~/src/github/FiXato`
* `git clone git://github.com/FiXato/weechat_scripts.git`
* `cd weechat_scripts`
* `ln -s *.py ~/.weechat/python/`
* and if you want to autoload: `ln -s *.py ~/.weechat/python/autoload/`


## History
******************************************************************************

See headers of individual scripts for their Changelogs.


## Notes on Patches/Pull Requests
******************************************************************************

1. Fork the project.
2. Make your feature addition or bug fix.
3. Add tests for it (even though I don't have tests myself at the moment). 
  This is important so I don't break it in a future version unintentionally.
4. Commit, but do not mess with gemspec, version, history, or README.
  Want to have your own version? Bump version in a separate commit!
  That way I can ignore that commit when I pull.
5. Send me a pull request. Bonus points for topic branches.
6. You'll be added to the credits.

## Acknowledgements
******************************************************************************

Thanks go out to:

* Sebastien "Flashcode" Helleu, for developing the kick-ass IRC client WeeChat
    and the iset.pl script which inspired me to write listbuffer.py.
* Nils "nils_2" Görs, for his contributions to iset.pl which served as
    example code for listbuffer.py.
* David "drubin" Rubin, for his urlgrab.py script, which also served
    as example code for listbuffer.py.
* ArZa, whose listsort.pl script helped me getting started with 
    grabbing the /list results for listbuffer.py and whose kickban.pl script
    served as an example for handling infolists for clone_scanner.py.
* Khaled Mardam-Bey, for making me yearn for similar /list support in 
    WeeChat as mIRC already offered. :P


## Copyright
******************************************************************************

Copyright (c) 2011 Filip H.F. "FiXato" Slagter,
    <FiXato [at] Gmail [dot] com>
    http://google.com/profiles/FiXato

See LICENSE for details.
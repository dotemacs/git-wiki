## git-wiki: even leaner version ##

Leaner version of git-wiki:

 * wiki & pages all in one repo

 * no **haml**, as **erb** is already part of the system, less to
   worry about when upgrading

 * all the pages directly under '/'

 * **maruku** for markup as it supports markdown extra

This is my version of git-wiki, which is a fork of Decklin Foster's,
which in turn is a fork of the original by Simon Rozet.

### Simple Install & Configuration

Execute:

     gem install sinatra grit maruku
     git clone git@github.com:dotemacs/git-wiki.git ~/wiki
     cd ~/wiki

Edit **git-wiki.rb**'s configure block and put your options in e.g.:

     configure do
       GitWiki.wiki_path = "~/wiki"
       GitWiki.root_page = 'Home'
       GitWiki.extension = '.md'
       GitWiki.link_pattern = /\[\[(.*?)\]\]/
     end

Run:  

     ./git-wiki.rb

and point browser to [http://localhost:4567/](http://localhost:4567/)

License
-------

    Copyright (C) 2008 Simon Rozet <simon@rozet.name>
    Copyright (C) 2009 Decklin Foster <decklin@red-bean.com>
    Copyright (C) 2010 Aleksandar Simić <asimic@gmail.com>

               DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE
                       Version 2, December 2004

    Everyone is permitted to copy and distribute verbatim or modified
    copies of this license document, and changing it is allowed as long
    as the name is changed.

               DO WHAT THE FUCK YOU WANT TO PUBLIC LICENSE
      TERMS AND CONDITIONS FOR COPYING, DISTRIBUTION AND MODIFICATION

     0. You just DO WHAT THE FUCK YOU WANT TO.

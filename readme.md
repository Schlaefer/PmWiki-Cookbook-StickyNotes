What
====

![Image](http://i49.tinypic.com/o5b2p1.png)

For the Admins
==============
Requirements
------------
* Requires probably PmWiki 2.0 and higher
* Last tested on PmWiki 2.2.36

Install
-------
1. put this script into your cookbook folder
2. include it into your config.php: 

    include_once("$FarmD/cookbook/postitnotes.php");

3. !!! not longer supported since 2.1 !!! if you want to use fancy notes download [this package][pdl] and put it into pub/cookbook/postitnotes

[pdl]: http://schlaefer.macbay.de/uploads/Main.StickySandbox/fancynoteimages.zip
    

Customization
-------------
* [optional] $PostItNotesEditLink = <true|false>
	* default = true 
	* shows an edit link

* [optional] $PostItNotesSkinDirUrl
	* default = /cookbook/postitnotes
	* path to the images relative to the pub directory


For the Users
=============
Normal
------
### Simple
Simple notes are only intended to hold one paragraph with no advanced markup.

    (:note Title | Content:)

### Simple Hidden
the hidden note is a normal note that only shows the title of the note until you clicked on the title

    (:notehidden Title | Content:)

### Block
The block note allows as many wiki markup as you want in Title and Content

	(:noteblock <color=argument> <float=right(default)|left> <hidden=false(default)|true>:)
	Title
	(:notecontent:)
	Content
	(:noteblockend:)

The color argument can be:

* yellow(default)|blue|gray|pink|purple|green - predefined colors in script
* a hex color value like `#cceecc`
* a websafe colorname in capitals like YELLOW, BLACK ... 

Fancy
-----

!!!Fancy is not longer supported by this script since version 2.1!!!

Fancy notes have a nice background image. Click on the pen to edit the note. 

### Simple Fancy
    (:notefancy Title | Content:)

### Block Fancy
    (:noteblockfancy <float=right(default)|left>:)
    Content
    (:noteblockend:)

   

For Developers
==============
Version History
---------------
* 2012-05-25 – Schlaefer
    * [new] notes are now styled with divs instead of table (upgrade your custom styles)
    * [new] style fancy is not supported anymore
* 2.0.4 - 2009-07-20 - Rik Blok
    * [bugfix] compatibility with TableEdit recipe (postitnotes.php needs to be "included" after tabledit.php)
* 2.0.3 - 2006-02-12 - Schlaefer
    * [feature] argument "width" for blocknotes
* 2.0 - 2006-02-09 - Schlaefer
    * Major Rewrite - Unifies all note types in one Markup
* 1.8.3 - 2005-10-24 - Schlaefer
    * [feature] $PostItNotesEditLink
* 1.8.2 
* 1.8.1 - 2005-09-04 - Schlaefer
    * [bugfix] in HandleEditNote
* 1.8 - 2005-08-30 - Schlaefer
    * [feature] edit links in simple and hidden notes
* 1.7 - 2005-08-30 - Schlaefer
    * [feature] edit links in fancy notes
* 1.6.2 - 2005-08-30 - Schlaefer
    * [code] phpdoc code comments 
    * [feature] $PostItNotesSkinDirUrl defines where the images for the fancy style life
* 1.6.1 - 2005-08-23 - Schlaefer
    * [bugfix] sometimes websafe colors were wiki links in noteblock 
* 1.6 - 2005-08-23 - Schlaefer
    * [feature] hidden option for block notes 
* 1.5 - 2005-08-23 - Schlaefer
    * [feature] hidden simple note
    * [change] fancy images have to be in the skin folder
    * code cleanup and comments
* 1.4 Schlaefer August 12, 2005, at 05:48 AM
    * Fancy style 
* 1.2 Schlaefer March 24, 2005, at 06:32 AM
    * Inspired by mailinglist discussion added block mode with OS X sticky colors and float parameter 
* 1.1 Schlaefer 19 November 2004 17:23 Uhr
    * Bug fixed caused by wikilinks with vertical bar | 
* 1.0 First Release for apfelwiki.de - Schlaefer 

# Home Points Reward System
The Home Points Reward System is a project designed to help limit your family's access to the electronics that are taking over our lives.  While there are numerous family monitoring and control systems out there, none of them suited my needs.

##Features
1.  **Multi-Platform**.  The suite can monitor different platforms, Android (Kindle Tablets, Amazon TV, Android Phones), Windows PCs, Mac OS X, Linux, and possibly more if you can get the [Mono](http://www.mono-project.com/) framework running.  Android and Windows will be supported in the first release.  Apple iOS and OS X on next cycle.  Linux will be last because I want to encourage my kids to use it.
2. **Easy Parental Control**. It is easy for a parent to quickly grant or deny time on a device.
3. **Sharing of Time**. Multiple accounts and split time on a device, like two children combining their last 15 minutes each so they can both watch a 30 minute show.
4. **"Smart-Card" style implementation**.  To identify which children are on devices that do not have a built-in account system, a "smart-card" type of solution was needed.  It will utilize plug-in drives, like a SD card or USB thumb drive, as an identifier.  
5. **Home Automation Compatible**.  The system can shut down the power to devices by communicating to a home automation hub.  Z-Wave will be the first protocol supported.  The system will also present Z-Wave endpoints to allow third-party home automation apps for parental control on top of the built-in control interface.  The target case for this is blocking television and console game access where a software solution is too cost prohibitive.
6. **Detailed Monitoring and Control**.  Ultimately, this will be provide detailed monitoring and control to allow for scenarios where kids can do homework or research without using points (and possibly gaining points) while blocking gaming.  Also, this would allow only approved games to be played.  

##Target Hardware
The system is targeted to run on minimal hardware.  I am using the [Raspberry Pi 2 Model B](https://www.raspberrypi.org/products/raspberry-pi-2-model-b/) as various computing modules, although stronger computers could be used.

##Modules (aka Points)
There are four main modules in the system.
1. **Server**.  The server is the brain, the Master Control Program.  It receives communications from all other module points, serves up web pages, and talks to the Z-Wave devices.  This will be targeted to work on a Pi 2.
1. **Command Points**. These are the various interfaces that the parents work with.  The current targets are web pages and Z-Wave.
2. **Monitor Points**.  These are the services or processes that reside on the physical devices being monitored.  These report and listen to the server for instructions.
3. **Identification Points**.  These are Pi 2 devices hooked up to an SD card reader (like this) or exposed USB ports, either directly, through extension cables, or a hub.  The sole function of this device is to identify which children are at a device.

##Technologies
* Raspberry Pi
* C#
* Mono
* SQLite
* Z-Wave
* Windows 10 IoT
* AllJoyn
* ASP.NET
* Xamarin
* 

> Written with [StackEdit](https://stackedit.io/).


-----------------------------------------------------
###Notes and stuff to figure out Markdown
https://stackedit.io/editor

Markdown is intended to be as easy-to-read and easy-to-write as is feasible.

Readability, however, is emphasized above all else. A Markdown-formatted
document should be publishable as-is, as plain text, without looking
like it's been marked up with tags or formatting instructions. 

*italic* _italic_ **bold** __bold__

Hrm, this seems to be a lot like Reddit.

Inline style URL:
An [example](http://www.google.com "Title")

Reference style URL:
An [example][id]. Then, anywhere
else in the doc, define the link:

  [id]: http://example.com/  "Title"

![alt text](/path/img.jpg "Title")

![alt text][id]

[id]: /url/to/img.jpg "Title"


Header 1
========

Header 2
--------

# Header 1 #

## Header 2 ##

###### Header 6

1.  Foo
2.  Bar

*   A list item.

    With multiple paragraphs.

*   Bar


*   Abacus
    * answer
*   Bubbles
    1.  bunk
    2.  bupkis
        * BELITTLER
    3. burper
*   Cunning


> Email-style angle brackets
> are used for blockquotes.

> > And, they can be nested.

> #### Headers in blockquotes
> 
> * You can quote a list.
> * Etc.


`<code>` spans are delimited
by backticks.

You can include literal backticks
like `` `this` ``.


This is a normal paragraph.

    This is a preformatted
    code block.



---

* * *

- - - - 


Roses are red,   
Violets are blue.



# Bash BBC Radio

A bash script to play high quality BBC streams from the command line, via VLCs cvlc command.
It also displays now/next information much quicker than navigating to the bbc website.

Thanks to simoncn and clanger9 at the [Linn forums](http://forums.linn.co.uk/bb/showthread.php?tid=29518&pid=348776#pid348776 "MinimStreamer") for the stream links and [Steve Seear](http://steveseear.org/high-quality-bbc-radio-streams/ "Steve Seear") for pointing the way. Also to Tom Scott at the Beeb's [radiolabs](http://www.bbc.co.uk/blogs/radiolabs/2008/05/helping_machines_play_with_pro.shtml "radiolabs") for the schedule data streams.

    $ radio 6
    ==========================================================================================
    Playing BBC Radio 6 Music
    16:00 - 18:00 - Jarvis Cocker's Sunday Service
                    - John Cooper Clarke
    John Cooper Clarke sits in on the Sunday Service with two hours of classic nuggets.
    
    ####  Next
    * 18:00 - 20:00  Now Playing @6Music
    * 20:00 - 22:00  Stuart Maconie's Freak Zone
    * 22:00 - 00:00  Don Letts' Culture Clash Radio
    * 00:00 - 02:00  Guy Garvey's Finest Hour
    
    ==========================================================================================

## Depends on
Bash
wget
vlc (has to be in single instance mode)

## Install
put 'radio' and 'radio_streams' in the same folder, in your path. Make 'radio' executable.

## Usage
### list all available stations
    radio list

### list stations matching [pattern]
    radio list [pattern]
eg

    radio list s

or

    radio [pattern] list
eg

    radio w list

### play station matching pattern
    radio [pattern]
eg

    radio 4

### stop playing
    radio stop
*Will not work if VLC is not configured for single-instance mode*

### display now / next info
    radio [pattern] now
eg

    radio 1x now

### display the remainder of today's schedule
    radio [pattern] later
eg

    radio R5X later

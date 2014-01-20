magic-monitor
=============

Simple bash script, that generate html page with ok / fail items on udp packet arrive.

All you need - is socat: http://www.dest-unreach.org/socat/

Run monitor-state and send to server some udp packet. Example for linux:

    echo kernel_build_devel 0 > /dev/udp/<server_ip>/44
    
Refresh page and you'll see green (ok) tile

    kernel
    build
    devel

To create fail tile - second value in udp message must not be equal to 0.

# beanstalkd

This container will start [beanstalkd][] with the binlog enabled (`-b /data`) on
the default port `11300/tcp`. If you want to backup the binlog folder `/data`,
it's exposed as `VOLUME` and ready for `--volumes-from`.

# Usage

    $ docker run --rm -p 11300:11300 -t michaelcontento/beanstalkd
    $ telnet 127.0.0.1 11300
    Trying 127.0.0.1...
    Connected to 127.0.0.1.
    Escape character is '^]'.
    stats
    OK 802
    ---
    ... bunch of stats ...

    quit
    Connection closed by foreign host.

[beanstalkd]: http://kr.github.io/beanstalkd/

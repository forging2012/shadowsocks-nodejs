shadowsocks-nodejs
===========

shadowsocks-nodejs is a lightweight tunnel proxy which can help you get through
 firewalls. It is a port of [shadowsocks](https://github.com/clowwindy/shadowsocks).

The nodejs version has a better performance than the original Python version.

The protocol is compatible with the origin shadowsocks(if both have been upgraded to the
 latest version). For example, you can use a python client with a nodejs server.

usage
-----------

Edit `config.json`, change the following values:

    server          your server ip or hostname
    server_port     server port
    local_port      local port
    password        a password used to encrypt transfer
    timeout         in seconds

Put all the files on your server.  Run `node server.js` on your server. To run it in the background, run
`setsid node server.js`.

Put all the files on your client machine. Run `node local.js` on your client machine.

Change proxy settings of your browser into

    SOCKS5 127.0.0.1:local_port


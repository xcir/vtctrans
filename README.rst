==============
vtctrans
==============


-------------------------------
Re-format tool for varnishtest
-------------------------------

:Author: Shohei Tanaka(@xcir)
:Date: 2013-04-30
:Version: 0.0-alpha1
:Manual section: 1

ATTENTION
===========
This version is alpha quality.
work in progress now.


DESCRIPTION
===========
Re-format tool for varnishtest


Original log
---------------------------------------
::

  **** top   0.0 macro def varnishd=varnishd
  **** top   0.0 macro def pwd=/root/git/vtctrans
  **** top   0.0 macro def topbuild=/root/git/vtctrans/../..
  **** top   0.0 macro def bad_ip=10.255.255.255
  **** top   0.0 macro def tmpdir=/tmp/vtc.14768.43d2044f
  *    top   0.0 TEST test.vtc starting
  ***  top   0.0 varnishtest
  *    top   0.0 TEST example
  ***  top   0.0 server
  ***  top   0.0 server
  **   s1    0.0 Starting server
  **** s1    0.0 macro def s1_addr=127.0.0.1
  **** s1    0.0 macro def s1_port=52740
  **** s1    0.0 macro def s1_sock=127.0.0.1 52740
  *    s1    0.0 Listen on 127.0.0.1 52740
  ***  top   0.0 varnish
  **   s1    0.0 Started on 127.0.0.1 52740
  **   v1    0.0 Launch
  ***  v1    0.0 CMD: cd ${pwd} && ${varnishd} -d -d -n /tmp/vtc.14768.43d2044f/v1 -l 10m,1m,- -p auto_restart=off -p syslog_cli_traffic=off -a '127 . 0.0.1:0' -S /tmp/vtc.14768.43d2044f/v1/_S -M '127.0.0.1 41567' -P /tmp/vtc.14768.43d2044f/v1/varnishd.pid -sfile,/tmp/vtc.14768.43d2044f/v 1,1 0M
  ***  v1    0.0 CMD: cd /root/git/vtctrans && varnishd -d -d -n /tmp/vtc.14768.43d2044f/v1 -l 10m,1m,- -p auto_restart=off -p syslog_cli_traffic=of f  -a '127.0.0.1:0' -S /tmp/vtc.14768.43d2044f/v1/_S -M '127.0.0.1 41567' -P /tmp/vtc.14768.43d2044f/v1/varnishd.pid -sfile,/tmp/vtc.14768.4 3d2 044f/v1,10M
  ***  v1    0.0 PID: 14774
  ***  v1    0.0 debug| Platform: Linux,2.6.32-71.18.1.el6.x86_64,x86_64,-sfile,-smalloc,-hcritbit\n
  ***  v1    0.0 debug| 200 251     \n
  ***  v1    0.0 debug| -----------------------------\n
  ***  v1    0.0 debug| Varnish Cache CLI 1.0\n
  ***  v1    0.0 debug| -----------------------------\n
  ***  v1    0.0 debug| Linux,2.6.32-71.18.1.el6.x86_64,x86_64,-sfile,-smalloc,-hcritbit\n
  ***  v1    0.0 debug| \n
  ***  v1    0.0 debug| Type 'help' for command list.\n
  ***  v1    0.0 debug| Type 'quit' to close CLI session.\n
  ***  v1    0.0 debug| Type 'start' to launch worker process.\n
  ***  v1    0.0 debug| \n
  **** v1    0.1 CLIPOLL 1 0x1 0x0
  ***  v1    0.1 CLI connection fd = 9
  ***  v1    0.1 CLI RX  107
  **** v1    0.1 CLI RX| sqxplzwdiomlmrclsxcyswqpnychpwuh\n
  **** v1    0.1 CLI RX| \n
  **** v1    0.1 CLI RX| Authentication required.\n
  **** v1    0.1 CLI TX| auth 810e086c0c1024ee3960fac753c9aa4bf3488605303b99d2f0fe152fca93d9e5\n
  ***  v1    0.1 CLI RX  200
  **** v1    0.1 CLI RX| -----------------------------\n
  **** v1    0.1 CLI RX| Varnish Cache CLI 1.0\n
  **** v1    0.1 CLI RX| -----------------------------\n
  **** v1    0.1 CLI RX| Linux,2.6.32-71.18.1.el6.x86_64,x86_64,-sfile,-smalloc,-hcritbit\n
  **** v1    0.1 CLI RX| \n
  **** v1    0.1 CLI RX| Type 'help' for command list.\n
  **** v1    0.1 CLI RX| Type 'quit' to close CLI session.\n
  **** v1    0.1 CLI RX| Type 'start' to launch worker process.\n
  **** v1    0.1 CLI TX| vcl.inline vcl1 << %XJEIFLH|)Xspa8P\n
  **** v1    0.1 CLI TX| backend s1 { .host = "127.0.0.1"; .port = "52740"; }\n
  **** v1    0.1 CLI TX| \n
  **** v1    0.1 CLI TX| \n
  **** v1    0.1 CLI TX|     sub vcl_recv {\n
  **** v1    0.1 CLI TX|         return(lookup);\n
  **** v1    0.1 CLI TX|     }\n
  **** v1    0.1 CLI TX| \n
  **** v1    0.1 CLI TX| %XJEIFLH|)Xspa8P\n
  ***  v1    0.2 CLI RX  200
  **** v1    0.2 CLI RX| VCL compiled.
  **** v1    0.2 CLI TX| vcl.use vcl1
  ***  v1    0.2 CLI RX  200
  **   v1    0.2 Start
  **** v1    0.2 CLI TX| start
  ***  v1    0.2 debug| child (14787) Started\n
  **** v1    0.2 vsl|     0 WorkThread   - 0x7fc9fd2efa90 start
  **** v1    0.2 vsl|     0 CLI          - Rd vcl.load "vcl1" ./vcl.mHMVYeG3.so
  **** v1    0.2 vsl|     0 CLI          - Wr 200 36 Loaded "./vcl.mHMVYeG3.so" as "vcl1"
  ***  v1    0.2 CLI RX  200
  ***  v1    0.2 wait-running
  **** v1    0.2 CLI TX| status
  ***  v1    0.2 debug| Child (14787) said Child starts\n
  ***  v1    0.2 debug| Child (14787) said SMF.s0 mmap'ed 10485760 bytes of 10485760\n
  **** v1    0.2 vsl|     0 CLI          - Rd vcl.use "vcl1"
  **** v1    0.2 vsl|     0 CLI          - Wr 200 0
  **** v1    0.2 vsl|     0 CLI          - Rd start
  **** v1    0.2 vsl|     0 Debug        - Acceptor is epoll
  **** v1    0.2 vsl|     0 CLI          - Wr 200 0
  **** v1    0.2 vsl|     0 WorkThread   - 0x7fc9f7af7a90 start
  **** v1    0.3 vsl|     0 WorkThread   - 0x7fc9f70f6a90 start
  **** v1    0.3 vsl|     0 WorkThread   - 0x7fc9f66f5a90 start
  **** v1    0.3 vsl|     0 WorkThread   - 0x7fc9f5cf4a90 start
  **** v1    0.3 vsl|     0 WorkThread   - 0x7fc9f52f3a90 start
  **** v1    0.3 vsl|     0 WorkThread   - 0x7fc9f48f2a90 start
  **** v1    0.3 vsl|     0 WorkThread   - 0x7fc9f3ef1a90 start
  **** v1    0.3 vsl|     0 WorkThread   - 0x7fc9f34f0a90 start
  **** v1    0.3 vsl|     0 WorkThread   - 0x7fc9f2aefa90 start
  ***  v1    0.3 CLI RX  200
  **** v1    0.3 CLI RX| Child in state running
  **** v1    0.3 CLI TX| debug.xid 1000
  ***  v1    0.3 CLI RX  200
  **** v1    0.3 CLI RX| XID is 1000
  **** v1    0.3 CLI TX| debug.listen_address
  **** v1    0.3 vsl|     0 CLI          - Rd debug.xid 1000
  **** v1    0.3 vsl|     0 CLI          - Wr 200 11 XID is 1000
  ***  v1    0.4 CLI RX  200
  **** v1    0.4 CLI RX| 127.0.0.1 54787\n
  **   v1    0.4 Listen on 127.0.0.1 54787
  **** v1    0.4 macro def v1_addr=127.0.0.1
  **** v1    0.4 macro def v1_port=54787
  **** v1    0.4 macro def v1_sock=127.0.0.1 54787
  ***  top   0.4 client
  **   c1    0.4 Starting client
  **   c1    0.4 Waiting for client
  ***  c1    0.4 Connect to 127.0.0.1 54787
  ***  c1    0.4 connected fd 10 from 127.0.0.1 33613 to 127.0.0.1 54787
  ***  c1    0.4 txreq
  **** c1    0.4 txreq| GET / HTTP/1.1\r\n
  **** c1    0.4 txreq| \r\n
  ***  c1    0.4 rxresp
  ***  s1    0.4 accepted fd 4
  ***  s1    0.4 rxreq
  **** s1    0.4 rxhdr| GET / HTTP/1.1\r\n
  **** s1    0.4 rxhdr| X-Varnish: 1001\r\n
  **** s1    0.4 rxhdr| Accept-Encoding: gzip\r\n
  **** s1    0.4 rxhdr| Host: 127.0.0.1\r\n
  **** s1    0.4 rxhdr| \r\n
  **** s1    0.4 http[ 0] | GET
  **** s1    0.4 http[ 1] | /
  **** s1    0.4 http[ 2] | HTTP/1.1
  **** s1    0.4 http[ 3] | X-Varnish: 1001
  **** s1    0.4 http[ 4] | Accept-Encoding: gzip
  **** s1    0.4 http[ 5] | Host: 127.0.0.1
  **** s1    0.4 bodylen = 0
  ***  s1    0.4 expect
  **** s1    0.4 EXPECT req.url (/) == / (/) match
  ***  s1    0.4 txresp
  **** s1    0.4 txresp| HTTP/1.1 200 Ok\r\n
  **** s1    0.4 txresp| Content-Length: 3\r\n
  **** s1    0.4 txresp| \r\n
  **** s1    0.4 txresp| .\n
  **** s1    0.4 txresp| .
  ***  s1    0.4 shutting fd 4
  **   s1    0.4 Ending
  **** c1    0.4 rxhdr| HTTP/1.1 200 Ok\r\n
  **** c1    0.4 rxhdr| Content-Length: 3\r\n
  **** c1    0.4 rxhdr| Accept-Ranges: bytes\r\n
  **** c1    0.4 rxhdr| Date: Mon, 29 Apr 2013 17:01:24 GMT\r\n
  **** c1    0.4 rxhdr| X-Varnish: 1001\r\n
  **** c1    0.4 rxhdr| Age: 0\r\n
  **** c1    0.4 rxhdr| Via: 1.1 varnish\r\n
  **** c1    0.4 rxhdr| Connection: keep-alive\r\n
  **** c1    0.4 rxhdr| \r\n
  **** c1    0.4 http[ 0] | HTTP/1.1
  **** c1    0.4 http[ 1] | 200
  **** c1    0.4 http[ 2] | Ok
  **** c1    0.4 http[ 3] | Content-Length: 3
  **** c1    0.4 http[ 4] | Accept-Ranges: bytes
  **** c1    0.4 http[ 5] | Date: Mon, 29 Apr 2013 17:01:24 GMT
  **** c1    0.4 http[ 6] | X-Varnish: 1001
  **** c1    0.4 http[ 7] | Age: 0
  **** c1    0.4 http[ 8] | Via: 1.1 varnish
  **** c1    0.4 http[ 9] | Connection: keep-alive
  **** c1    0.4 body| .\n
  **** c1    0.4 body| .
  **** c1    0.4 bodylen = 3
  ***  c1    0.4 expect
  **** c1    0.4 EXPECT resp.status (200) == 200 (200) match
  ***  c1    0.4 closing fd 10
  **   c1    0.4 Ending
  *    top   0.4 RESETTING after test.vtc
  **   s1    0.4 Waiting for server
  **** s1    0.4 macro undef s1_addr
  **** s1    0.4 macro undef s1_port
  **** s1    0.4 macro undef s1_sock
  **** v1    0.4 macro undef v1_addr
  **** v1    0.4 macro undef v1_port
  **** v1    0.4 macro undef v1_sock
  **   v1    0.4 Stop
  **** v1    0.4 CLI TX| stop
  **** v1    0.4 vsl|     0 CLI          - Rd debug.listen_address
  **** v1    0.4 vsl|     0 CLI          - Wr 200 16 127.0.0.1 54787

  **** v1    0.4 vsl|    11 SessionOpen  c 127.0.0.1 33613 127.0.0.1:0
  **** v1    0.4 vsl|    11 ReqStart     c 127.0.0.1 33613 1001
  **** v1    0.4 vsl|    11 RxRequest    c GET
  **** v1    0.4 vsl|    11 RxURL        c /
  **** v1    0.4 vsl|    11 RxProtocol   c HTTP/1.1
  **** v1    0.4 vsl|    11 VCL_call     c recv
  **** v1    0.4 vsl|    11 VCL_return   c lookup
  **** v1    0.4 vsl|    11 VCL_call     c hash
  **** v1    0.4 vsl|    11 Hash         c /
  **** v1    0.4 vsl|    11 Hash         c 127.0.0.1
  **** v1    0.4 vsl|    11 VCL_return   c hash
  **** v1    0.4 vsl|    11 VCL_call     c miss
  **** v1    0.4 vsl|    11 VCL_return   c fetch
  **** v1    0.4 vsl|    13 BackendOpen  b s1 127.0.0.1 46014 127.0.0.1 52740
  **** v1    0.4 vsl|    11 Backend      c 13 s1 s1
  **** v1    0.4 vsl|    13 TxRequest    b GET
  **** v1    0.4 vsl|    13 TxURL        b /
  **** v1    0.4 vsl|    13 TxProtocol   b HTTP/1.1
  **** v1    0.4 vsl|    13 TxHeader     b X-Varnish: 1001
  **** v1    0.4 vsl|    13 TxHeader     b Accept-Encoding: gzip
  **** v1    0.4 vsl|    13 TxHeader     b Host: 127.0.0.1
  **** v1    0.4 vsl|    13 RxProtocol   b HTTP/1.1
  **** v1    0.4 vsl|    13 RxStatus     b 200
  **** v1    0.4 vsl|    13 RxResponse   b Ok
  **** v1    0.4 vsl|    13 RxHeader     b Content-Length: 3
  **** v1    0.4 vsl|    11 TTL          c 1001 RFC 120 -1 -1 1367254884 0 0 0 0
  **** v1    0.4 vsl|    11 VCL_call     c fetch
  **** v1    0.4 vsl|    11 VCL_return   c deliver
  **** v1    0.4 vsl|    11 ObjProtocol  c HTTP/1.1
  **** v1    0.4 vsl|    11 ObjResponse  c Ok
  **** v1    0.4 vsl|    13 Fetch_Body   b 4(length) cls 0 mklen 1
  **** v1    0.4 vsl|    13 Length       b 3
  **** v1    0.4 vsl|    13 BackendReuse b s1
  **** v1    0.4 vsl|    11 VCL_call     c deliver
  **** v1    0.4 vsl|    11 VCL_return   c deliver
  **** v1    0.4 vsl|    11 TxProtocol   c HTTP/1.1
  **** v1    0.4 vsl|    11 TxStatus     c 200
  **** v1    0.4 vsl|    11 TxResponse   c Ok
  **** v1    0.4 vsl|    11 TxHeader     c Content-Length: 3
  **** v1    0.4 vsl|    11 TxHeader     c Accept-Ranges: bytes
  **** v1    0.4 vsl|    11 TxHeader     c Date: Mon, 29 Apr 2013 17:01:24 GMT
  **** v1    0.4 vsl|    11 TxHeader     c X-Varnish: 1001
  **** v1    0.4 vsl|    11 TxHeader     c Age: 0
  **** v1    0.4 vsl|    11 TxHeader     c Via: 1.1 varnish
  **** v1    0.4 vsl|    11 TxHeader     c Connection: keep-alive
  **** v1    0.4 vsl|    11 Length       c 3
  **** v1    0.4 vsl|    11 ReqEnd       c 1001 1367254884.356311321 1367254884.356886864 0.000077486 0.000503778 0.000071764
  **** v1    0.4 vsl|    11 SessionClose c EOF
  **** v1    0.4 vsl|    11 StatSess     c 127.0.0.1 33613 0 1 1 0 0 1 164 3
  ***  v1    0.4 debug| Stopping Child\n
  ***  v1    0.4 CLI RX  200
  **** v1    0.4 CLI TX| status
  ***  v1    0.4 debug| Child (14787) said Child dies\n
  ***  v1    0.4 debug| Child (14787) died status=1\n
  ***  v1    0.4 debug| Child cleanup complete\n
  **** v1    0.4 vsl|     0 CLI          - EOF on CLI connection, worker stops
  ***  v1    0.4 CLI RX  200
  **** v1    0.4 CLI RX| Child in state stopped
  **   v1    0.4 Wait
  **   v1    0.4 R 14774 Status: 0000
  *    top   0.5 TEST test.vtc completed
  
  #     top  TEST test.vtc passed (0.471)


Re-formatted log(python vtctrans.py test.vtc -v)
---------------------------------------------------
::

  <<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<<
  test.vtc
  ----------------------------------------------------------------------
  Test start
    | top | macro def | varnishd=varnishd
    | top | macro def | pwd=/root/git/vtctrans
    | top | macro def | topbuild=/root/git/vtctrans/../..
    | top | macro def | bad_ip=10.255.255.255
    | top | macro def | tmpdir=/tmp/vtc.14812.346c7e27
    | top | TEST      | test.vtc starting
    | top |           | varnishtest
    | top | TEST      | example
    | top |           | server
    | top |           | server
  ----------------------------------------------------------------------
  Starting server s1
    | s1  |           | Starting server
    | s1  | macro def | s1_addr=127.0.0.1
    | s1  | macro def | s1_port=48998
    | s1  | macro def | s1_sock=127.0.0.1 48998
    | s1  |           | Listen on 127.0.0.1 48998
    | top |           | varnish
  ----------------------------------------------------------------------
  Started server s1
    | s1 |  | Started on 127.0.0.1 48998
  ----------------------------------------------------------------------
  Launch varnish v1
    | v1 |                      | Launch
    | v1 |                      | CMD: cd ${pwd} && ${varnishd} -d -d -n /tmp/vtc.14812.346c7e27/v1 -l 10m,1m,- -p auto_restart=off -p syslog_cli_tr a ffic=off -a '127.0.0.1:0' -S /tmp/vtc.14812.346c7e27/v1/_S -M '127.0.0.1 35000' -P /tmp/vtc.14812.346c7e27/v1/varnishd.pid -sfile,/tmp/vtc.14 812 .346c7e27/v1,10M
    | v1 |                      | CMD: cd /root/git/vtctrans && varnishd -d -d -n /tmp/vtc.14812.346c7e27/v1 -l 10m,1m,- -p auto_restart=off -p sysl o g_cli_traffic=off -a '127.0.0.1:0' -S /tmp/vtc.14812.346c7e27/v1/_S -M '127.0.0.1 35000' -P /tmp/vtc.14812.346c7e27/v1/varnishd.pid -sfile,/t mp/ vtc.14812.346c7e27/v1,10M
    | v1 |                      | PID: 14818
    | v1 | debug                |  Platform: Linux,2.6.32-71.18.1.el6.x86_64,x86_64,-sfile,-smalloc,-hcritbit\n
    | v1 | debug                |  200 251     \n
    | v1 | debug                |  -----------------------------\n
    | v1 | debug                |  Varnish Cache CLI 1.0\n
    | v1 | debug                |  -----------------------------\n
    | v1 | debug                |  Linux,2.6.32-71.18.1.el6.x86_64,x86_64,-sfile,-smalloc,-hcritbit\n
    | v1 | debug                |  \n
    | v1 | debug                |  Type 'help' for command list.\n
    | v1 | debug                |  Type 'quit' to close CLI session.\n
    | v1 | debug                |  Type 'start' to launch worker process.\n
    | v1 | debug                |  \n
    | v1 |                      | CLIPOLL 1 0x1 0x0
    | v1 |                      | CLI connection fd = 9
    | v1 | CLI:v1 <- v1(Result) |  107
    | v1 | CLI:v1 <- v1         |  vcxramevbwtbbazlsbyaucxqbxiewmit\n
    | v1 | CLI:v1 <- v1         |  \n
    | v1 | CLI:v1 <- v1         |  Authentication required.\n
    | v1 | CLI:v1 -> v1         |  auth d35c73d03bdb5a81b0a0b49a712534d8d79e0b83f40d8b328043af20375e79e6\n
    | v1 | CLI:v1 <- v1(Result) |  200
    | v1 | CLI:v1 <- v1         |  -----------------------------\n
    | v1 | CLI:v1 <- v1         |  Varnish Cache CLI 1.0\n
    | v1 | CLI:v1 <- v1         |  -----------------------------\n
    | v1 | CLI:v1 <- v1         |  Linux,2.6.32-71.18.1.el6.x86_64,x86_64,-sfile,-smalloc,-hcritbit\n
    | v1 | CLI:v1 <- v1         |  \n
    | v1 | CLI:v1 <- v1         |  Type 'help' for command list.\n
    | v1 | CLI:v1 <- v1         |  Type 'quit' to close CLI session.\n
    | v1 | CLI:v1 <- v1         |  Type 'start' to launch worker process.\n
    | v1 | CLI:v1 -> v1         |  vcl.inline vcl1 << %XJEIFLH|)Xspa8P\n
    | v1 | CLI:v1 -> v1         |  backend s1 { .host = "127.0.0.1"; .port = "48998"; }\n
    | v1 | CLI:v1 -> v1         |  \n
    | v1 | CLI:v1 -> v1         |  \n
    | v1 | CLI:v1 -> v1         |      sub vcl_recv {\n
    | v1 | CLI:v1 -> v1         |          return(lookup);\n
    | v1 | CLI:v1 -> v1         |      }\n
    | v1 | CLI:v1 -> v1         |  \n
    | v1 | CLI:v1 -> v1         |  %XJEIFLH|)Xspa8P\n
    | v1 | CLI:v1 <- v1(Result) |  200
    | v1 | CLI:v1 <- v1         |  VCL compiled.
    | v1 | CLI:v1 -> v1         |  vcl.use vcl1
    | v1 | CLI:v1 <- v1(Result) |  200
  ----------------------------------------------------------------------
  Start child process v1
    | v1 |                      | Start
    | v1 | CLI:v1 -> v1         |  start
    | v1 | debug                |  child (14833) Started\n
    | v1 | vsl                  |      0 WorkThread   - 0x7f16582efa90 start
    | v1 | vsl                  |      0 CLI          - Rd vcl.load "vcl1" ./vcl.Y4IKMy1w.so
    | v1 | vsl                  |      0 CLI          - Wr 200 36 Loaded "./vcl.Y4IKMy1w.so" as "vcl1"
    | v1 | vsl                  |      0 CLI          - Rd vcl.use "vcl1"
    | v1 | vsl                  |      0 CLI          - Wr 200 0
    | v1 | vsl                  |      0 CLI          - Rd start
    | v1 | vsl                  |      0 Debug        - Acceptor is epoll
    | v1 | vsl                  |      0 CLI          - Wr 200 0
    | v1 | CLI:v1 <- v1(Result) |  200
  ----------------------------------------------------------------------
  Wait running v1
    | v1  |                      | wait-running
    | v1  | CLI:v1 -> v1         |  status
    | v1  | debug                |  Child (14833) said Child starts\n
    | v1  | debug                |  Child (14833) said SMF.s0 mmap'ed 10485760 bytes of 10485760\n
    | v1  | vsl                  |      0 WorkThread   - 0x7f1652af7a90 start
    | v1  | vsl                  |      0 WorkThread   - 0x7f16520f6a90 start
    | v1  | vsl                  |      0 WorkThread   - 0x7f16516f5a90 start
    | v1  | vsl                  |      0 WorkThread   - 0x7f1650cf4a90 start
    | v1  | vsl                  |      0 WorkThread   - 0x7f16502f3a90 start
    | v1  | vsl                  |      0 WorkThread   - 0x7f164f8f2a90 start
    | v1  | vsl                  |      0 WorkThread   - 0x7f164eef1a90 start
    | v1  | vsl                  |      0 WorkThread   - 0x7f164e4f0a90 start
    | v1  | vsl                  |      0 WorkThread   - 0x7f164daefa90 start
    | v1  | CLI:v1 <- v1(Result) |  200
    | v1  | CLI:v1 <- v1         |  Child in state running
    | v1  | CLI:v1 -> v1         |  debug.xid 1000
    | v1  | CLI:v1 <- v1(Result) |  200
    | v1  | CLI:v1 <- v1         |  XID is 1000
    | v1  | CLI:v1 -> v1         |  debug.listen_address
    | v1  | vsl                  |      0 CLI          - Rd debug.xid 1000
    | v1  | vsl                  |      0 CLI          - Wr 200 11 XID is 1000
    | v1  | CLI:v1 <- v1(Result) |  200
    | v1  | CLI:v1 <- v1         |  127.0.0.1 39623\n
    | v1  |                      | Listen on 127.0.0.1 39623
    | v1  | macro def            | v1_addr=127.0.0.1
    | v1  | macro def            | v1_port=39623
    | v1  | macro def            | v1_sock=127.0.0.1 39623
    | top |                      | client
  ----------------------------------------------------------------------
  Starting client c1
    | c1 |  | Starting client
    | c1 |  | Waiting for client
  ----------------------------------------------------------------------
  Connecting c1 -> todo(write sock)
    | c1 |  | Connect to 127.0.0.1 39623
  ----------------------------------------------------------------------
  Send Request c1 -> todo(write sock)
    | c1 |                | connected fd 10 from 127.0.0.1 40888 to 127.0.0.1 39623
    | c1 |                | txreq
    | c1 | txreq:c1 -> v1 |  GET / HTTP/1.1\r\n
    | c1 | txreq:c1 -> v1 |  \r\n
  ----------------------------------------------------------------------
  Return response c1
    | c1 |  | rxresp
  ----------------------------------------------------------------------
  Accepted Request s1 <- todo(write sock)
    | s1 |           | accepted fd 4
    | s1 |           | rxreq
    | s1 | rxhdr     |  GET / HTTP/1.1\r\n
    | s1 | rxhdr     |  X-Varnish: 1001\r\n
    | s1 | rxhdr     |  Accept-Encoding: gzip\r\n
    | s1 | rxhdr     |  Host: 127.0.0.1\r\n
    | s1 | rxhdr     |  \r\n
    | s1 | http[ 0]  |  GET
    | s1 | http[ 1]  |  /
    | s1 | http[ 2]  |  HTTP/1.1
    | s1 | http[ 3]  |  X-Varnish: 1001
    | s1 | http[ 4]  |  Accept-Encoding: gzip
    | s1 | http[ 5]  |  Host: 127.0.0.1
    | s1 | bodylen   | 0
    | s1 |           | expect
    | s1 | EXPECT    | req.url (/) == / (/) match
    | s1 |           | txresp
    | s1 | txresp    |  HTTP/1.1 200 Ok\r\n
    | s1 | txresp    |  Content-Length: 3\r\n
    | s1 | txresp    |  \r\n
    | s1 | txresp    |  .\n
    | s1 | txresp    |  .
    | s1 |           | shutting fd 4
  ----------------------------------------------------------------------
  End server s1
    | s1 |                | Ending
    | c1 | rxhdr:c1 <- v1 |  HTTP/1.1 200 Ok\r\n
    | c1 | rxhdr:c1 <- v1 |  Content-Length: 3\r\n
    | c1 | rxhdr:c1 <- v1 |  Accept-Ranges: bytes\r\n
    | c1 | rxhdr:c1 <- v1 |  Date: Mon, 29 Apr 2013 17:03:12 GMT\r\n
    | c1 | rxhdr:c1 <- v1 |  X-Varnish: 1001\r\n
    | c1 | rxhdr:c1 <- v1 |  Age: 0\r\n
    | c1 | rxhdr:c1 <- v1 |  Via: 1.1 varnish\r\n
    | c1 | rxhdr:c1 <- v1 |  Connection: keep-alive\r\n
    | c1 | rxhdr:c1 <- v1 |  \r\n
    | c1 | http[ 0]       |  HTTP/1.1
    | c1 | http[ 1]       |  200
    | c1 | http[ 2]       |  Ok
    | c1 | http[ 3]       |  Content-Length: 3
    | c1 | http[ 4]       |  Accept-Ranges: bytes
    | c1 | http[ 5]       |  Date: Mon, 29 Apr 2013 17:03:12 GMT
    | c1 | http[ 6]       |  X-Varnish: 1001
    | c1 | http[ 7]       |  Age: 0
    | c1 | http[ 8]       |  Via: 1.1 varnish
    | c1 | http[ 9]       |  Connection: keep-alive
    | c1 | body           |  .\n
    | c1 | body           |  .
    | c1 | bodylen        | 3
    | c1 |                | expect
    | c1 | EXPECT         | resp.status (200) == 200 (200) match
    | c1 |                | closing fd 10
  ----------------------------------------------------------------------
  End client c1
    | c1  |             | Ending
    | top |             | RESETTING after test.vtc
    | s1  |             | Waiting for server
    | s1  | macro undef | s1_addr
    | s1  | macro undef | s1_port
    | s1  | macro undef | s1_sock
    | v1  | macro undef | v1_addr
    | v1  | macro undef | v1_port
    | v1  | macro undef | v1_sock
    | v1  |             | Stop
  ----------------------------------------------------------------------
  Stop varnish v1
    | v1 | CLI:v1 -> v1 |  stop
    | v1 | vsl          |      0 CLI          - Rd debug.listen_address
    | v1 | vsl          |      0 CLI          - Wr 200 16 127.0.0.1 39623
    | v1 | vsl          |     11 SessionOpen  c 127.0.0.1 40888 127.0.0.1:0
    | v1 | vsl          |     11 ReqStart     c 127.0.0.1 40888 1001
    | v1 | vsl          |     11 RxRequest    c GET
    | v1 | vsl          |     11 RxURL        c /
    | v1 | vsl          |     11 RxProtocol   c HTTP/1.1
    | v1 | vsl          |     11 VCL_call     c recv
    | v1 | vsl          |     11 VCL_return   c lookup
    | v1 | vsl          |     11 VCL_call     c hash
    | v1 | vsl          |     11 Hash         c /
    | v1 | vsl          |     11 Hash         c 127.0.0.1
    | v1 | vsl          |     11 VCL_return   c hash
    | v1 | vsl          |     11 VCL_call     c miss
    | v1 | vsl          |     11 VCL_return   c fetch
    | v1 | vsl          |     13 BackendOpen  b s1 127.0.0.1 51103 127.0.0.1 48998
    | v1 | vsl          |     11 Backend      c 13 s1 s1
    | v1 | vsl          |     13 TxRequest    b GET
    | v1 | vsl          |     13 TxURL        b /
    | v1 | vsl          |     13 TxProtocol   b HTTP/1.1
    | v1 | vsl          |     13 TxHeader     b X-Varnish: 1001
    | v1 | vsl          |     13 TxHeader     b Accept-Encoding: gzip
    | v1 | vsl          |     13 TxHeader     b Host: 127.0.0.1
    | v1 | vsl          |     13 RxProtocol   b HTTP/1.1
    | v1 | vsl          |     13 RxStatus     b 200
    | v1 | vsl          |     13 RxResponse   b Ok
    | v1 | vsl          |     13 RxHeader     b Content-Length: 3
    | v1 | vsl          |     11 TTL          c 1001 RFC 120 -1 -1 1367254993 0 0 0 0
    | v1 | vsl          |     11 VCL_call     c fetch
    | v1 | vsl          |     11 VCL_return   c deliver
    | v1 | vsl          |     11 ObjProtocol  c HTTP/1.1
    | v1 | vsl          |     11 ObjResponse  c Ok
    | v1 | vsl          |     13 Fetch_Body   b 4(length) cls 0 mklen 1
    | v1 | vsl          |     13 Length       b 3
    | v1 | vsl          |     13 BackendReuse b s1
    | v1 | vsl          |     11 VCL_call     c deliver
    | v1 | vsl          |     11 VCL_return   c deliver
    | v1 | vsl          |     11 TxProtocol   c HTTP/1.1
    | v1 | vsl          |     11 TxStatus     c 200
    | v1 | vsl          |     11 TxResponse   c Ok
    | v1 | vsl          |     11 TxHeader     c Content-Length: 3
    | v1 | vsl          |     11 TxHeader     c Accept-Ranges: bytes
    | v1 | vsl          |     11 TxHeader     c Date: Mon, 29 Apr 2013 17:03:12 GMT
    | v1 | vsl          |     11 TxHeader     c X-Varnish: 1001
    | v1 | vsl          |     11 TxHeader     c Age: 0
    | v1 | vsl          |     11 TxHeader     c Via: 1.1 varnish
    | v1 | vsl          |     11 TxHeader     c Connection: keep-alive
    | v1 | vsl          |     11 Length       c 3
    | v1 | vsl          |     11 ReqEnd       c 1001 1367254992.908947945 1367254992.909488678 0.000076771 0.000500917 0.000039816
    | v1 | vsl          |     11 SessionClose c EOF
    | v1 | vsl          |     11 StatSess     c 127.0.0.1 40888 0 1 1 0 0 1 164 3
  ----------------------------------------------------------------------
  Stop varnish child process v1
    | v1  | debug                |  Stopping Child\n
    | v1  | CLI:v1 <- v1(Result) |  200
    | v1  | CLI:v1 -> v1         |  status
    | v1  | debug                |  Child (14833) said Child dies\n
    | v1  | debug                |  Child (14833) died status=1\n
    | v1  | debug                |  Child cleanup complete\n
    | v1  | vsl                  |      0 CLI          - EOF on CLI connection, worker stops
    | v1  | CLI:v1 <- v1(Result) |  200
    | v1  | CLI:v1 <- v1         |  Child in state stopped
    | v1  |                      | Wait
    | v1  |                      | R 14818 Status: 0000
    | top | TEST                 | test.vtc completed
    | top | TEST                 | test.vtc passed
  ######################################################################
  Macro list
  ----------------------------------------------------------------------
  [key]     |  [value]
  ----------+-----------------------------------------------------------
  varnishd  |  varnishd
  s1_port   |  48998
  s1_addr   |  127.0.0.1
  v1_port   |  39623
  v1_addr   |  127.0.0.1
  s1_sock   |  127.0.0.1 48998
  bad_ip    |  10.255.255.255
  pwd       |  /root/git/vtctrans
  topbuild  |  /root/git/vtctrans/../..
  v1_sock   |  127.0.0.1 39623
  tmpdir    |  /tmp/vtc.14812.346c7e27

  ######################################################################
  Expect list
  ----------------------------------------------------------------------
  [compornent] | [result]     | [data]
  ----------------------------------------------------------------------
  s1           | result       | match
               |              |
               | HTTP:header  | GET
               | HTTP:header  | /
               | HTTP:header  | HTTP/1.1
               | HTTP:header  | X-Varnish: 1001
               | HTTP:header  | Accept-Encoding: gzip
               | HTTP:header  | Host: 127.0.0.1
               | HTTP:bodylen | 0
               | expr         | req.url == /
               | expr(val)    | / == /
  ----------------------------------------------------------------------
  c1           | result       | match
               |              |
               | HTTP:header  | HTTP/1.1
               | HTTP:header  | 200
               | HTTP:header  | Ok
               | HTTP:header  | Content-Length: 3
               | HTTP:header  | Accept-Ranges: bytes
               | HTTP:header  | Date: Mon, 29 Apr 2013 17:03:12 GMT
               | HTTP:header  | X-Varnish: 1001
               | HTTP:header  | Age: 0
               | HTTP:header  | Via: 1.1 varnish
               | HTTP:header  | Connection: keep-alive
               | HTTP:body    | .\n
               | HTTP:body    | .
               | HTTP:bodylen | 3
               | expr         | resp.status == 200
               | expr(val)    | 200 == 200
  ----------------------------------------------------------------------

  ######################################################################
  VTC result
    | passed | test.vtc
  ----------------------------------------------------------------------
  >>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>>

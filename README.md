# Home-AssistantConfig

change dns for github.com

cat /etc/hosts
~~~
127.0.0.1	localhost
::1		localhost ip6-localhost ip6-loopback
ff02::1		ip6-allnodes
ff02::2		ip6-allrouters

127.0.1.1		raspberrypi
185.199.108.133 raw.githubusercontent.com
140.82.114.4 github.com
~~~

service networking restart

before
~~~
ping github.com
PING github.com (20.205.243.166) 56(84) bytes of data.
~~~

after

~~~
ping github.com
PING github.com (140.82.114.4) 56(84) bytes of data.
64 bytes from github.com (140.82.114.4): icmp_seq=1 ttl=44 time=232 ms
64 bytes from github.com (140.82.114.4): icmp_seq=2 ttl=44 time=231 ms
~~~



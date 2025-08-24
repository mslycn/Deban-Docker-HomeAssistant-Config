# Home-AssistantConfig

local：/data  # on debain 12.9 via vmware on windows10

remote：https://github.com/mslycn/Deban-Docker-HomeAssistant-Config.git

## Enable Raspberry ssh client  root Login
~~~
PermitRootLogin yes

/etc/ssh/sshd_config
~~~
detail:https://blog.matterxiaomi.com/blog/raspberry-pi-ssh-server-part1/


## change dns for github.com

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

git
~~~
cd /data
git add .
git commit -m "all"
git push -u origin main
~~~
https://github.com/mslycn/Deban-Docker-HomeAssistant-Config


esphome

~~~
http://192.168.2.138:6052/
esphome
esphome
~~~



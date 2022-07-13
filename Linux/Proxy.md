# Use Git with SSH over Proxy
Put this in `~/.ssh/config`. [ref](https://adangel.org/2020/10/15/github-behind-proxy/)
```
Host github.com
	Hostname ssh.github.com
	Port 443
	ProxyCommand nc -X connect -x 192.168.x.y:8080 %h %p
```

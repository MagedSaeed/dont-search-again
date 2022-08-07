To clear the cache of `memcached` framework:

- Through netcat `nc`:
```bash
echo 'flush_all' | nc localhost 11211
# or
echo 'flush_all' | netcat localhost 11211
```
- Through telnet:
```bash
telnet localhost 11211
flush_all
quit
```
## More:
- https://serverfault.com/questions/259114/how-to-restart-clear-memcache-without-restarting-the-whole-web-server
- https://www.cyberciti.biz/faq/linux-unix-flush-contents-of-memcached-instance/

Add this to every container/pod:

```yaml
postStart:
  exec:
    command:
    - /bin/sh
    - -c 
    - "/bin/echo 'options single-request-reopen' >> /etc/resolv.conf"
```

```
single-request-reopen (since glibc 2.9)
  Sets RES_SNGLKUPREOP in _res.options.  The resolver
  uses the same socket for the A and AAAA requests.  Some
  hardware mistakenly sends back only one reply.  When
  that happens the client system will sit and wait for
  the second reply.  Turning this option on changes this
  behavior so that if two requests from the same port are
  not handled correctly it will close the socket and open
  a new one before sending the second request.
```
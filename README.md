# collectd-plugin-timesync

collectd plugin

# Behavior

1. Request send to NTP host(ex: 169.254.169.123, time.google.com, ...)
2. Retrive offset
3. Put offset to collectd

# Usage

```
  -host string
        destination host (default "169.254.169.123")
  -identifier string
        collectd identifier. first tier is replaced to hostname. (default "babatoshiakinoMacBook-Air.local/time/offset")
  -interval int
        interval(sec) (default 60)
```

# Example

```
LoadPlugin exec
<Plugin exec>
  Exec ubuntu "/usr/local/bin/collectd-plugin-timesync"
</Plugin>
```

# Install

1. Download and extract release artifacts
2. `chmod +x /path/to/collectd-plugin-timesync`
3. `mv /path/to/collectd-plugin-timesync /usr/local/bin/.`
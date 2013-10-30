# XAPI Braindump

XAPI plugin to generate arbitrary amount of data on request.

This is useful for testing database update request limits from slaves to pool
masters.

## Usage
Upload this plugin to your XenServer host and use the CLI to call the host
plugin:

```bash
[user@local ~]$ git clone https://github.com/simonjbeaumont/xapi-braindump
[user@local ~]$ scp xapi-braindump/braindump root@xs-host:/etc/xapi.d/plugins
[user@local ~]$ ssh root@xs-host
[root@xs-host ~]# xe host-call-plugin host-uuid=<host-uuid> plugin=braindump args:brain-size=<size-in-bytes> 
```

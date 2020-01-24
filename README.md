
## Copying down Splunk dashboards

- `jump entsec-spsh-00p-waz1.sys.comcast.net`
- `sudo tar cfvz file.tgz \ 
	-C /opt/splunk/etc/apps/SDA_Access_Level/local/data/ui/views .`
- `exit`
- `alias jumpscp='scp -o '\''ProxyCommand ssh -qx svcAutobahn@jump.autobahn.comcast.com -W %h:%p'\'''`
- `jumpscp entsec-spsh-00p-waz1.sys.comcast.net:file.tgz .`
- `mkdir dashbaords`
- `tar xfvz file.tgz -C dashboards`
- `rm file.tgz`
- `git commit -m "commit message" .`
- `git push origin`




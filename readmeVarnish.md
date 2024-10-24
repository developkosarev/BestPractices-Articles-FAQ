
```bash
#https://ma.ttias.be/reload-varnish-vcl-without-losing-cache-data/
#VARNISH_0 = /etc/init.d/varnish reload

# if you want to reload varnish without losing current cache you can
#VARNISH_1 = sudo varnishadm vcl.load vcl_some_name /etc/varnish/default.vcl
#VARNISH_2 = sudo varnishadm vcl.use vcl_some_nma

#to back to previous vcl:
#VARNISH_3 = sudo varnishadm vcl.list 
#VARNISH_4 = sudo varnishadm vcl.use vcl_choosen_name


@echo "$(call format,varnishtop,'Varnish [varnishtop]')"
@echo "$(call format,varnishhist,'Varnish [varnishhist]')"
@echo "$(call format,varnishstat,'Varnish [varnishstat]')"
@echo "$(call format,varnishadm,'Varnish param show [varnishadm param.show]')"
```

How to change Varnish config
https://www.varnish-software.com/developers/tutorials/configuring-varnish-systemd-services/

```bash
sudo systemctl edit varnish.service
cat /lib/systemd/system/varnish.service
Editing /etc/systemd/system/varnish.service.d/override.conf
```

```bash
dev@magento2-varnish:~$ cat /etc/systemd/system/varnish.service.d/override.conf
[Service]
ExecStart=
ExecStart=/usr/sbin/varnishd \
          -F \
          -a :6081 \
          -T localhost:6082 \
          -p feature=+http2 \
          -f /etc/varnish/default.vcl \
          -s malloc,16g \
          -p http_max_hdr=4096 \
          -p http_resp_hdr_len=1M \
          -p http_req_hdr_len=32k \
          -p http_req_size=64k \
          -p http_resp_size=1M \
          -p workspace_backend=2M \
          -p workspace_client=2M \
          -p workspace_thread=6k
```

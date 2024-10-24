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

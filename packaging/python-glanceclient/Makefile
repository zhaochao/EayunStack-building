srpm_repo = http://192.168.2.65:11080/pulp/repos/rdo/openstack-juno/epel-7
base_srpm = python-glanceclient-0.15.0-1.el7.centos.src.rpm
spec_file = python-glanceclient.spec

sources:
	mv $(spec_file) $(spec_file).new
	wget "$(srpm_repo)/$(base_srpm)" && \
	rpm2cpio $(base_srpm) | cpio -idmv && \
	rm -f $(spec_file) && \
	mv $(spec_file).new $(spec_file) && \
	rm -f $(base_srpm)

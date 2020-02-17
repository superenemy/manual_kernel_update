# manual_kernel_update
Kernel update. Create custom box for Vagrant Clound. Packer.

During performing the homework I've used the manual https://github.com/dmitry-lyutenko/manual_kernel_update/blob/master/manual/manual.md

But I faced some problem with commands in manual and I changed them to commands that wirked fine.

For example, I've changed command:

	curl https://releases.hashicorp.com/packer/1.4.4/packer_1.4.4_linux_amd64.zip | \
	sudo gzip -d > /usr/local/bin/packer && \
	sudo chmod +x /usr/local/bin/packer
to command:

	curl https://releases.hashicorp.com/packer/1.4.4/packer_1.4.4_linux_amd64.zip | \
	sudo ungzip packer_1.4.4_linux_amd64.zip -d /usr/local/bin/packer && \
	sudo chmod +x /usr/local/bin/packer
	
Any other commads worked fine and I successufully fullfild them. 

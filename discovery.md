note: clicking "Learn more about Supervisor Management" in vcenter supervisor managment displays a blank page. reference url: https://techdocs.broadcom.com/bin/gethidpage?ux-context-string=WCP-LEARN-MORE&appid=vsphere-9-0&language=en&format=rendered

# create a webserver to host supervisor files
Broadcom public url for supervisor files: https://wp-content.broadcom.com/supervisor/v1/latest/

# create a content library for supervisor images
use the webserver created previously

# Issue NSX Active/Active
On step 5 Workload Network the default NSX project is populated. you need to select a vpc connectivity provile, but the default one does not populate and is not an option. this is because the Default VPC Connectivity Profile has Default Outbound NAT set to off when it needs to be on. You cannot turn it on in an active/active setup, you must use active/standby
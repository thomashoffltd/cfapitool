# cfapitool

```	This tool is for creating/updating/deleting/showing DNS records in cloudflare.
	
	Credentials can be stored by creating ~/.cfapitoolcreds with the these variables:
	apikey_str=2dcfffaff0ff9ff7cf7ffffff1ffff5fffafd
	email_str="example@example.com"

	Created by thomashoffltd@gmail.com

	Usage: cfapitool [--apikey APIKEY_STR] [--email EMAIL_STR] [--domain DOMAIN_STR]
			 [--type TYPE_STR] [--name NAME_STR] [--CONTENT CONTENT_STR] [--ttl TTL_STR] 
			 [--priority PRIORITY_STR] [--proxied PROXIED_STR] 
			 [--create | --delete | --update | --show] 
			 [--verbose]

	Arguments:
	-h, --help			show this help message and exit
	-a, --apikey APIKEY_STR		specify Cloudflare apikey
	-e, --email EMAIL_STR		specify email address
	-d, --domain DOMAIN_STR		specify domain
	-t, --type TYPE_STR		specify DNS record type.
						default: A
						valid values: A, AAAA, CNAME, TXT, SRV, LOC, MX, NS, SPF read only
	-n, --name NAME_STR		specify DNS record name. 
						default: "example.com"
						max length: 255
	-c, --content CONTENT_STR	specify DNS record content. 
						default: "127.0.0.1"
	-T, --ttl TTL_STR			specify time to live for DNS record. 
						default: 120
						min value: 120
						max value: 2147483647
	-p, --priority	PRIORITY_STR	Used with some records like MX and SRV to determine priority.
						default: 0
						min value: 0
						max value: 65535
	-P, --proxied	PROXIED_STR	Whether the record is receiving the performance and security benefits of Cloudflare. 
						default: false
						valid values: (true,false)
	-C, --create			Create DNS record
	-D, --delete			Delete DNS record
	-U, --update			Update DNS record
	-S, --show			Show DNS record
	-v, --verbose			increase the verbosity of the bash script

	Example Usage:
	cfapitool --domain example.com -t A -n blah.example.com -c 192.168.252.128 -T 120 -p 0 -P false  -C -v -h

	This will create a DNS "A" record for "blah.example.com" with an IP address of "192.168.252.128". ```

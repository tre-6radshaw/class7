Class 7 EC2 Basics

Task -- building an Amazon Linux EC2 with a custom script

Template == https://github.com/MookieWAF/bmc4/blob/main/ec2scrpit

Steps:

	1. Create a Security Group
		a. Network & Security -> Security Groups -> Create Security Group
			i. Name Security Group
			ii. Copy Name to Description
			iii. Ignore VPC field
			iv. Inbound Rules
				1) Add Rule
				2) Type = HTTP
				3) Source = Anywhere-IPv4
			v. Outbound Rules
				1) …Keisha…
			vi. Tags are Optional
			vii. Create Security Group
	2. Build an Instance
		a. Name instance
		b. Application and OS Images (AMI)
			i. leave default
		c. Instance type
			i. leave default
		d. Key Pair (login)
			i. Create new key pair
			ii. Name it
			iii. Leave Key pair type default
			iv. Leave Private key file format default
			v. Create key pair
		e. Network settings
			i. Select existing security group
			ii. Select Security Group from Step 1
		f. Configure Storage
			i. Leave default
		g. Advanced details
			i. Scroll to bottom
			ii. User data - optional
				1) Select Choose file
				2) Upload 'startupscript.txt' file
		h. Select Launch instance
	3. Copy public DNS, make it into a useable link, paste link to chat
		a. Make sure to type http:// instead of https:// before any links are made
	4. Teardown Instructions
		a. Instances
			i. Check the box of the running instance
			ii. Select Instance State
				1) Terminate (Delete Instance) 
					a) Terminate(delete)
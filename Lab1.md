 
# CREATING AN AMAZON EBS-BACKED WINDOWS AMI  #



## Launching an Instance


1. Open the Amazon EC2 console.

![](https://cloud.githubusercontent.com/assets/13194331/8731165/3ddd4146-2c13-11e5-992b-326fd8e82664.png)



2. In the navigation bar at the top of the screen, the current region is displayed. Select the region for the instance.  

![](https://cloud.githubusercontent.com/assets/13194331/8731167/3de50908-2c13-11e5-98dd-d329d5102113.png)




3. From the Amazon EC2 console dashboard, click Launch Instance.

![](https://cloud.githubusercontent.com/assets/13194331/8731166/3de1e0f2-2c13-11e5-8ca8-fa34fa69fe34.png)



4. On the Choose an Amazon Machine Image (AMI) page, choose an AMI.

![](https://cloud.githubusercontent.com/assets/13194331/8731169/3e1309ac-2c13-11e5-80f3-71872ae6e741.png)

![](https://cloud.githubusercontent.com/assets/13194331/8731170/3e197850-2c13-11e5-8336-6eeb8f1e713a.png)



5. On the Choose an Instance Type page, select the hardware configuration and size of the instance to launch. Eligible for the free tier, select the t2.micro instance type. 
Note --> Set up an instance quickly for testing purposes, you can click Review and Launch at this point to accept default configuration settings, and launch your instance. 

To configure your instance further, click Next: Configure Instance Details.

![](https://github.com/krlLashini/ESBII-IT12024582/commit/4fdbc65b046e8a70335cf1072a15f2bc0cc813f9)



6. On the Configure Instance Details page, change the settings as necessary and then click Next. ( Here I have selected the default configuration settings )

![](https://cloud.githubusercontent.com/assets/13194331/8731173/3e3bd756-2c13-11e5-8f81-5ae50e3ec1d4.png)



7. On the Add Storage page, you can specify volumes to attach to the instance besides the volumes specified by the AMI (such as the root device volume) then click Next: Tag Instance when you have finished.

![](https://cloud.githubusercontent.com/assets/13194331/8731172/3e38e578-2c13-11e5-8633-8a67b6bc4154.png)



8. On the Configure Security Group page, use a security group to define firewall rules for your instance. These rules specify which incoming network traffic is delivered to your instance. All other traffic is ignored. Select or create a security group and then click Review and Launch.

Here I have selected create a new security group.

In Create a new security group the wizard automatically defines the launch-wizard-x security group.You can edit the name and description of the security group.

Here I have edited the name and the description as shown in the prints screen. 

The wizard automatically defines an inbound rule to allow to you connect to your instance over SSH (port 22) for Linux or RDP (port 3389) for Windows.

![](https://github.com/krlLashini/ESBII-IT12024582/commit/4fdbc65b046e8a70335cf1072a15f2bc0cc813f9)



9. On the Review Instance Launch page, check the details of your instance, and make any necessary changes by clicking the appropriate Edit link.When you are ready, click Launch.

![](https://cloud.githubusercontent.com/assets/13194331/8731175/3e426d0a-2c13-11e5-91d8-d33a9eb2cb72.png)



10. In the Select an existing key pair or create a new key pair dialog box, you can choose an existing key pair, or create a new one. Here I have created a new key pair.

To launch your instance, select the acknowledgment check box, then click Launch Instances.

Note --> If you select the Proceed without key pair option, you won't be able to connect to the instance unless you choose an AMI that is configured to allow users another way to log in.

![](https://cloud.githubusercontent.com/assets/13194331/8731177/3e680ae2-2c13-11e5-974d-7643d09a60c7.png)




11. Launch Instance.

![](https://cloud.githubusercontent.com/assets/13194331/8731178/3e6abc24-2c13-11e5-9226-6fa5c16775b2.png)

![](https://cloud.githubusercontent.com/assets/13194331/8731179/3e77272a-2c13-11e5-8ac4-c582fd8f4430.png)


## CONNECT TO THE INSTANCE AND CUSTOMIZE IT ##


**PREREQUISITES

Before you connect to your Linux instance using PuTTY, complete the following prerequisites:**



1. Install PuTTY
Download and install PuTTY

2. Get the ID of the instance
u can get the ID of your instance using the Amazon EC2 console

3. Get the public DNS name of the instance
You can get the public DNS for your instance using the Amazon EC2 console (check the Public DNS column; if this column is hidden, click the Show/Hide icon and select Public DNS)

4. Locate the private key
your IP address to your instance
You'll need the fully-qualified path of the .pem file for the key pair that you specified when you launched the instance.

5. Enable inbound SSH traffic from 


## CONVERTING YOUR PRIVATE KEY USING PUTTYGEN ##


1. Start PuTTYgen. Under Type of key to generate, select SSH-2 RSA.

![](https://cloud.githubusercontent.com/assets/13194331/8733106/79febc7a-2c1f-11e5-8ae3-8825bf5db428.png)


2. lick Load. By default, PuTTYgen displays only files with the extension .ppk. To locate your .pem file, select the option to display files of all types.Select your .pem file for the key pair that you specified when you launch your instance, and then click Open. Click OK to dismiss the confirmation dialog box.

![](https://cloud.githubusercontent.com/assets/13194331/8733107/7a044a00-2c1f-11e5-9c9c-df5a6b43f231.png)



3. Click Save private key to save the key in the format that PuTTY can use. PuTTYgen displays a warning about saving the key without a passphrase. Click Yes.

![](https://cloud.githubusercontent.com/assets/13194331/8733111/7a08e04c-2c1f-11e5-956b-1f21804e20a5.png)

![](https://cloud.githubusercontent.com/assets/13194331/8733110/7a0740ca-2c1f-11e5-9bb3-01a18db75e41.png)



4.  Specify the same name for the key that you used for the key pair (for example, my-key-pair). PuTTY automatically adds the .ppk file extension.

Your private key is now in the correct format for use with PuTTY. You can now connect to your instance using PuTTY's SSH client.

![](https://cloud.githubusercontent.com/assets/13194331/8733112/7a2b8ec6-2c1f-11e5-9b9c-ae81dd5b3320.png)



5. Start PuTTY 

![](https://cloud.githubusercontent.com/assets/13194331/8733113/7a3227e0-2c1f-11e5-8778-835f51105a19.png)



6. In the Category pane, select Session and complete fields.In the Host Name box, enter user_name@public_dns_name. Be sure to specify the appropriate user name for your AMI. Under Connection type, select SSH. Ensure that Port is 22.

![](https://cloud.githubusercontent.com/assets/13194331/8733114/7a33c6ae-2c1f-11e5-98ac-40d83a109a1d.png)



7. In the Category pane, expand Connection, expand SSH, and then select Auth. Complete the following:


Click Browse.

Select the .ppk file that you generated for your key pair, and then click Open.

![](https://cloud.githubusercontent.com/assets/13194331/8733115/7a34d04e-2c1f-11e5-9e70-d98ff0406eed.png)

If you plan to start this session again later, you can save the session information for future use. Select Session in the Category tree, enter a name for the session in Saved Sessions, and then click Save.Click Open to start the PuTTY session.

![](https://cloud.githubusercontent.com/assets/13194331/8733114/7a33c6ae-2c1f-11e5-98ac-40d83a109a1d.png)



# CREATING AN AMAZON EBS SNAPSHOT #


1. Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/. Choose Snapshots in the navigation pane

![](https://cloud.githubusercontent.com/assets/13194331/8733655/8771fd92-2c22-11e5-9c47-3c0278c6be63.png)


2. Choose Create Snapshot

![](https://cloud.githubusercontent.com/assets/13194331/8733657/8773532c-2c22-11e5-98cc-90f214e08c14.png)



3. In the Create Snapshot dialog box, select the volume to create a snapshot for, and then choose Create.

![](https://cloud.githubusercontent.com/assets/13194331/8733658/8774afc4-2c22-11e5-9a94-797d602a81f6.png)

![](https://cloud.githubusercontent.com/assets/13194331/8733656/87733072-2c22-11e5-9792-f01045246ac0.png)

![](https://cloud.githubusercontent.com/assets/13194331/8733749/1f38b170-2c23-11e5-9b29-c9142d4ab3e6.png)




1. In the navigation pane, click Instances and select your instance. Click Actions, select Image, and then click Create Image.
(note-->
If this option is disabled, your instance isn't an Amazon EBS-backed instance.)

![](https://cloud.githubusercontent.com/assets/13194331/8733965/6b4af5cc-2c24-11e5-843b-e4515f7edcaf.png)



2. In the Create Image dialog box, specify the following, and then click Create Image.



- A unique name for the image.
- A description of the image, up to 255 characters.
- By default, Amazon EC2 shuts down the instance, takes snapshots of any attached volumes, creates and registers the AMI, and then reboots the instance. Select No reboot if you don't want your instance to be shut down.
-  You can modify the root volume, Amazon EBS volumes, and instance store volumes

![](https://cloud.githubusercontent.com/assets/13194331/8733968/6b4d2d7e-2c24-11e5-87a5-f69ce2cc1cd7.png)



3. We can add new volume as shown in the print screen below

![](https://cloud.githubusercontent.com/assets/13194331/8733970/6b4daede-2c24-11e5-9113-3cc29ce3f48b.png)



4. Press create. 

![](https://cloud.githubusercontent.com/assets/13194331/8733966/6b4c33ba-2c24-11e5-9d95-3a69c49a86fb.png)





-  Click AMIs in the navigation pane to view the status of your AMI. While the new AMI is being created, its status is pending. This process typically takes a few minutes	to finish, and then the status of your AMI is available.

![](https://cloud.githubusercontent.com/assets/13194331/8733967/6b4c9d1e-2c24-11e5-9515-737b53389fc3.png)

![](https://cloud.githubusercontent.com/assets/13194331/8733969/6b4d425a-2c24-11e5-8686-8d343fdf68c5.png)



## CREATING AN AMI FROM A SNAPSHOT  ##


**If you have a snapshot of the root device volume of an instance, you can create an AMI from this snapshot using the AWS Management Console or the command line.**

**To create an AMI from a snapshot using the console**


1. Open the Amazon EC2 console at https://console.aws.amazon.com/ec2/.In the navigation pane, under Elastic Block Store, choose Snapshots.

![](https://cloud.githubusercontent.com/assets/13194331/8734344/10e9ca7e-2c27-11e5-8810-2d80af1d47bf.png)



2. Choose the snapshot, and then choose Create Image from the Actions list.

![](https://cloud.githubusercontent.com/assets/13194331/8734345/10ebb49c-2c27-11e5-8eb6-aa89a1c6460a.png)



3. In the Create Image from EBS Snapshot dialog box, complete the fields to create your AMI, then choose Create. If you're re-creating a parent instance, then choose the same options as the parent instance.

![](https://cloud.githubusercontent.com/assets/13194331/8734346/10ef4cec-2c27-11e5-9f9a-d83518c7b4a0.png)



4. Press Create

![](https://cloud.githubusercontent.com/assets/13194331/8734347/10efa3cc-2c27-11e5-8936-6c4a7e23dc2d.png)


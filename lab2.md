NAME 		: K.R.L.LASHINI

REG.NO 		: IT12024582

SUBJECT 	: ENTERPRISE STANDARDS AND BEST PRACTICES FOR 			  IT INFRASTRUCTURE

LAB			: 01

DATE		: 10.07.2015




# CREATE A BUCKET  #
**
To create a bucket**




1.Sign into the AWS Management Console and open the Amazon S3 console at https://console.aws.amazon.com/s3.Click Create Bucket. In the Create a Bucket dialog box, in the Bucket Name box, enter a bucket name.


![](https://cloud.githubusercontent.com/assets/13194331/8734967/3b613af4-2c2b-11e5-9e6b-448597f73567.png)


The bucket name you choose must be unique across all existing bucket names in Amazon S3.Bucket names must comply with certain rules. Example we can't use uppercase letters in bucket name. 

![](https://cloud.githubusercontent.com/assets/13194331/8734970/3b670664-2c2b-11e5-88b5-ca42e9492a39.png)


Note--> In the Region box, select a region. For this exercise, select Oregon from the drop-down list. 


2.Click Create.When Amazon S3 successfully creates your bucket, the console displays your empty bucket in the Buckets panel.

![](https://cloud.githubusercontent.com/assets/13194331/8734969/3b66550c-2c2b-11e5-9751-55e1c39f1401.png)






# ADD AN OBJECT TO A BUCKET  #

An object can be any kind of file: a text file, a photo, a video and so forth. When you add a file to Amazon S3, you have the option of including metadata with the file and setting permissions to control access to the file.


**To upload an object**

1.In the Amazon S3 console, click the name of bucket that you want to upload an object to and then click Upload. (note --> In the Upload - Select Files wizard, if you want to upload an entire folder, you must click Enable Enhanced Uploader to install the necessary Java applet. You only need to do this once per console session.) Click Add Files.A file selection dialog box opens:

![](https://cloud.githubusercontent.com/assets/13194331/8734972/3b81f78a-2c2b-11e5-8ccb-f0fc5a4ae97b.png)


![](https://cloud.githubusercontent.com/assets/13194331/8734973/3b8eb038-2c2b-11e5-8340-7848b8f37668.png)


2.Select the file that you want to upload and then click Open.

![](https://cloud.githubusercontent.com/assets/13194331/8734975/3b94347c-2c2b-11e5-99c9-00dbd9a00b37.png)


3.Click Start Upload.
You can watch the progress of the upload from within the Transfer panel.

![](https://cloud.githubusercontent.com/assets/13194331/8734974/3b9186dc-2c2b-11e5-8c19-17db925576bf.png)




# VIEW AN OBJECT #


You can open and view it in a browser. You can also download the object to your local computer.

**To open or download an object**


1.In the Amazon S3 console, in the Objects and Folders list, right-click the object or objects that you want to open or download, then click Open or Download as appropriate.


![](https://cloud.githubusercontent.com/assets/13194331/8734977/3b9eb820-2c2b-11e5-83a1-cd922190c101.png)


![](https://cloud.githubusercontent.com/assets/13194331/8734988/3bfd075e-2c2b-11e5-89a7-05f98b715002.png)


![](https://cloud.githubusercontent.com/assets/13194331/8734989/3c05f9d6-2c2b-11e5-8b46-bd1a2b28ad0c.png)


2.If you are downloading the object, specify where you want to save it. The procedure for saving the object depends on the browser and operating system that you are using.

![](https://cloud.githubusercontent.com/assets/13194331/8734990/3c13207a-2c2b-11e5-889b-a7ac7b603ae4.png)

![](https://cloud.githubusercontent.com/assets/13194331/8734991/3c238c44-2c2b-11e5-83bd-b3c22c5ae350.png)



Note --> By default, your Amazon S3 buckets and objects are private. To make an object viewable by using a URL.

![](https://cloud.githubusercontent.com/assets/13194331/8734984/3be029cc-2c2b-11e5-8cd9-421132e0a0db.png)




# EDITING OBJECT PERMISSIONS #


you must make the object publicly readable. Otherwise, you will need to create a signed URL that includes a signature with authentication information. 


1.Click the object whose permissions you want to change, and then click Permissions.

![](https://cloud.githubusercontent.com/assets/13194331/8734978/3bb23d1e-2c2b-11e5-8a6d-6bbf80741f68.png)


2.Click Add more permissions.
In the Grantee box of the new line that appears, add the name of the person or group for which you want to set permissions. The name can be the email address associated with an AWS account, a canonical ID, or one of the predefined Amazon S3 groups.Select or clear the check boxes, as appropriate, next to the permissions you want to grant or deny. lick the "x" on the line of the grantee that you want to remove. Then click Save.

![](https://cloud.githubusercontent.com/assets/13194331/8734979/3bc22b34-2c2b-11e5-8616-6969d4db5f6e.png) 




**To make an object accessible by everyone**

The console provides a shortcut for making objects accessible to everyone, meaning that everyone can both view and download the object.



1.Right-click the object that you want to make accessible, and then click Make Public.

![](https://cloud.githubusercontent.com/assets/13194331/8734982/3bc79966-2c2b-11e5-996a-b85a1fe7ce5a.png)


![](https://cloud.githubusercontent.com/assets/13194331/8734981/3bc71c98-2c2b-11e5-8851-132239f0dd23.png)


2.Click Permissions. The newly added grantee appears in the display.

![](https://cloud.githubusercontent.com/assets/13194331/8734983/3bd325e2-2c2b-11e5-964c-dee12dbd872a.png) 


3.Get the link for the object to share in the object properties pane as shown in the picture below.

![](https://cloud.githubusercontent.com/assets/13194331/8734984/3be029cc-2c2b-11e5-8cd9-421132e0a0db.png) 



# MOVE AN OBJECT #


you can move the object to a different bucket or folder.


1.In the Amazon S3 console, right-click the object that you want to move, and then click Cut. (note --> You can use the SHIFT and CTRL keys to select multiple objects and perform the same action on them simultaneously )

![](https://cloud.githubusercontent.com/assets/13194331/8734998/3c56acb4-2c2b-11e5-8cf7-8c8c60732892.png)


2.Navigate to the bucket or folder where you want to move the object. Right-click the folder or bucket and then click Paste Into.


![](https://cloud.githubusercontent.com/assets/13194331/8734992/3c288604-2c2b-11e5-8143-26f9c6082219.png) 


![](https://cloud.githubusercontent.com/assets/13194331/8734993/3c2baf5a-2c2b-11e5-9c05-c54eaff4cee0.png)




# EDITING OBJECT METADATA #

Each object in Amazon S3 has a set of key-value pairs that represents its metadata. There are two types of metadata:


- System metadata – Sometimes processed by Amazon S3, e.g., Content-Type, and Content-Length.



- User metadata – Never processed by Amazon S3.

User metadata is stored with the object and returned with it.The maximum size for user metadata is 2 KB, and both the keys and their values must conform to US-ASCII standards.


**To edit the metadata of an object**

1.Sign in to the AWS Management Console and open the Amazon S3 console at https://console.aws.amazon.com/s3/.
Click the object whose metadata you want to edit, and then click Metadata.

![](https://cloud.githubusercontent.com/assets/13194331/8734991/3c238c44-2c2b-11e5-83bd-b3c22c5ae350.png)

2.lick Add more metadata.
In the Key box, click one of the available keys, or type a new one, starting with x-amz-meta- (for example, x-amz-meta-<name>).In the corresponding Value box, click an entry in the list, if available, or type a value.  Then press save.

![](https://cloud.githubusercontent.com/assets/13194331/8734986/3bf4637e-2c2b-11e5-9ac2-84a6f1c7ce0d.png)


Note --> 

- User-defined metadata names must begin with "x-amz-meta-", otherwise Amazon S3 will not set the key value pair as you define it.


- Click the key-value pair that you want to remove.Click Remove selected metadata, or click the "x" on the line of the key-value pair that you want to remove.




# RENAMING AN OBJECT #


1.Sign in to the AWS Management Console and open the Amazon S3 console at https://console.aws.amazon.com/s3/.
Right-click the object that you want to rename, and then click Rename.


![](https://cloud.githubusercontent.com/assets/13194331/8734994/3c30c954-2c2b-11e5-8f74-bff2ad50eb31.png)



2.n the box for the name, type a new name, and then click the checkmark icon to the right of the box to submit the name change.

![](https://cloud.githubusercontent.com/assets/13194331/8734995/3c3568c4-2c2b-11e5-8ce2-8cf1fad54630.png) 




# DELETE AN OBJECT AND BUCKET #


If you no longer need to store the objects that you uploaded and moved, you should delete them to prevent further charges.

**To delete an object**

1.In the Amazon S3 console, in the Objects and Folders panel, right-click the object that you want to delete, and then click Delete.


![](https://cloud.githubusercontent.com/assets/13194331/8734996/3c428ef0-2c2b-11e5-83d1-72592f786a3e.png)


![](https://cloud.githubusercontent.com/assets/13194331/8734997/3c5119b6-2c2b-11e5-8685-5a8f2c779359.png)


Note --> To delete a bucket, you must first delete all of the objects in it. Right-click the bucket you want to delete, and then click Delete.When a confirmation message appears, click OK.


# AWS-IAM

<h1>AWS Identity and Access Management</h1>

<h2> Project Description</h2>
AWS-IAM is a web service for managing users and user permissions in AWS. This project will demonstrate inspecting IAM policies, adding users to groups with specific capabilities enabled, using the IAM sign-in URL and experimenting with the effects of policies on service access.
<br />


<h2>Project steps </h2>
The following tasks are performed:
<p align="left">
<h3>Accessing the AWS Management Console</h3> 
Connecting to the AWS Management Console is the first step of this process. The following image shows the AWS management console panel after logging into AWS account: <br/> <br />
<img src="https://imgur.com/RxFYVX5.png" height="80%" width="80%" alt="IAM first step"/>
<br />
<br />
 <h3>Exploring Users and groups</h3> 
This task involves exploring the users and groups. Here 3 users and 3 groups have been created. Note that no user has any permissions. Below is a summary page of all the users : <br/><br/>
<img src="https://imgur.com/Mp3SDWh.png" height="80%" width="80%" alt="file permission steps"/>
<br />
<br />
here is a summary page of all the groups created:<br/><br/>
<img src="https://imgur.com/Mp3SDWh.png" height="80%" width="80%" alt="file permission steps"/>
<br />
<br />
  
  <h3>Business scenario</h3> 
A company is growing its use of AWS and has new users that we need to access the servces depending upon their job function. <br/><br/>
 - <b>user-1:</b> Group: S3-Support <br/>Permissions: Read-Only 
 access to Amazon S3<br/><br/> 
  - <b>user-2:</b> Group: EC2-Support <br/>Permissions: Read-Only 
 access to Amazon EC2<br/><br/> 
  - <b>user-3:</b> Group: EC2-Admin <br/>Permissions: View, start and Stop amazon EC2 instances<br/>

To achieve the above requirements, we have a number of tasks to do:
                  
   - <b>Add users to Groups:</b> user-1, user-2 and user-3 are added and assigned to their respective groups. Permissions are also added during this task. When one of these characters is a hyphen (-) instead, it indicates that this permission is not granted to the user.<br/>
   - <b>Sign in and test users'permissions:</b> In this task, the persmissions of each IAM user is tested.<br/>
 <img src="https://imgur.com/Mp3SDWh.png" height="80%" width="80%" alt="file permission steps"/>
<br />
<br />
  <h3>Change file permissions on a hidden file</h3> 
The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. I know .project_x.txt is a hidden file because it starts with a period (.). In this example, I removed write permissions from the user and group, and added read permissions to the group. I removed write permissions from the user with u-w. Then, I removed write permissions from the group with g-w, and added read permissions to the group with g+r.   <br/> <br />
<img src="https://imgur.com/T1lyFlQ.png" height="80%" width="80%" alt="file permission steps"/>
<br />
<br />
<h3>Change  directory permissions</h3> 
The first two lines of the screenshot display the commands I entered, and the other lines display the output of the second command. I previously determined that the group had execute permissions, so I used the chmod command to remove them. The researcher2 user already had execute permissions, so they did not need to be added.  <br/> <br />
<img src="https://imgur.com/S7RMgbN.png" height="80%" width="80%" alt="file permission steps"/>
<br />
<br />



<h2>Summary of the project </h2>

The first step in this was using ls -la to check the permissions for the directory. This informed my decisions in the following steps. I then used the chmod command multiple times to change the permissions on files and directories.

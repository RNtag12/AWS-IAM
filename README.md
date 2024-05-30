# AWS-IAM

<h1>AWS Identity and Access Management(IAM)</h1>

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
<img src="https://imgur.com/SHax6sw.png" height="80%" width="80%" alt="users"/> 
<br />
<br />

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
                  
   - <b>Add users to Groups:</b> user-1, user-2 and user-3 are added and assigned to their respective groups. Permissions are also added during this task.<br/>
-Adding user-1 to S3-support<br/>
<img src="https://imgur.com/evvgRmC.png" height="80%" width="80%" alt="user1"/>
<br />
<img src="https://imgur.com/Ew3FdwD.png" height="80%" width="80%" alt="user1"/>
<br /><br />

-Adding user-2 to EC2-Support group <br/>
<img src="https://imgur.com/pYpztRg.png" height="80%" width="80%" alt="user2"/>
<br />
<img src="https://imgur.com/1ZUoAnA.png" height="80%" width="80%" alt="user2"/>
<br /><br />
-Adding user-3 to EC2-Admin group <br/>
<img src="https://imgur.com/9GtlrTa.png" height="80%" width="80%" alt="user3"/>
<br />
<img src="https://imgur.com/3xp8JMT.png" height="80%" width="80%" alt="user3"/>
<br /><br />

   - <b>Sign in and test users'permissions:</b> In this task, the persmissions of each IAM user is tested.<br/><br/>
 -For user-1, we first verified if they had accesss to S3 services. The ouput shows that user-1 has access to S3 services<br/>
<img src="https://imgur.com/JhQRUEu.png" height="80%" width="80%" alt="user1"/>
<br />
Then we tried to access EC2 instances. The results show that user-1 does not have required permissions to access EC2 instances. The reason is that user-1 was assigned to a group that only has access to S3 services
<img src="https://imgur.com/BfK4SEV.png" height="80%" width="80%" alt="user1"/>
<br /><br />

-For user-2, we also verified if they had accesss to EC2 instances. The ouput shows that user-2 has access to EC2 instances since he can see a list of running instances<br/>
<img src="https://imgur.com/TdBCIfN.png" height="80%" width="80%" alt="user2"/>
<br /><br />
Although user-2 can access the EC2 instances, he cannot modify the state of the instances. Indeed, he has a read-only permission
<br />
<img src="https://imgur.com/hciQ2jR.png" height="80%" width="80%" alt="user2"/>
<br /><br />
Then we tried to access S3 buckets. The results show that he does not have permissions to list buckets. The reason is that user-2 was assigned to a group that only has access to EC2 instances.
<img src="https://imgur.com/zcZtJks.png" height="80%" width="80%" alt="user2"/>
<br /><br />
-For user-3, he has access to EC2 instances and can modify the state of the instances  <br/>
<img src="https://imgur.com/QhfRsDR.png" height="80%" width="80%" alt="user3"/>
<br /><br />
We stopped the labhost instances .
<img src="https://imgur.com/WGdOOe3.png" height="80%" width="80%" alt="user3"/>
<br /><br />
<br />


<h2>Summary of the Project </h2>
This project serves as a practical exploration of some of the AWS-IAM functions. we first assigned each user to their respective groups then we checked their access to resources to ensure that they had the right permissions.

  




# 09 Deployment
Agenda dag 9 d. 30-10-2017

## Web Publish
You can publish your ASP.NET Core MVC sites to many hosts. The sort of "Default" is "Azura". The only problem with that is that you are never totally sure when or what you are going to pay for what you are doing.    

A good and free alternative is [AppHarbor](https://apphb.com)

#### Visual Studio
* Right click your solution and choose **publish**
* choose to publish to your file system
* in your git bash or terminal browse to the **bin\Release\PublishOutput** folder
* make it a local git repository ```` git init ````    

#### Deploy Application to AppHarbor
To deploy your first app, do the following:

1. Go to appharbor.com
1. Create an account
1. Go to appharbor.com/applications
1. Create an application
1. Get the AppHarbor respository URL from the box on the left
1. Add the remote repository like this ```` git remote add appharbor MY_REPOSITORY_URL ````   
1. Deploy using ```` git push appharbor master  ````   

#### Database publish
* appharbor.com/applications/NAME_OF_YOUR_APP
* add-ons
* in categories choose **Database**
* choose the free SQL server called **Yocto**
* When installed click **Go to SQL Server** link
* You will need the Hostname, username and password when you connect from Visual Studio

##### Visual Studio
* Open **SQL Server Object Explorer**
* Right click **SQL Server** and choose **Add SQL Server**
* Under Authendication choose ** SQL Server Authendication **
* copy and paste Hostname, username and password

###### ConnectionString
* Change the connectionstring in your **appsettings.json** file to the one you see on appharbor.



## View Models
This is based on the project we worked on earlier this semester. [StudentAdmin](https://github.com/ElectiveAspNet/09_studentAdmin).     

In order to show not only a Student or an Enrollment or a Course, but also all related data we need to use the navigation properties from our Entity Models.

We will do it together later but first you should give it a try.

###Entity Models vs View Models
Entity Models deals with how the tabels in the database should look like. ViewModels deals with the data shown in the views.

<img src="https://github.com/keacore/07_RepositoriesViewModels/blob/master/Materials/img/ViewModel.png" width="600">

### TASK
On the Students Details page you should be able to show the Enrollments of the student. It should look something like this:    

<img src="https://github.com/ElectiveAspNet/09_deployment/blob/master/img/Udklip_2.PNG" width="600">    

You will find these links helpful in solving the task:
* [Querying Data](https://docs.microsoft.com/en-us/ef/core/querying/)
* [Basic Queries](https://docs.microsoft.com/en-us/ef/core/querying/basic)
* [Loading Related Data](https://docs.microsoft.com/en-us/ef/core/querying/related-data)




# 09 Deployment
Agenda dag 9 d. 30-10-2017

## Web Publish
You can publish your ASP.NET Core MVC sites to many hosts. The sort of "Default" is "Azura". The only problem with that is that you are never totally sure when or what you are going to pay for what you are doing.    

A good and free alternative is [AppHarbor](https://apphb.com)

#### Visual Studio
* Right click your solution and choose **publish**
* choose to publish to your file system
* in you git bash or terminal browse to the **bin\Release\PublishOutput** folder
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



## View Models


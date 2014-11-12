Description:
=================
I am working on Leasing application for a Multinational Giant. The application Produces / Consumes several Web services. Most of the data in our application comes in XML format from another web service and will be displayed in the User Interface. Business Users always provides some changes to our Application and this needs to be achieved in shorter Time Periods. In this Scenario we will do Parallel development where Some Team members will work on Web Services changes and Some Team members will work on User Interface Changes. User Interface Cannot be tested until Web Services development/modifications completed.

In this situation MockServicesServer Comes to Rescue.

Software Requirements:
======================

To Work With Source Code Visual Studio 2010 is required
.NET Framework 4.0

Instructions:
=============

 - Open/Download the Source Code

 ![Step-1](https://github.com/sunilpottumuttu/MockServicesServer/blob/master/Docs/Step1.PNG)

 - Start the MockServicesServer.

 ![Step-2](https://github.com/sunilpottumuttu/MockServicesServer/blob/master/Docs/Step2.PNG) 

 - By Default the application start listening at port 3333.(The
    behaviour can be changed by changing app.config port value)
Edit the MockServices.xml

 - To Serve a Static Content for a given Request URL

<Handler Name="Scenario1" Description="" RequestUrl="http://staticurl.com"> <Response HandlerType="Static" FileName="one.xml" /> </Handler>

 - In Some scenarios you may need to modify the response for a request

<Handler Name="Scenario2" Description="" RequestUrl="www.codeproject.com"> <Response HandlerType="FromAssembly" FileName="MockServices.Server.Scenario2Test,MockServices.Server.Scenario2Test.CodeProjectBlocker" /> </Handler>

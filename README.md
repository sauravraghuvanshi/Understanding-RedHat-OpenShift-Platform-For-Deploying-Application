# Deploying and Managing apllication on Red Hat OpenShift.

## Introducing OpenShift Container Platform:

Red Hat OpenShift Container Platform is a self-service platform where development teams can deploy their applications. The platform integrates the tools to build and run applications, and manages the complete application life cycle from initial development to production.

OpenShift offers several deployment scenarios. One typical workflow starts when a developer provides the Git repository URL for an application to OpenShift.

The platform automatically retrieves the source code from Git, and then builds and deploys the application. The developer can also configure OpenShift to detect new Git commits, and then automatically rebuild and redeploy the application.
By automating the build and deployment processes, OpenShift allows developers to focus on application design and development. By rebuilding your application with every change you commit, OpenShift gives you immediate feedback. You can detect and fix errors early in the development process, before they become an issue in production.

OpenShift provides the building mechanisms, libraries, and runtime environments for the most popular languages, such as Java, Ruby, Python, PHP, .NET, Node.js, and many more. It also comes with a collection of additional services that you can directly use for your application, such as databases.

As traffic and load to your web application increases, OpenShift can rapidly provision and deploy new instances of the application components. For the Operations team, it provides additional tools for logging and monitoring.

## OpenShift Container Platform Architecture:
Red Hat OpenShift Online, at [here](https://www.openshift.com/), is a public OpenShift instance run by Red Hat. With that cloud platform, customers can directly deploy their applications online, without needing to install, manage, and update their own instance of the platform.

Red Hat also provides the Red Hat OpenShift Container Platform that companies can deploy on their own infrastructure. By deploying your own instance of OpenShift Container Platform, you can fine tune the cluster performance specific to your needs. In this classroom, you will be provided access to a private OpenShift cluster.

## Application Architecture:
Several development teams or customers usually share the same OpenShift platform. For security and isolation between projects and customers, OpenShift builds and runs applications in isolated containers. A container is a way to package an application with all its dependencies, such as runtime environments and libraries.


To manage the containerized applications, OpenShift adds a layer of abstraction known as the pod. Pods are the basic unit of work for OpenShift. A pod encapsulates a container, and other parameters, such as a unique IP address or storage. A pod can also group several related containers that share resources.

## Project-1: Deploying Applications to Red Hat OpenShift Container Platform:
In this exercise, I used the OpenShift web console to deploy a Node.js application.
**Outcomes**
we should be able to use the OpenShift web console to:
* Create a new project.
* Add a new application from a Git repository.
* Inspect the resources that OpenShift creates during build and deployment.
* To perform this exercise, ensure that the express-helloworld Node.js application is in your  GitHub DO101-app repository from the previous activity. Your changes should be in the devenv-versioning branch.
* Red Hat Training manages an OpenShift cluster dedicated to this course. Your Red Hat Training Online Learning environment provides access to this platform.

<img src="Images/1.png" width="1000">

## Steps:
### 1. Open a web browser and access the OpenShift web console. Log in and switch to the Developer perspective.

 * Open a web browser and navigate to https://console-openshift-console.apps.cluster.domain.example.com to access the OpenShift web console. Replace the URL with the value from your Red Hat Training Online Learning environment. The login page for the web console displays.
 * Log in with the user name and password from your Red Hat Training Online Learning environment.
  
 * From the list at the top of the menu on the left, select the Developer perspective.
 <img src="Images/2.png" width="1000">

### 2. Create a new project named youruser-deploy-app. Replace youruser with your user name.
* Use the Advanced → Projects menu and click Create Project.
* Enter youruser-deploy-app in the Name field. Replace youruser with your user name. Leave the other fields empty and click Create.

### 3. Create a new JavaScript Node.js application named helloworld. Use the code you pushed to the Git repository in the previous exercise. The code is in the express-helloworld subdirectory. The branch name is devenv-versioning.
* Click the Add tab on the left side of the page and then click From Catalog.
 <img src="Images/3.png" width="1000">

* Click Languages → JavaScript and then click the first option, Node.js. Click Create Application to enter the details of the application.
* Complete the form according to the following table. To access the Git parameters, click Show Advanced Git Options.
Table Shows New Application Parameters:

| Parameter     | Value         |
| ------------- | ------------- |
| Git Repo URL  | https://github.com/sauravraghuvanshi/Introduction-to-OpenShift-Application-by-RedHat |
| Git Reference | devenv-versioning |
| Context Dir | /express-helloworld |
| Application Name | helloworld |
| Name | helloworld |
| Create a route to the application | Make sure the box is checked |

### 4. Wait for OpenShift to build and deploy your application.
* The web console should automatically show the Topology page. If necessary, click the Topology tab on the left side of the page.
* Wait for the application icon to change to the build complete status.
<img src="Images/4.png" width="1000">

### 5. Review the application resources and confirm that you can access the application from the internet.
* Click the Node.js icon to access the application details.
* Click the Resources tab to list the resources that OpenShift created during the application deployment.
<img src="Images/5.png" width="1000">

* Click the Location link in the route resource. Your web browser opens a new tab and accesses the application public URL.
<img src="Images/6.png" width="1000">

# My application on OpenShift is created.


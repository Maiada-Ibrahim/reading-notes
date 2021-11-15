
# Android Fundamentals
To develop apps that take advantage of the Android operating system and UI, use the Android software development kit (SDK).

 The SDK includes software libraries of prewritten code, a debugger, a device emulator, documentation, sample code, and tutorials.

 To develop apps using the SDK, you use the Java programming language to develop the app and Extensible Markup Language (XML) files to describe data resources. By writing the code in Java and creating a single app binary.

Android SDK tools compile the code, data and resource files into 


 - Apk  (.apk)

  have the file we need in runtime it is the file that Android-powered devices use to install the app.

- an Android App Bundle(.aab)
have additional metadata that is not required at runtime so it is a publishing format and is not installable on Android devices

the Android app lives has  own security sandbox so  protected by operating system is a multi-user Linux system,each app a unique Linux user ID,Each process has its own virtual machine (VM)


# App components
- Activities	They dictate the UI and handle the user interaction to the smart phone screen
- Services	They handle background processing associated with an application.
- Broadcast Receivers	They handle communication between Android OS and applications.
- Content Providers	They handle data and database management issues.

![](https://i2.wp.com/techvidvan.com/tutorials/wp-content/uploads/sites/2/2021/06/Android_Application_Components.jpg?fit=1200%2C628&ssl=1)

# Activating components
three components are active (activities, services, and broadcast receivers) by an asynchronous message called an intentat run time An intent is created with an Intent object, which defines a message to activate either a specific component for activities and services component , an intent defines the action,for broadcast receivers the announcement being broadcast.
### we have three methods for activating 
- using by passing an Intent to startActivity() or startActivityForResult()
- JobScheduler class to schedule actions by passing an Intent to startService()
-  by passing an Intent to methods such as sendBroadcast(), sendOrderedBroadcast(), or sendStickyBroadcast().

# The manifest file

that use to know if the file is exists so reading the  AndroidManifest.xml. this do some thing Identifies any user permissions ,know the minimum API Level required,know , hardware and software features,Declares API libraries the app needs.


# App resources
One of the most important aspects of providing resources separate from your source code is the ability to provide alternative resources for different device configurations that mean easy to update various characteristics of your app without modifying code.
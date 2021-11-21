# Espresso
is an open source android user interface (UI) testing framework , Espresso is a simple, efficient and flexible testing framework.

- A part of the development lifecycle and  While it can be used for black-box testing, Espresso’s full power is unlocked .

## Synchronization capabilities
expresso test call onView() this do some action
- The message queue is empty.
- There are no instances of AsyncTask currently executing a task.
- All developer-defined idling resources are idle.
This capability gives you more reliable and dependable test results.



![](https://themodestack.com/wp-content/uploads/2018/11/Espresso-test-steps.png)
## Create UI tests with Espresso Test Recorder
the test will be for UI interactions include tap and type actions that a person may use to interact with your app
- Turn off animations on your test device
- Click Run > Record Espresso Test.
- In the Select Deployment Target window, choose the device on which you want to record the test
- the app must install and launch before Espresso Test Recorder allows you to interact with it and will try executing these actions in the same order.


## Add assertions to verify UI elements
we will check at view element text is ,exists, does not exist
- Click Add Assertion. A Screen Capture dialog appears while Espresso gets the UI hierarchy and other information about the current app state

- click on the element in the screenshot or use the first drop-down menu in the Edit assertion box at the bottom of the window.

- in the Edit assertion box select the assertion

- click Save Assertion

- Click Complete Recording then Pick a test class name for your test then  Click Save.
it will save  in src > androidTest > java > com.example.username.appname

## Run an Espresso test locally

- use the Project  window on the left side of the Android Studio IDE open app module and choose the test
- Right-click on the test and click Run ‘testName.’
- In the Select Deployment Target window, choose the device then Click OK.

Monitor the progress of your test in the Run window at the bottom of the IDE
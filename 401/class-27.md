
# Read: Class 27 Read: 27 - Intents, Activities, and SharedPreferences
## Tasks and the back stack
- A task is a collection of activities that users interact with when performing a certain job. The activities are arranged in a stack—the back stack—in the order in which each activity is opened. 
- Android Activities are the logical construct of the screens that we want a user to navigate through. The relation that each Activity holds with respect to other is very crucial for a good user experience.

## Lifecycle of a task and its back stack
![](https://developer.android.com/images/fundamentals/diagram_backstack.png)
-the activity pushed onto the stack when started by the current activity and popped off when the user leaves it using the Back button or gesture. As such, the back stack operates as a last in, first out object structure

### Back press behavior for root launcher activities
to provide custom back navigation we use AndroidX Activity APIs, or overriding onBackPressed()

The system moves the activity and its task to the background instead of finishing the activity
when press the home button the benifite of that resume your app from a warm state, instead of having to completely restart the app from a cold state.


### Multiple activity instances
- if we cane open the activity from different place   a new instance of that activity is created and pushed onto the stack (rather than bringing any previous instance of the activity to the top)
- if the user navigates backward using the Back button or gesture, each instance of the activity is revealed in the order they were opened (each with their own UI state)


# Managing Tasks
\<activity> manifest element in the intent that you pass to startActivity() has a principal attributes :


- taskAffinity
- launchMode
- allowTaskReparenting
- clearTaskOnLaunch
- alwaysRetainTaskState
- finishOnTaskLaunch

And it hase principal intent flags :

- FLAG_ACTIVITY_NEW_TASK
- FLAG_ACTIVITY_CLEAR_TOP
- FLAG_ACTIVITY_SINGLE_TOP

we use these manifest attributes and intent flags to define how activities are associated with tasks and how they behave in the back stack.

--------------------------------------------------

## Define launch modes using Intent flags
Launch modes allow you to define how a new instance of an activity is associated with the current task.
You can define different launch modes in two ways:

- Using the manifest file

When you declare an activity in your manifest file, you can specify how the activity should associate with tasks when it starts.

- Using Intent flags

When you call startActivity(), you can include a flag in the Intent that declares how (or whether) the new activity should associate with the current task.


## Handling affinities
An affinity indicates which task an activity prefers to belong to. By default, all the activities from the same app have an affinity for each other. So, by default, all activities in the same app prefer to be in the same task
we can change that using FLAG_ACTIVITY_NEW_TASK or  allowTaskReparenting attribute set to "true"


## Clear the back stack
he system clears the task of all activities except the root activity. When the user returns to the task again, only the root activity is restored that the default but we can change that using 
- alwaysRetainTaskState if true all activity is still and can retains 

- clearTaskOnLaunch if ture the task is cleared down to the root activity it's the opposite of alwaysRetainTaskState

- finishOnTaskLaunch
This attribute is like clearTaskOnLaunch, but it operates on a single activity, not an entire task.


## Save key-value data 
with small collection of key-values we use SharedPreferences APIs is object points to a file containing key-value pairs it allows us to store the data in the form of key-value pairs similar to a Map. Each SharedPreferences object reference a file, which contains the key-value pairs and provides methods to read and write them.
![](https://miro.medium.com/max/616/1*dYBUWGgnwJsf_iiX6yIhcg.png)
 getSharedPreferences()  for  multiple shared preference files identified by name

 getPreferences() for you need to use only one shared preference file for the activity.


 -  You can call this from any Context in your app.

 -  SharedPreferences.Editor editor = sharedPref.edit()  we use that to shared preferences


 - int highScore = sharedPref.getInt(getString(R.string.saved_high_score_key), defaultValue) we use that to read from SharedPreferences

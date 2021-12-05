# Read: 41 - Intent Filters

## Allowing Other Apps to Start Your Activity 
- if we want to  can share messages or photos then should support  ACTION_SEND intent so when click on share the app apear as option that need to you need to add an <intent-filter> element in your manifest file for the corresponding <activity> element.

- When your app is installed on a device, the system identifies your intent filters and adds the information to an internal catalog of intents supported by all installed apps  so when click on share the app apear as option


## Add an Intent Filter
criteria of the Intent object

- Action: A string naming the action to perform. Usually one of the platform-defined values such as ACTION_SEND or ACTION_VIEW

- Data : <data> A description of the data associated with the intent

- Category :<category> Provides an additional way to characterize the activity handling the intent

Each incoming intent specifies only one action and one data type, but it's OK to declare multiple instances of the <action>, <category>, and <data> elements in each <intent-filter>

If any two pairs of action and data are mutually exclusive in their behaviors, you should create separate intent filters to specify which actions are acceptable when paired with which data types

## Handle the Intent in Your Activity
we  call getIntent() to retrieve the Intent that started the activity. You can choose start from where but the better choose  early callbacks such as onCreate() or onStart()


# Return a Result

- call setResult() to specify the result code and result Intent. When your operation is done and the user should return to the original activity

 - call finish() to close (and destroy) your activity

- Generally, it's either RESULT_OK or RESULT_CANCELED. You can then provide additional data with an Intent
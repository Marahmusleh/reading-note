# Intent Filters
* Intent filter is a property that used in your app to allow other apps use a feature of your app.

* It is added in the manifest file if you want to use it

## Allowing Other Apps to Start Your Activity
* If your app can perform an action that might be useful from another app, your app should be prepared to respond to action requests by specifying the appropriate intent filter in your activity.

* To allow other apps to start your activity in this way, you need to add an <intent-filter> element in your manifest file for the corresponding <activity> element.

* When your app is installed on a device, the system identifies your intent filters and adds the information to an internal catalog of intents supported by all installed apps. When an app calls startActivity() or startActivityForResult(), with an implicit intent, the system finds which activity (or activities) can respond to the intent.

## Add an Intent Filter
* In order to properly define which intents your activity can handle, each intent filter you add should be as specific as possible in terms of the type of action and data the activity accepts.

* Action:A string naming the action to perform. Usually one of the platform-defined values such as ACTION_SEND or ACTION_VIEW.

* Data: A description of the data associated with the intent.

* Category: Provides an additional way to characterize the activity handling the intent, usually related to the user gesture or location from which it's started.

## Handle the Intent in Your Activity
* In order to decide what action to take in your activity, you can read the Intent that was used to start it.

* As your activity starts, call getIntent() to retrieve the Intent that started the activity. You can do so at any time during the lifecycle of the activity, but you should generally do so during early callbacks such as onCreate() or onStart().

## Return a Result
* If you want to return a result to the activity that invoked yours, simply call setResult() to specify the result code and result Intent. When your operation is done and the user should return to the original activity, call finish() to close (and destroy) your activity.
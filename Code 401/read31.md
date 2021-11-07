# Espresso
```
Use Espresso to write concise, beautiful, and reliable Android UI tests.

@Test
public void greeterSaysHello() {
    onView(withId(R.id.name_field)).perform(typeText("Steve"));
    onView(withId(R.id.greet_button)).perform(click());
    onView(withText("Hello Steve!")).check(matches(isDisplayed()));
}
```
Espresso tests run optimally fast! It lets you leave your waits, syncs, sleeps, and polls behind while it manipulates and asserts on the application UI when it is at rest.

### packages
* espresso-core - Contains core and basic View matchers, actions, and assertions. See Basics and Recipes.

* espresso-web - Contains resources for WebView support.

* espresso-idling-resource - Espresso's mechanism for synchronization with background jobs.

* espresso-contrib - External contributions that contain DatePicker, RecyclerView and Drawer actions, accessibility checks, and CountingIdlingResource.

* espresso-intents - Extension to validate and stub intents for hermetic testing.

* espresso-remote - Location of Espresso's multi-process functionality.

### 1. Record UI interactions:
To start recording a test with Espresso Test Recorder, proceed as follows:

* Click Run > Record Espresso Test.

* In the Select Deployment Target window, choose the device on which you want to record the test.

* Espresso Test Recorder triggers a build of your project, and the app must install and launch before Espresso Test Recorder allows you to interact with it. The Record Your Test window appears after the app launches, and since you have not interacted with the device yet, the main panel reads "No events recorded yet." Interact with your device to start logging events such as "tap" and "type" actions.

### 2. Add assertions to verify UI elements
Assertions verify the existence or contents of a View element through three main types:

* text is: Checks the text content of the selected View element.

* exists: Checks that the View element is present in the current View hierarchy visible on the screen.

* does not exist: Checks that the View element is not present in the current View hierarchy.

To add an assertion to your test, proceed as follows:

1. Click Add Assertion. A Screen Capture dialog appears while Espresso gets the UI hierarchy and other information about the current app state. The dialog closes automatically once Espresso has captured the screenshot.

2. A layout of the current screen appears in a panel on the right of the Record Your Test window. To select a View element on which to create an assertion, click on the element in the screenshot or use the first drop-down menu in the Edit assertion box at the bottom of the window. The selected View object is highlighted in a red box.

3. Select the assertion you want to use from the second drop-down menu in the Edit assertion box. Espresso populates the menu with valid assertions for the selected View element.

* If you choose the "text is" assertion, Espresso automatically inserts the text currently inside the selected View element. You can edit the text to match your desired assertion using the text field in the Edit assertion box.
4. Click Save and Add Another to create another assertion or click Save Assertion to close the assertion panels.

### Save a recording
Once you finish interacting with your app and adding assertions, use the following steps to save your recording and generate the Espresso test:

1. Click Complete Recording. The Pick a test class name for your test window appears.

2. Espresso Test Recorder gives your test a unique name within its package based on the name of the launched activity. Use the Test class name text field if you want to change the suggested name. Click Save.

3. Click Yes to automatically add the dependencies to your build.gradle file. The file automatically opens after Espresso Test Recorder generates it, and Android Studio shows the test class as selected in the Project window of the IDE.

### Run an Espresso test locally
To run an Espresso test, use the Project window on the left side of the Android Studio IDE:

1. Open the desired app module folder and navigate to the test you want to run. The test’s location depends on the location of your instrumentation test root and the package name of the launched activity.

2. Right-click on the test and click Run ‘testName.’ Alternatively, you can open the test file and right-click on the generated test class or method. Read more about how to run tests on the Test Your App page.

3. In the Select Deployment Target window, choose the device on which you want to run the test. If necessary, create a new Android Virtual Device. Click OK.
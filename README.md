
# Mapbook Android
This  is home to the mobile mapbook . Replace the paper maps you use for field work with offline maps. **Note:** this app is meant for tablets only and won't render properly on phone screens.


## Features
- Mobile map packages
- Feature layers
- Identify
- Table of Contents
- Show a legend
- Use a map view callout
- Geocode addresses
- Suggestion search
- Bookmarks
- Sign in to an ArcGIS account



```xml
<?xml version="1.0" encoding="utf-8"?>
<resources>

    <!-- TODO: add your own client id here-->
    <string name="client_id">YOUR_CLIENT_ID</string>

    <!-- This redirect URI is the default value for https://www.arcgis.com -->
    <string name="redirect_uri">my-ags-app://auth</string>

</resources>
```
* As part of the registration process, add a redirect uri for your app.  Navigate to the Redirect URIs section at the bottom of the registration page and set the redirect uri to `my-ags-app://auth`.  This redirect uri is the default redirect for `https://www.arcgis.com`.

![](Register2.png)
* Note that the scheme for the `DefaultOAuthIntentReceiver` in the Android Manifest file is derived from the redirect uri.
```xml
        <activity
            android:name="com.esri.arcgisruntime.security.DefaultOAuthIntentReceiver"
            android:label="OAuthIntentReceiver"
            android:launchMode="singleTask">
            <intent-filter>
                <action android:name="android.intent.action.VIEW"/>
                <category android:name="android.intent.category.DEFAULT"/>
                <category android:name="android.intent.category.BROWSABLE"/>

                <data android:scheme="my-ags-app"/>
            </intent-filter>
        </activity>
 ```



### Fork the repo
**Fork** the Mapbook for Android repo.

### Clone the repo
Once you have forked the repo, you can make a clone



### Configuring a Remote for a Fork


1. In the Terminal (for Mac users) or command prompt (fow Windows and Linux users) type ```git remote -v``` to list the current configured remote repo for your fork.
2.  to specify new remote upstream repository that will be synced with the fork. You can type ```git remote -v``` to verify the new upstream.

If there are changes made in the Original repository, you can sync the fork to keep it updated with upstream repository.

1. In the terminal, change the current working directory to your local project
2. Type ```git fetch upstream``` to fetch the commits from the upstream repository
3. ```git checkout master``` to checkout your fork's local master branch.
4. ```git merge upstream/master``` to sync your local `master' branch with `upstream/master`. **Note**: Your local changes will be retained and your fork's master branch will be in sync with the upstream repository.


## Testing With Robotium
The project includes a small suite of Robotium tests that test various features of the application.  The Robotium tests for the mapbook-app will run best on an attached device, rather than in the emulator.  Use the following steps to configure your environment for running the tests.  During some of the tests, screen shots are captured by Robotium and by default are stored in the /sdcard/Robotium-Screenshots/ directory on the device.  

1.  Attach a non-emulated Android device to your computer.
2.  Ensure location services are enabled on the Android device.
3.  Ensure you have internet connectivity on the Android device.
4.  Adjust the entries in your values/app_settings.xml.
5.  Right-click on the MapbookTest.java file in Android Studio and select Run 'MapbookTest'.



Find a bug or want to request a new feature enhancement? Let us know by submitting an issue.

#




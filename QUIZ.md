## ANDROID QUIZ

Sure, here's the revised version with each answer followed by a note explaining it:

#### Q1. To add features, components, and permissions to your Android app, which file needs to be edited?

- [x] AndroidManifest.xml
- [ ] Components.xml
- [ ] AppManifest.xml
- [ ] ComponentManifest.xml

> [!NOTE]
> The correct file to edit when adding features, components, and permissions to your Android app is the AndroidManifest.xml. This file contains essential information about your app and its components.

#### Q2. Which XML attribute should be used to make an Image View accessible?

- [ ] android:talkBack
- [ ] android:labelFor
- [ ] android:hint
- [x] android:contentDescription

>> [!NOTE] The `android:contentDescription` attribute should be used to provide a textual description of the image for accessibility purposes, aiding users who rely on screen readers.

#### Q3. You launch your app, and when you navigate to a new screen it crashes. Which action will NOT help you diagnose the issue?

- [ ] Set breakpoints and then step through the code line by line
- [ ] Use the profiler tools in Android Studio to detect anomalies in CPU and network usage.
- [x] Add a Thread.sleep() call before you start the new activity.
- [ ] Inspect the logs in Logcat.

>> [!NOTE] Adding a `Thread.sleep()` call before starting a new activity will not help diagnose the issue of a crashing app. It might introduce artificial delays but won't address the root cause of the crash.

#### Q4. Why might push notifications stop working?

- [x] all of these answers
- [ ] The device token is not being sent to push the provider correctly.
- [ ] Google Play Services is not installed on the device/emulator.
- [ ] Battery optimization is turned on on the device.

>> [!NOTE] Push notifications might stop working due to various reasons listed in the options, including issues with the device token, Google Play Services, and battery optimization.

#### Q5. What is the correct set of component classes needed to implement a RecyclerView of items that displays a list of widgets vertically?

- [ ] A

```java
    RecycleView
    RecyclerView.Adapter<T extends BaseAdapter>
    RecyclerView.ViewHolder<T extends BaseViewHolder>
    LinearLayoutManager
```

- [ ] B

```java
    RecycleView
    RecyclerView.Adapter
    RecyclerView.ViewHolder<T extends BaseViewHolder>
    LinearLayoutManager
```

- [ ] C

```java
    RecycleView
    RecyclerView.Adapter
    RecyclerView.ViewHolder
    LinearLayoutManager
```

- [x] D

```java
    RecycleView
    RecyclerView.Adapter<VH extends ViewHolder>
    RecyclerView.ViewHolder
    LinearLayoutManager
```

>> [!NOTE] The correct set of component classes needed for a RecyclerView includes `RecyclerView`, `RecyclerView.Adapter<VH extends ViewHolder>`, `RecyclerView.ViewHolder`, and `LinearLayoutManager`.

#### Q6. The Android system kills the process when it needs to free up memory. The likelihood of the system killing a given process depends on the state of the process and the activity at the time. With a combination of process and activity state is most likely to be killed?

- [x] Process: In the background; Activity: Is stopped
- [ ] Process: In the background; Activity: Is paused
- [ ] Process: In the foreground; Activity: Is started
- [ ] Process: In the foreground; Activity: Is paused

>> [!NOTE] When the process is in the background and the activity is stopped, it's more likely for the Android system to kill the process to free up memory.

#### Q7. You have created a NextActivity class that relies on a string containing some data that passes inside the intent. Which code snippet allows you to launch your activity?

- [ ] A

```java
    Intent(this, NextActivity::class.java).also { intent ->
        startActivity(intent)
    }
```

- [ ] B

```java
    Intent(this, NextActivity::class.java).apply {
        put(EXTRA_NEXT, "some data")
    }.also { intent ->
        activityStart(intent)
    }
```

- [x] C

```java
    Intent(this, NextActivity::class.java).apply {
        putExtra(EXTRA_NEXT, "some data")
    }.also { intent ->
        startActivity(intent)
    }
```

- [ ] D

```java
    Intent(this, NextActivity::class.java).apply {
        put(EXTRA_NEXT, "some data")
    }.also { intent ->
        activityStart(intent)
    }
```

>> [!NOTE] The correct way to launch an activity with intent containing data is to use `putExtra()` to add data to the intent before starting the activity using `startActivity(intent)`.

#### Q8. You want to include about and setting modules in your project. Which files accurately reflect their inclusion?

- [ ] `in build.gradle:include ':app',':about' ':settings'`
- [x] `in settings.gradle:include ':app',':about' ':settings'`
- [ ] `in settings.gradle:include ':about',':settings'`
- [ ] `in gradle.properties:include ':app',':about' ':settings'`

>> [!NOTE] To include modules in your project, you need to modify the `settings.gradle` file to list the modules to be included.

#### Q9. What is the benefit of using @VisibleForTesting annotation?

- [x] to denote that a class, method, or field has its visibility relaxed to make code testable
- [ ] to denote that a class, method, or field is visible only in the test code
- [ ] to denote that a class, method, or field has its visibility increased to make code less testable
- [ ] to throw a run-time error if a class, method, or field with this annotation is accessed improperly

>> [!NOTE] The `@VisibleForTesting` annotation is used to denote that a class, method, or field has its visibility relaxed to make the code testable. It's typically used in situations where you need to access normally private or package-private members for testing purposes.

#### Q10. How would you specify in your build.gradle file that your app required at least API level 21 to run, but it can be tested on API level 28?

- [ ] A

```
      defaultConfig {
        ...
        minApiVersion 21
        targetApiVersion 28
      }
```

- [ ] B

```
      defaultConfig {
        ...
        targetSdkVersion 21
        testSdkVersion 28
      }
```

- [ ] C

```
      defaultConfig {
        ...
        minSdkVersion 21
        testApiVersion 28
      }
```

- [x] D

```
      defaultConfig {
        ...
      minSdkVersion 21
        targetSdkVersion 28
      }
```

>> [!NOTE] To specify in the build.gradle file that your app requires at least API level 21 to run but can be tested on API level 28, you need to set `minSdkVersion` to 21 and `targetSdkVersion` to 28 in the `defaultConfig` block.

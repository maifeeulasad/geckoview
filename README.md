This GitHub repository contains the documentation for [GeckoView][8]. If you are looking for the code for GeckoView you can find it at [Mozilla Central][9].

If there is documentation that you feel is missing, or an existing document doesn't cover the aspect that you are looking for, please request it by [raising an issue][10].

If you have a GeckoView bug that you want to raise, please do so on our [Bugzilla][11].

## Get Started with GeckoView

* [GeckoView Quick Start Guide][1]
* [Interacting with Web content and WebExtension][7]


## API Documentation

* [Changelog][2]
* [API][12]

## Get Started as a Contributor

* [GeckoView Contributor Quick Start Guide][3]
* [Mozilla Central Quick Start Guide][4]
* [Mozilla Central Contributor Guide][5]
* [Guide to Native Debugging in Android Studio][6]


## More information
You can read more about GeckoView on the [wiki](https://wiki.mozilla.org/Mobile/GeckoView).


[1]:https://firefox-source-docs.mozilla.org/mobile/android/geckoview/consumer/geckoview-quick-start.html
[2]:https://geckoview.dev/javadoc/mozilla-central/org/mozilla/geckoview/doc-files/CHANGELOG
[3]:https://firefox-source-docs.mozilla.org/mobile/android/geckoview/contributor/geckoview-quick-start.html
[4]:https://firefox-source-docs.mozilla.org/mobile/android/geckoview/contributor/mc-quick-start.html
[5]:https://firefox-source-docs.mozilla.org/mobile/android/geckoview/contributor/contributing-to-mc.html
[6]:https://firefox-source-docs.mozilla.org/mobile/android/geckoview/contributor/native-debugging.html
[7]:https://firefox-source-docs.mozilla.org/mobile/android/geckoview/consumer/web-extensions.html
[8]:https://geckoview.dev
[9]:https://searchfox.org/mozilla-central/source/mobile/android/geckoview
[10]:https://github.com/mozilla/geckoview/issues
[11]:https://bugzilla.mozilla.org/enter_bug.cgi?product=GeckoView
[12]:https://geckoview.dev/javadoc/mozilla-central/index.html


# For quick usage :
```
//Add repository from mozilla
repositories {
    maven {
        url "https://maven.mozilla.org/maven2/"
    }
}
//Add compile options
compileOptions {
    sourceCompatibility JavaVersion.VERSION_1_8
    targetCompatibility JavaVersion.VERSION_1_8
}
//Add dependency
dependencies {
    // ...
  implementation "org.mozilla.geckoview:geckoview-${geckoviewChannel}:${geckoviewVersion}"
}
//In XML
<org.mozilla.geckoview.GeckoView
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:id="@+id/geckoview"
    android:layout_width="fill_parent"
    android:layout_height="fill_parent" />
//In Java import
import org.mozilla.geckoview.GeckoRuntime;
import org.mozilla.geckoview.GeckoSession;
import org.mozilla.geckoview.GeckoView;
GeckoView view = findViewById(R.id.geckoview);
GeckoSession session = new GeckoSession();
GeckoRuntime runtime = GeckoRuntime.create(this);
//In Java
session.open(runtime);
view.setSession(session);
session.loadUri("about:buildconfig"); // Or any other URL...
```

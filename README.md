[![ForTheBadge built-with-love](http://ForTheBadge.com/images/badges/built-with-love.svg)](https://GitHub.com/Naereen/)
[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-green.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity)
[![Open Source Love svg1](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/)
[![GitHub license](https://img.shields.io/github/license/Naereen/StrapDown.js.svg)](https://github.com/Naereen/StrapDown.js/blob/master/LICENSE)
[![](https://jitpack.io/v/wise4rmgod/AdnetwrokManager.svg)](https://jitpack.io/#wise4rmgod/AdnetwrokManager)
# AdnetwrokManager
A Simple Android library to check various types of network connections (WIFI,INTERNET), to allow an android app to check internet connectivity status in realtime.

# Prerequisite
* Androidx
* Kotlin

![Alt Text](https://res.cloudinary.com/wise4rmgod/image/upload/v1585409145/ezgif.com-video-to-gif.gif)
 

# How to set up
And add a dependency code to your module's build.gradle file.
```
dependencies {
	        implementation 'com.github.wise4rmgod:AdnetwrokManager:0.1.0'
	}

```
Add below codes to your root build.gradle file (not your module build.gradle file).
```
	allprojects {
		repositories {
			...
			maven { url 'https://jitpack.io' }
		}
	}
```

## Permissions

Add the neccesary permissions in the manifest file

```

<uses-permission android:name="android.permission.ACCESS_NETWORK_STATE"/>

<uses-permission android:name="android.permission.INTERNET"/>

```
## Example

```kotlin

import com.dev.adnetworkm.CheckNetworkStatus
import com.example.refressh_networkconnection.utils.NetworkUtil
import kotlinx.android.synthetic.main.activity_main.*

class MainActivity : AppCompatActivity() {

    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContentView(R.layout.activity_main)

        CheckNetworkStatus.getNetworkLiveData(applicationContext).observe(this, Observer { t ->
            when (t) {
                true -> {
                    // TODO: Handle the connection...
                }
                false -> {
                   // TODO: Handle the connection...
                }
                null -> {
                    // TODO: Handle the connection...
                }
            }
        })
    }



}


```
## Contributions and Issues
feel free to open an issue if any or contribute to it, its an open source library.

## Licence
MIT License

## Author
nwokocha Wisdom - Android Engineer @Savics

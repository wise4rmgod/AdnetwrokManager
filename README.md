# AdnetwrokManager
A Simple Android library to check various types of network connections (WIFI,INTERNET), to allow an android app to check internet connectivity status in realtime.

# Prerequisite
* Androidx
* Kotlin

[![Watch the video](https://i.imgur.com/vKb2F1B.png)](https://res.cloudinary.com/wise4rmgod/video/upload/v1585408036/Github_recording.......mov)

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
```



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

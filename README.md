# android-kotlin-splashscreen
Create SplashScreen by using handler to hold the screen for specific time

[![SplashScreen with Kotlin in Android](https://i.imgur.com/5JYbq2J.png)](https://youtu.be/A-lXw-TJA60)

```kotlin
// styles.xml
<style name="SplashTheme" parent="Theme.AppCompat.Light.NoActionBar"></style>
```
```kotlin
// AndroidManifest.xml
<activity android:name=".SplashScreen"
    android:theme="@style/SplashTheme"
    android:noHistory="true">
    <intent-filter>
        <action android:name="android.intent.action.MAIN" />

        <category android:name="android.intent.category.LAUNCHER" />
    </intent-filter>
</activity>
```
```kotlin
// MainActivity.kt
override fun onCreate(savedInstanceState: Bundle?) {
    super.onCreate(savedInstanceState)
    setContentView(R.layout.activity_splash_screen)

    Handler().postDelayed({
        val intent = Intent(this, MainActivity::class.java)
        startActivity(intent)
    }, 500)
}
```

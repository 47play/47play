### eclipse或者手动接入

##### （1）引入SDK文件lib47play.jar

##### （2）拷贝assets和res到对应的目录

##### （3）修改AndroidManifest.xml

```xml
	<uses-permission android:name="android.permission.INTERNET" />
	<uses-permission android:name="android.permission.REQUEST_INSTALL_PACKAGES" />
	
	<application
        android:allowBackup="true"
        android:label="@string/app_name"
        android:supportsRtl="true" >
        <activity
            android:name="com.sdk.play47.SdkActivity"
            android:configChanges="orientation|screenSize|keyboardHidden"
            android:theme="@android:style/Theme.Dialog"
            android:windowSoftInputMode="stateAlwaysHidden|adjustResize" />

        <!-- 7.0调用安装程序 -->
        <provider
            android:name="android.support.v4.content.FileProvider"
            android:authorities="${applicationId}.fileprovider"
            android:exported="false"
            android:grantUriPermissions="true" >
            <meta-data
                android:name="android.support.FILE_PROVIDER_PATHS"
                android:resource="@xml/play47_plugin" />
        </provider>
    </application>
```
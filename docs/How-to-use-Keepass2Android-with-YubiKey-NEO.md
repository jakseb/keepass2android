# How to use Keepass2Android with YubiKey NEO

Please refer to the documentation on the Keepass website (<http://keepass.info/help/kb/yubikey.html>) or the Yubico website (<http://www.yubico.com/applications/password-management/consumer/keepass/>)
 on how to set up a Keepass 2 database with Yubikey/OTP protection.

After successful setup you should have the database file, e.g. yubi.kdbx, and the OTP auxiliary file, e.g. yubi.otp.xml, both in the same folder.

[![OTPAuxFile](How%20to%20use%20Keepass2Android%20with%20YubiKey%20NEO_OTPAuxFile_thumb.png)](How%20to%20use%20Keepass2Android%20with%20YubiKey%20NEO_OTPAuxFile_2.png)

Make sure you make **both files** available to Keepass2Android, e.g. by placing them both in your Dropbox.

Now you should check your NDEF setup of the Yubikey NEO. Therefore, go to the Tools menu in the Yubico Personalization Utility. Select the same slot as used for OTPs with Keepass 2. The default setting for NDEF type and payload should work. If you experience
 problems, you may use the configuration as shown in this screenshot or simply press the &ldquo;Reset&rdquo; button:

[![image](How%20to%20use%20Keepass2Android%20with%20YubiKey%20NEO_image_thumb.png)](How%20to%20use%20Keepass2Android%20with%20YubiKey%20NEO_image_2.png)

In Keepass2Android, select &quot;Open file&quot; and locate your database file, e.g. yubi.kdbx.

In the password screen under &quot;Select master key type&quot; select &quot;Password &#43; OTP&quot;.

[![Screenshot_2013-12-13-06-38-50](How%20to%20use%20Keepass2Android%20with%20YubiKey%20NEO_Screenshot_2013-12-13-06-38-50_thumb.png)](How%20to%20use%20Keepass2Android%20with%20YubiKey%20NEO_Screenshot_2013-12-13-06-38-50_2.png)

Click &quot;Load auxiliary OTP file&quot;. This is required to load the information how many OTPs must be entered. As loading the file might require user action in some cases, this is not performed automatically.

[![Screenshot_2013-12-13-06-38-12](How%20to%20use%20Keepass2Android%20with%20YubiKey%20NEO_Screenshot_2013-12-13-06-38-12_thumb.png)](How%20to%20use%20Keepass2Android%20with%20YubiKey%20NEO_Screenshot_2013-12-13-06-38-12_2.png)

After loading the OTP auxiliary file, you should see a few text fields for entering the OTPs. Now swipe your YubiKey NEO at the back of your Android device. If you have multiple apps which can handle NFC actions, you might be prompted to select which app to
 use. Select Keepass2Android in this case. Swipe your YubiKey again until all OTP fields are filled. Note: You don't need to select the next text field, this is done automatically!

[![Screenshot_2013-12-13-06-38-36](How%20to%20use%20Keepass2Android%20with%20YubiKey%20NEO_Screenshot_2013-12-13-06-38-36_thumb.png)](How%20to%20use%20Keepass2Android%20with%20YubiKey%20NEO_Screenshot_2013-12-13-06-38-36_2.png)

Don't forget to also enter your password and click OK. You will see the &ldquo;Saving auxiliary OTP file&hellip;&rdquo; dialog. Note that there is some encryption envolved which is probably fast on your PC but might take some time on your mobile device. You
 can reduce the look-ahead window length to speed this up.

[![Screenshot_2013-12-13-06-39-47](How%20to%20use%20Keepass2Android%20with%20YubiKey%20NEO_Screenshot_2013-12-13-06-39-47_thumb.png)](How%20to%20use%20Keepass2Android%20with%20YubiKey%20NEO_Screenshot_2013-12-13-06-39-47_2.png)

## A note about offline access

If your database is stored in the cloud or on the web, you can still access it if you have enabled file caching (which is on by default). With OTPs, this becomes a little bit more complicated: If you repeatedly open your datbase while being offline, the
 OTP counter stored on the Yubikey will be increased. Don&rsquo;t forget to synchronize the database (which will also synchronize the OTP auxiliary file) as soon as possible to avoid problems with accessing your database on other devices! If you often need
 to open the database while you&rsquo;re offline, consider increasing the look-ahead window length!

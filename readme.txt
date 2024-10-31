=== DX reCaptcha for Jetpack ===
Contributors: devrix
Tags: multisite, forms, contact, jetpack, spam, anti-spam, captcha, google, recaptcha
Requires at least: 3.1
Tested up to: 5.5.1
Stable tag: 0.2.3
Requires PHP: 5.6
License: GPLv2 or later
License URI: https://www.gnu.org/licenses/gpl-2.0.html
Author URI: https://devrix.com/

Google reCaptcha integration for Jetpack contact forms

== Description ==

DX reCaptcha for Jetpack plugin helps integrate Google reCaptcha in your Jetpack contact forms.

This plugin opts to filter your content and search for `[contact-form]` shortcode (i.e find the inserted contact forms) and append a new field to these forms, for parsing the Google reCaptcha `[jp-recaptcha]`.

If you're adding the contact form shortcode somewhere where the plugin cannot filter with `the_content` filter, please either add the shortcode `[jp-recaptcha]` where you want the reCaptcha field to be parsed, or better off, just point this plugin to filter your content with the following code:

<pre>
// get the global instance of JPreCaptcha class
global $JPreCaptchaCore;

// if your content is pluggable with a filter
add_filter('my_content_filter_tag_name', array($JPreCaptchaCore, 'appendField'));

// or, if not, just call the method directly
echo $JPreCaptchaCore::appendField( $myHTML );
</pre>

Once you activate the plugin, you should now navigate to "Settings" > "DX JP reCaptcha" (or "Options" > "DX JP reCaptcha" for network activated plugin) and add your Google reCaptcha credentials (public and private keys) which you can obtain from https://www.google.com/recaptcha/admin

**Translations:**

DX reCaptcha for Jetpack plugin is translated by the community into the following languages:

* Polish by [Maciej Michalowski](http://michalowski.pro)


**Stay up to date**

*Become a fan on Facebook*
[https://www.facebook.com/DevriXLtd](https://www.facebook.com/DevriXLtd "Facebook DevriX")

*Follow us on Twitter*
[https://twitter.com/wpdevrix](https://twitter.com/wpdevrix)

== Installation ==

1. Visit 'Plugins > Add New'
2. Search for 'DX reCaptcha for Jetpack'
3. Activate DX reCaptcha for Jetpack from your Plugins page. You will have to activate it for the whole network.

Once you activate the plugin, you should now navigate to "Settings" > "JP reCaptcha" (or "Options" > "JP reCaptcha" for network activated plugin) and add your Google reCaptcha credentials (public and private keys) which you can obtain from https://www.google.com/recaptcha/admin

== Screenshots ==

1. Example form with reCaptcha field and a failed submission
2. Admin settings screen


== Frequently Asked Questions ==

= Where are the plugin's settings? =

In your WordPress admin under Settings -> DX JP reCaptcha

= How to get your reCaptcha Keys? =
Go to Settings -> DX JP reCaptcha and click to [Google reCaptcha](https://www.google.com/recaptcha/intro/v3.html "Google reCaptcha")
Now go to Google reCAPTCHA and register a new reCaptcha. This step is needed so you can register this key later
Once you are ready, please go to Google reCAPTCHA site and click to Admin Console. Now you are in the administrative part of the site
Click on the “plus button” in the top right corner and fill your data to get a key
Once you hit the submit button you will receive your keys
The contact form is now secured

== Upgrade Notice ==
The plugin ownership was transferred to DevriX. There are no functionality changes. We are going to work on a few version, adding some nice feature in the near feature, stay tuned! :)


== Changelog ==

= 0.1 =
* Initial stable release.

= 0.2 =
* Added Polish translation, thanks Maciej Michalowski!

= 0.2.2 =
* Code refactor and updated plugin info

= 0.2.3 =
* Validate readme.txt 
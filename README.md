# Salesforce.com Mobile SDK for Android

You have arrived at the source repository for the Salesforce Mobile SDK for Android. Welcome! Starting with our 2.0 release, there are now two ways you can choose to work with the Mobile SDK:

- If you'd like to work with the source code of the SDK itself, you've come to the right place! You can browse sample app source code and debug down through the layers to get a feel for how everything works under the covers. Read on for instructions on how to get started with the SDK in your development environment.
- If you're just eager to start developing your own application, the quickest way is to use our npm binary distribution package, called [forcedroid](https://npmjs.org/package/forcedroid), which is hosted on [npmjs.org](https://npmjs.org/). Getting started is as simple as installing the npm package and launching your template app. You'll find more details on the forcedroid package page.

Installation (do this first - really)
==

After cloning the SalesforceMobileSDK-Android project from github, run the install script from the command line:

`./install.sh`

This pulls submodule dependencies from github.

(Windows users: run `cscript install.vbs` from the command line instead.)

Introduction
==

### What's New in 3.2

**SmartSync Library Enhancements**
- SmartSync now supports incremental sync, which allows the developer to download only data that has been updated on the server, rather than the entire data set.
- The sync up operation now offers merge modes that let the developer decide whether to overwrite data that has been modified on the server or discard local changes.
- SmartSync now supports custom targets, which can manage the data interchange in sync operations. Custom targets let you tailor network interactions to the specific demands of the sync operation.

**SmartStore Library Enhancements**
- SmartStore now provides the ability to obtain a global (app-level) SmartStore instance. A global SmartStore instance can be populated with user-agnostic data that will not be deleted when users log out.

**Sample App Updates**
- SmartSyncExplorer has been updated to demonstrate periodic background sync at a specified interval.
- A new sample app, `NoteSync`, has been added to demonstrate the syncing of content notes using custom targets.

**Other Technical Improvements**
- It is now possible to obtain an unauthenticated RestClient instance for use with APIs that do not require authentication.
- Various bug fixes.

Check http://developer.force.com/mobilesdk for additional articles and tutorials

### Native Applications
The Salesforce Mobile SDK provides essential libraries for quickly building native mobile apps that seamlessly integrate with the Salesforce cloud architecture.  Out of the box, we provide an implementation of OAuth2, abstracting away the complexity of securely storing refresh tokens or fetching a new session ID when a session expires. The SDK also provides Java wrappers for the Salesforce REST API, making it easy to retrieve, store, and manipulate data.

### Hybrid Applications
HTML5 is quickly emerging as dominant technology for developing cross-platform mobile applications. While developers can create sophisticated apps with HTML5 and JavaScript, some limitations remain, specifically: session management, access to the camera and address book, and the inability to distribute apps inside public App Stores. The Salesforce Mobile Container makes possible to combine the ease of web app development with power of the Android platform by wrapping a web app inside a thin native container, producing a hybrid application.

### WARNING: OAuth2 token storage on devices without encryption
The Salesforce Mobile SDK provides PIN-based OAuth token encryption for Android devices that don't provide full storage encryption functionality.  The SDK implementation is **NOT** designed to provide complete security. It's simply offered as an option for temporarily protecting your app from eavesdroppers. Please use caution in your production deployment with sensitive data. **We strongly recommend deploying production apps on the latest generation of Android devices with build-in device encryption.**

Setting up your Development Environment
==

The following steps will help you get started with your development environment, whether you choose to develop native apps or hybrid apps. See the `README` files in the `native/` and `hybrid/` folders for additional notes pertaining to development in those environments.

1. Install the Android SDK (r21 or above): http://developer.android.com/sdk/index.html
2. Install ant 1.8.0 or later: http://ant.apache.org/manual/install.html (in order to build from the command line)
3. Install Eclipse: http://www.eclipse.org/
4. Install the Android Development Tools (ADT) plugin for Eclipse (r21 or above): http://developer.android.com/sdk/eclipse-adt.html
5. Get setup on github: http://help.github.com/

Downloading the Salesforce SDK
==

To pull down the SDK from github, create a new directory and git clone the salesforce SDK repo.
<pre>
git clone https://github.com/forcedotcom/SalesforceMobileSDK-Android.git
</pre>

Documentation
==

* [SalesforceSDK](http://forcedotcom.github.com/SalesforceMobileSDK-Android/index.html)

Discussion
==

If you would like to make suggestions, have questions, or encounter any issues, we'd love to hear from you.  Post any feedback you have on our [Google+ Community](https://plus.google.com/communities/114225252149514546445).

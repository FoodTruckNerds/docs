# Food Truck Fan features

## Favorites ❤️

Scan QR code to Favorite the Food Truck in our App.

- If the person has the app installed, open the Food Truck profile and favorite the Food Truck automatically
- If the person does not have the app installed, open the food truck in a [Temporary App](#temporary-app-for-info) without installing the app first.
  - The instant app will let them save the food truck to local cache without logging in, so they can receive notifications when the food truck comes back. The instant app will have a button at the bottom for "Favorite". When they click the button, they will see a pop-up dialog telling them that they will be notified when the food truck arrives in their location.
  - Under the "Favorite" button, there will be a "Sign up" button. When they click, offer to install the app immediately, or open the app store page

## Temporary App for info 📲

- Android Instant App
- iOS App Clips

We can show the food truck's profile to users in an App format (rather than web browser) as a way to invite (funnel) users into the app without forcing them to download the app first. We can show some of the information like the Food Truck profile, and, when they click the "Favorite" button, we forward them to the full app to set up their account. This will make people familiar with the app before committing to it.

### Android Instant App

The type of app you're referring to is known as **Android Instant Apps**. These apps allow users to access and use certain features without needing to install the full app on their device. Here's a summary of how they work and their benefits:

1. **Immediate Access**: Instant Apps can be launched with just a tap on a URL, bypassing the need for installation. This is particularly useful for one-time use scenarios, such as paying for parking or viewing a specific video, without cluttering your device with apps you might not use again[1](https://mobisoftinfotech.com/resources/blog/android-instant-apps-android-apps-to-run-instantly-without-installation)[2](https://www.makeuseof.com/tag/try-android-apps-without-installing/)[3](https://www.deccanchronicle.com/technology/in-other-news/070817/use-android-apps-without-installing-them-heres-how.html).
2. **Seamless Experience**: These apps provide a native app experience but run temporarily. They are designed to offer a rich user experience by loading only the necessary parts of the app on demand[1](https://mobisoftinfotech.com/resources/blog/android-instant-apps-android-apps-to-run-instantly-without-installation).
3. **Compatibility**: Instant Apps are compatible with Android devices running Android 4.1 (API level 16) or higher, as long as they have Google Play services installed[1](https://mobisoftinfotech.com/resources/blog/android-instant-apps-android-apps-to-run-instantly-without-installation).
4. **Use Cases**: Examples of use cases include viewing a recipe from a shared link, making a purchase directly from a Google search result, or paying for parking via NFC without having the parking app installed[1](https://mobisoftinfotech.com/resources/blog/android-instant-apps-android-apps-to-run-instantly-without-installation)[3](https://www.deccanchronicle.com/technology/in-other-news/070817/use-android-apps-without-installing-them-heres-how.html).
5. **Developer Integration**: Developers can enable Instant App functionality in their existing apps with minimal effort, using the same Android APIs and source code. This allows for quick setup and deployment[1](https://mobisoftinfotech.com/resources/blog/android-instant-apps-android-apps-to-run-instantly-without-installation).

Instant Apps are a convenient way to interact with apps without the commitment of a full installation, making them ideal for temporary or one-time needs.

To open an app installation process from your instant app in Android, you can follow these steps:

1. **Enable Google Play Instant**: Ensure that Google Play Instant is enabled on the user's device. This allows users to try out a portion of your app without installing it fully. Users can access instant apps through links from search results, emails, or ads [1](https://support.google.com/googleplay/answer/7240211?hl=en).
2. **Use the Install Button**: Within your instant app, provide an "Install" button. When users click this button, they should be directed to a prompt that allows them to install the full version of the app from the Google Play Store. This process is designed to be seamless, making it easy for users to transition from the instant app to the full app [2](https://www.androidauthority.com/use-android-instant-apps-749544/).
3. **App Links**: Implement Android App Links in your instant app. These links ensure that when a user clicks on a URL associated with your app, it opens the instant app instead of a web browser. This requires verifying your website's ownership of the URLs and setting up intent filters in your app's manifest [3](https://developer.android.com/training/app-links/instant-app-links).
4. **Instant-Enabled App Bundle**: Create an instant-enabled app bundle using Android Studio. This bundle includes the necessary components for both the instant and full versions of your app. You can manage this through the Google Play Console under the instant app production track [4](https://developer.android.com/topic/google-play-instant/getting-started/instant-enabled-app-bundle).
5. **Prompt Users to Install**: Use the Google Play Instant Development SDK to detect when your app is running as an instant app. You can then display a prompt inviting users to install the full app, ensuring a smooth transition from the instant experience to the full app [4](https://developer.android.com/topic/google-play-instant/getting-started/instant-enabled-app-bundle).

By following these steps, you can effectively guide users from trying your instant app to installing the full version, providing a seamless and convenient experience.

#### iOS App Clips

For iPhone users, there are a few alternatives to using full apps without installation, similar to Android's Instant Apps. These options provide quick access to app-like functionality without the need for a full download:

1. **Mini-Apps**: These are lightweight versions of apps that run within other apps like WeChat or Snapchat. They are written in HTML5 and offer quick, interactive experiences without requiring installation. They are commonly used for tasks like ordering food or playing simple games[4](https://www.cnbc.com/2020/09/01/how-to-get-iphone-software-without-using-apples-app-store.html).
2. **App Clips**: Introduced by Apple, App Clips are small parts of an app that can be quickly accessed via QR codes, NFC tags, or links. They provide a limited but immediate functionality, such as renting a scooter or ordering take-out, without downloading the full app[4](https://www.cnbc.com/2020/09/01/how-to-get-iphone-software-without-using-apples-app-store.html).

These methods offer iPhone users ways to access app functionalities without committing to a full installation, providing convenience for one-time or temporary use cases.

## Experimental ideas

Augmented Reality 🤳: Scan QR code to see an AR menu.

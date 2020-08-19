# Rakuten Analytics SDK for Android

The Analytics module enables applications to record user activity and automatically send tracking events to a configured endpoint.

This SDK supports Android API level 21 (Lollipop) and above and has been tested with Android API level 21 (Lollipop) and above. It is intended to be used only by Rakuten approved applications.

This repository contains the published Analytics artifacts using [GitHub Packages](https://docs.github.com/en/packages).

## Getting started

To access and use the Analytics artifacts, you must add the Analytics GitHub Packages repository to your project's Gradle config.

```gradle
repositories {
  maven("https://maven.pkg.github.com/rakutentech/android-analytics") {
    credentials {
      username = "your_github_username"
      password = "your_github_personal_access_token"
    }
  }
}

dependency {
  implementation 'com.rakuten.tech.mobile.analytics:analytics:${latest_version}'
}
```

You will need to have an access token with `read:packages` scope to be able to install a GitHub package.

To get a token, go to the Settings page on your GitHub account. Go to Developer settings > Personal access tokens and generate a new token.

See [About Tokens](https://docs.github.com/en/packages/publishing-and-managing-packages/about-github-packages#about-tokens) for more details.

### SDK Integration

### #1 Configure RAT Tracker in your app's `AndroidManifest.xml`
```xml
<manifest>
  <application >
    <meta-data  android:name="com.rakuten.tech.mobile.analytics.RATAccountId"
                android:value="YOUR_RAT_ACCOUNT_ID" />
    <meta-data  android:name="com.rakuten.tech.mobile.analytics.RATApplicationId"
                android:value="YOUR_RAT_APPLICATION_ID" />
    <meta-data  android:name="com.rakuten.tech.mobile.analytics.RATEndpoint"
                android:value="YOUR_ENDPOINT" />
  </application>
</manifest>
```

### #2 Track an event
```java
// Create Map for Parameters
Map<String, Object> params = new HashMap<>();
params.put("foo", "bar");

// Create event track it
RatTracker.event("click", params).track();
```

For more information (including full configuration instructions, how to get support, API usage, and a full change log) please visit the internal documentation site of the `android-analytics` SDK or raise an inquiry with your Rakuten contact.
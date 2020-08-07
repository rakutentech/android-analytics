# Analytics SDK for Android

The Analytics module enables applications to record user activity and automatically send tracking events to the Rakuten Analytics Tracker.

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


### SDK Integration (in-progress)

Please see the [User Guide](https://rakutentech.github.io/android-analytics/) for instructions on integrating the SDK to your application.
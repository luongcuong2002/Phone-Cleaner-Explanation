# Phone Cleaner Explanation
- For security reasons, I cannot share the source code or APK file. Instead, I will share what I have done in this project through screenshots accompanied by descriptions.
> Due to a violation of Google's policies, the store hosting this application has been banned from the Google Play Store. Therefore, this app is currently not available on the Play Store.

## Overview
- This is an application that is cloned based on [CCleaner](https://play.google.com/store/apps/details?id=com.piriform.ccleaner) and includes nearly all the features that [CCleaner](https://play.google.com/store/apps/details?id=com.piriform.ccleaner) has.
- It utilizes [Flutter](https://flutter.dev/) for UI and employs [Android Native](https://developer.android.com/docs) to handle all system-related functionalities.
## What is my role in this project?
- My role is to write the functional functions in Android Native, such as getSimilarPhotos(), uninstallApps(), getAppUsageTime(), etc.
- Others will invoke them in Flutter through Method Channels and use the data provided by these functions to display the UI.
- See, [writing custom platform-specific code](https://docs.flutter.dev/platform-integration/platform-channels).
## What I have done
- _I have made numerous features in this project, and here are some of them._

---
#### Detect similar photos
- This feature utilizes [OpenCV](https://github.com/QuickBirdEng/opencv-android) to analyze the similarity level between two images and then provides the result.
<img width="250" alt="similar_photo" src="https://github.com/LuongCuong244/Phone-Cleaner-Explanation/assets/83854080/957156dc-3c07-4aff-9267-f5027425e680">

---
#### The number of app openings and usage time
- Using [UsageStatsManager](https://developer.android.com/reference/android/app/usage/UsageStatsManager) to retrieve [UsageEvents](https://developer.android.com/reference/android/app/usage/UsageEvents), we can calculate the number of app openings and the usage time of a specific application within a certain time period.

<img width="510" alt="photo" src="https://github.com/LuongCuong244/Phone-Cleaner-Explanation/assets/83854080/5fb40ab9-ba8a-4ed7-b1b4-00ab9a619d27">
<img width="250" alt="app_usage_time_demo" src="https://github.com/LuongCuong244/Phone-Cleaner-Explanation/assets/83854080/9202faf9-df77-4b37-82b5-9950c5444cb3">

#### Notification count
- Using [NotificationListenerService](https://developer.android.com/reference/android/service/notification/NotificationListenerService) to listen for when a notification is posted.

<img width="250" alt="notification_count_demo" src="https://github.com/LuongCuong244/Phone-Cleaner-Explanation/assets/83854080/81bafe47-1da5-4bd2-b046-606360857d12">

#### Optimize image
- Simply use [Bitmap.compress](https://developer.android.com/reference/android/graphics/Bitmap#compress(android.graphics.Bitmap.CompressFormat,%20int,%20java.io.OutputStream)) to optimize the image and then save it to the device.

<img width="250" alt="optimize_image" src="https://github.com/LuongCuong244/Phone-Cleaner-Explanation/assets/83854080/22bdeee2-0137-436f-ab37-6e4f1056902c">

#### Uninstall app
- Use [Intent.ACTION_UNINSTALL_PACKAGE](https://developer.android.com/reference/android/content/Intent#ACTION_UNINSTALL_PACKAGE) to request uninstallation of the application.

https://github.com/LuongCuong244/Phone-Cleaner-Explanation/assets/83854080/fe374baf-3957-4903-90d3-bc7128d8ce7c





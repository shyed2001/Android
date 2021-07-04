# Android
## Android Workflow
The workflow to develop an app for Android is conceptually the same as other app platforms. However, to efficiently build a well-designed app for Android, you need some specialized tools. The following list provides an overview of the process to build an Android app and includes links to some Android Studio tools you should use during each phase of development.
 
* Set up your workspace
   - This is the phase you probably already finished: Install Android Studio and create a project.For a walkthrough with Android Studio that teaches some Android development fundamentals, also check out the guide to Building your first app.

* Write your app:
  - Now you can get to work. Android Studio includes a variety of tools and intelligence to help you work faster, write quality code, design a UI, and create resources for different device types. For more information about the tools and features available, see Write your app.

* Build and run
  - During this phase, you build your project into a debuggable APK package that you can install and run on the emulator or an Android-powered device. For more information about how to run your code, see Build and run your app.You can also begin customizing your build. For example, you can create build variants that produce different types of APKs from the same project, and shrink your code and resources to make your APK file smaller. For an introduction to customizing your build, see Configure your build.

* Debug, profile, and test
  - This is the iterative phase in which you continue writing your app but with a focus on eliminating bugs and optimizing app performance. Of course, creating tests will help you in those endeavors.For information about basic debugging tasks, read Debug your app and Write and view logs.To view and analyze various performance metrics such as memory usage, network traffic, CPU impact, and more, see Performance profiling tools. And for an introduction to building tests, see Test your app.

* Publish
  - When you're ready to release your app to users, there are just a few more things to consider, such as versioning your app and signing it with a key. For more information, see the Publish your app.
 
 
 
 
 
# Problems and Issues with Android developmen and Fixes:

## Intel HAXM Installation /  Uninstallation failed in Android studio SDK manager

```shell
>PowerShell 7.1.3
Copyright (c) Microsoft Corporation.

https://aka.ms/powershell
Type 'help' to get help.

PS C:\Users\shyed> C:"Program Files"\Intel\HAXM\checktool.exe --verbose
CPU vendor * GenuineIntel
Intel64 supported * Yes
VMX supported * Yes
VMX enabled * Yes
EPT supported * Yes
NX supported * Yes
NX enabled * Yes
Hyper-V disabled * Yes
OS version * Windows 10.0.19043
OS architecture * x86_64
Guest unoccupied * Yes. 0 guest(s)
PS C:\Users\shyed> echo %ERRORLEVEL%
%ERRORLEVEL%
PS C:\Users\shyed> bcdedit /set hypervisorlaunchtype off
The operation completed successfully.
PS C:\Users\shyed> echo %ERRORLEVEL%
%ERRORLEVEL%
PS C:\Users\shyed> C:"Program Files"\Intel\HAXM\checktool.exe --verbose
CPU vendor * GenuineIntel
Intel64 supported * Yes
VMX supported * Yes
VMX enabled * Yes
EPT supported * Yes
NX supported * Yes
NX enabled * Yes
Hyper-V disabled * Yes
OS version * Windows 10.0.19043
OS architecture * x86_64
Guest unoccupied * Yes. 0 guest(s)
PS C:\Users\shyed> echo %ERRORLEVEL%
%ERRORLEVEL%
PS C:\Users\shyed>

```

### run below command to see whether the output is 0 after running checktool.exe?

```shell
> echo %ERRORLEVEL%

```

If the output is not 0, try to run below command to disable Hyper-V and reboot your Windows.

```shell
> bcdedit /set hypervisorlaunchtype off

```

This was helpful.
-----

But could not run emulator on android studio.
--------
> ### If having problem running Android Emulator with API level 30 , Move down and install Lower level API and Android versions.

> ### Or Can Use Online Emulator to upload and test / run apk.

> ### Or can use an actual android device

## Fixed Error Emulator was killed android studio | The Emulator process for AVD was killed Fixed Error Emulator was killed android studio | The Emulator process for AVD was killed
 https://www.youtube.com/watch?v=AOK9ZxiBOGg


- solution-: Restart Your PC, it works in many cases.

- solution-: AVD Manager - Edit - Graphics : From Automatic(by default) change to Software.


# How to export an Android Studio project and move it to another computer

We explain how to export an Android Studio project and move it to another computer. Instructions for beginners or anybody who started with Android Studio.

## Transfer android project from one computer to another (Android Studio)

https://www.youtube.com/watch?v=lG8CV3nRQh8

## How To Import Project Into Android Studio

 https://www.youtube.com/watch?v=FeKfIWJyQMs


# How to export an Android Studio project?
--  

 We get asked about this a lot from our students at Code Development. Students want to move Android Studio projects from one computer to another. They are constantly showing their projects and asking how they can improve their project even further, and for that, they need to move it to a different computer or send it to a colleague. However, you have to know How to export an Android Studio project in the right way. 

Projects do not work on all computers. If you do not move a project the right way, it might not work on a target computer. That’s why we decided to write a short step by step guide on how to do it. Projects do not work on all computers. If you do not move a project the right way, it might not work on a target computer. Consequently, that’s why we decided to write a short step by step guide on how to do it.

## Learn about exporting an Android Studio project:

How to use a tool: Export to Zip File…
Manually export Android Studio project
How to locate the project folder
How to clean the folder for shorter export size
Create a zip or a package
 

If you are starting and don’t even have Android Studio, you can download it for free. All in all, exporting a project is a good way to start for beginners if you ask your friend to share a project with you. This way, you see how to start and how the code looks. For others, this is a way to share your knowledge.

# Solution: Export to Zip File… (The new way of exporting Android Studio project)
Export to Zip File… is a new tool available for us in Android Studio 3.0 onwards. You can use it via menu: File | Export to Zip File…

Here is an example of how you can export an Android Project for our Love Calculator from a blog post on how to make an android app. 

First, choose Export to Zip File... from the file menu:

Export an Android Project - Export to Zip

Next, choose the destination and file name:

Export an Android Project - Choose destination

 

All that is left for you to do is to share your zip file.

 

## Manually export an Android Studio project
We can now say that manually exporting a project is the old way to export our projects. In fact, manual export was the only way in older versions of Android Studio (before 3.0) since there was no tool in Android Studio. We have prepared a Windows and Mac version for you to understand the logic behind it better.

## How to export an Android Studio project and make a zip file on Windows
 
### Locate the Android Studio project folder on Windows
Views are a little bit different on Windows and Mac, this is why we have both screenshots for you. These steps are for Windows

In Project Tool Window, you usually have two ways, according to the view mode you have selected. If you are in the Project View, the app name is the first item in the list. In Android view “app” is the first item. See the both options below:

Right click on the application name or “app” to find a folder with all the files from your project.

In Windows, you have the option “Show in Explorer” (in MacOS it’s “Reveal in Finder”). 


###  How to make a zip file (of an Android Studio project) in Windows

Once Android Studio selects the folder for you, it opens an Explorer, and selects a folder within your project folder. To create a zip you have to Right click it and select: “Send To/Compressed (zipped) folder”.

Export an Android Project - Send to compressed

 

With that, you get a “.zip” file that you can take with you, send over mail, share… You can also use GDriver, DropBox, OneDrive or some other kind of Cloud drive.

 

How to export an Android Studio project and make zip on Mac
--- 


In the Project Tool Window, you usually have two ways, according to the view mode you have selected. If you are in the Project View, app name is the first item in the list. In Android view “app” is the first item. See the both options below:

Right click on application name or “app” to find a folder with all the files from your project. Use Reveal in Finder from the context menu (right click on app folder)
Zip in MacOS - Reveal in finder

Once Android Studio locates files and opens up finder for you, choose Compress “...” option from Context menu. It creates a zip file for you.

## Clean the folder to reduce the size of the export project
### Main folder files you can delete:To Reduce size. App folder files you can delete:Remove App folder files . For simple projects you reduce project zip size quite a bit, for our example: 5.2MB -> 0.4MB

#### For more advanced users you can also clean up your zip file to reduce its length. In the first place, you remove “build” folders. The first one is in the main folder and the second one in the “app” folder. In addition, you can also remove .iml files (these files are computer associated with relative paths and are created on other computers automatically).

 

# Conclusion

Knowing how to export an Android Studio project is excellent when you need to move files and code to another computer over mail or sharing it in any other way. Moreover, sharing projects like this can be a perfect way of collaboration for beginners. Equally important, when working on a larger project there is a better way of sharing projects, you mostly use version control systems like GIT (preferably on a cloud solution like BitBucket, GitHub,... or local if needed; plain Git or something like GitLab).

In conclusion, exporting a project and using GIT is one of the skills you need to become an Android Developer, read more in our blog post about all the skills needed to be an Android Developer.

Have fun, coding software solutions with Code.


# অ্যান্ড্রয়েড
## অ্যান্ড্রয়েড ওয়ার্কফ্লো
অ্যান্ড্রয়েডের জন্য একটি অ্যাপ্লিকেশন বিকাশের কর্মপ্রবাহটি অন্যান্য অ্যাপ্লিকেশন প্ল্যাটফর্মের মত ধারণাগতভাবে একই। তবে অ্যান্ড্রয়েডের জন্য দক্ষতার সাথে একটি ভাল ডিজাইনের অ্যাপ তৈরি করতে আপনার কিছু বিশেষ সরঞ্জামের প্রয়োজন need নিম্নলিখিত তালিকাটিতে অ্যান্ড্রয়েড অ্যাপ তৈরির প্রক্রিয়াটির ওভারভিউ সরবরাহ করে এবং উন্নয়নের প্রতিটি পর্যায়ে আপনার ব্যবহার করা উচিত এমন কিছু অ্যান্ড্রয়েড স্টুডিও সরঞ্জামগুলির লিঙ্ক অন্তর্ভুক্ত করে।
 
* আপনার কর্মক্ষেত্র সেট আপ করুন
   - এটি সম্ভবত আপনার ইতিমধ্যে শেষ হওয়া পর্ব: অ্যান্ড্রয়েড স্টুডিও ইনস্টল করুন এবং একটি প্রকল্প তৈরি করুন some অ্যান্ড্রয়েড স্টুডিওর সাথে চলার জন্য যা কিছু অ্যান্ড্রয়েড বিকাশের মৌলিক বিষয়গুলি শেখায়, আপনার প্রথম অ্যাপটি তৈরির গাইডও পরীক্ষা করে দেখুন।

* আপনার অ্যাপটি লিখুন:
  - এখন আপনি কাজ পেতে পারেন। অ্যান্ড্রয়েড স্টুডিওতে আপনাকে আরও দ্রুত কাজ করতে, মানের কোড লিখতে, একটি ইউআই ডিজাইন করতে এবং বিভিন্ন ডিভাইসের ধরণের সংস্থান তৈরি করতে সহায়তা করতে বিভিন্ন সরঞ্জাম এবং বুদ্ধি অন্তর্ভুক্ত। উপলভ্য সরঞ্জামগুলি এবং বৈশিষ্ট্যগুলি সম্পর্কে আরও তথ্যের জন্য, আপনার অ্যাপ্লিকেশনটি লিখুন দেখুন।

* নির্মাণ এবং চালানো
  - এই ধাপের সময় আপনি নিজের প্রকল্পটি ডিবাগযোগ্য এপিএল প্যাকেজে তৈরি করেন যা আপনি এমুলেটর বা অ্যান্ড্রয়েড চালিত ডিভাইসে ইনস্টল করে চালাতে পারবেন। আপনার কোডটি কীভাবে চালানো যায় সে সম্পর্কে আরও তথ্যের জন্য, আপনার অ্যাপ্লিকেশনটি তৈরি করুন এবং চালান দেখুন You আপনি নিজের বিল্ডটি কাস্টমাইজ করাও শুরু করতে পারেন। উদাহরণস্বরূপ, আপনি একই প্রকল্প থেকে বিভিন্ন প্রকারের APK তৈরি করতে পারে এমন বিল্ড ভেরিয়েন্ট তৈরি করতে পারেন এবং আপনার APK ফাইলকে আরও ছোট করতে আপনার কোড এবং সংস্থান সংকুচিত করতে পারেন। আপনার বিল্ডটি কাস্টমাইজ করার জন্য একটি পরিচিতির জন্য দেখুন আপনার বিল্ডটি কনফিগার করুন।

* ডিবাগ, প্রোফাইল এবং পরীক্ষা
  - এটি পুনরাবৃত্তির পর্যায়ে আপনি নিজের অ্যাপটি লিখতে চালিয়ে যাচ্ছেন তবে বাগগুলি মুছে ফেলার এবং অ্যাপের কার্য সম্পাদনকে অনুকূলকরণের দিকে মনোনিবেশ রেখে। অবশ্যই, পরীক্ষাগুলি তৈরি করা আপনাকে সেই প্রচেষ্টাগুলিতে সহায়তা করবে basic মৌলিক ডিবাগিংয়ের কাজগুলি সম্পর্কে তথ্যের জন্য, আপনার অ্যাপ্লিকেশনটিকে ডিবাগ করুন এবং লগগুলি লিখুন এবং দেখুন memory মেমরির ব্যবহার, নেটওয়ার্ক ট্র্যাফিক, সিপিইউ প্রভাব এবং আরও অনেকগুলি পারফরম্যান্সের মেট্রিকগুলি দেখতে ও বিশ্লেষণ করতে, পারফরম্যান্স প্রোফাইলিং সরঞ্জামগুলি দেখুন। বিল্ডিং টেস্টগুলির পরিচিতির জন্য, আপনার অ্যাপ্লিকেশনটি পরীক্ষা করুন।

* প্রকাশ
  - আপনি যখন আপনার অ্যাপ্লিকেশন ব্যবহারকারীদের কাছে প্রকাশ করতে প্রস্তুত হবেন তখন আপনাকে আরও কয়েকটি বিষয় বিবেচনা করতে হবে যেমন আপনার অ্যাপ্লিকেশনটির সংস্করণ করা এবং কী দিয়ে এটিতে স্বাক্ষর করা। আরও তথ্যের জন্য, আপনার অ্যাপ্লিকেশনটি প্রকাশ করুন দেখুন।
 
 
# অ্যান্ড্রয়েড বিকাশকারী এবং ফিক্সগুলির সাথে সমস্যা এবং সমস্যা:

## অ্যান্ড্রয়েড স্টুডিও এসডিকে পরিচালকের ইনটেল HAXM ইনস্টলেশন / আনইনস্টলশন ব্যর্থ

* যদি এপিআই লেভেল 30 সহ অ্যান্ড্রয়েড এমুলেটর চালনায় সমস্যা হয় তবে নীচে সরান এবং নিম্ন স্তরের এপিআই এবং অ্যান্ড্রয়েড সংস্করণ ইনস্টল করুন।

*  বা অ্যাপ্লিকেশন আপলোড এবং পরীক্ষার জন্য অনলাইন এমুলেটর ব্যবহার করতে পারেন।

*  অথবা প্রকৃত অ্যান্ড্রয়েড ডিভাইস ব্যবহার করতে পারেন

স্থির ত্রুটি এমুলেটরটি অ্যান্ড্রয়েড স্টুডিও নিহত হয়েছিল | এভিডির জন্য এমুলেটর প্রক্রিয়াটি হত্যা করা হয়েছিল স্থির ত্রুটি এমুলেটরকে হত্যা করা হয়েছিল অ্যান্ড্রয়েড স্টুডিও | এভিডির এমুলেটর প্রক্রিয়াটি হত্যা করা হয়েছিল
 https://www.youtube.com/watch?v=AOK9ZxiBOGg


সমাধান-: আপনার পিসি পুনরায় চালু করুন, এটি অনেক ক্ষেত্রে কাজ করে।

সমাধান-: এভিডি ম্যানেজার - সম্পাদনা - গ্রাফিকস: স্বয়ংক্রিয় থেকে (ডিফল্টরূপে) সফ্টওয়্যারটিতে পরিবর্তন।


# কীভাবে একটি অ্যান্ড্রয়েড স্টুডিও প্রকল্প রফতানি করতে এবং এটি অন্য কম্পিউটারে সরানো যায়

আমরা ব্যাখ্যা করি কীভাবে একটি অ্যান্ড্রয়েড স্টুডিও প্রকল্প রফতানি করা যায় এবং এটিকে অন্য কম্পিউটারে স্থানান্তরিত করতে হয়। নবীনতর বা যে কেউ অ্যান্ড্রয়েড স্টুডিও দিয়ে শুরু করেছেন তাদের জন্য নির্দেশাবলী।

# অ্যান্ড্রয়েড প্রকল্পটি একটি কম্পিউটার থেকে অন্য কম্পিউটারে স্থানান্তর করুন (অ্যান্ড্রয়েড স্টুডিও)

https://www.youtube.com/watch?v=lG8CV3nRQh8

## অ্যান্ড্রয়েড স্টুডিওতে কীভাবে প্রকল্পটি আমদানি করা যায়

 https://www.youtube.com/watch?v=FeKfIWJyQMs


# কীভাবে একটি অ্যান্ড্রয়েড স্টুডিও প্রকল্প রফতানি করবেন?
-
কোড বিকাশে আমাদের শিক্ষার্থীদের কাছ থেকে আমরা এটি সম্পর্কে অনেক কিছু জানতে চাই। শিক্ষার্থীরা অ্যান্ড্রয়েড স্টুডিও প্রকল্পগুলি এক কম্পিউটা থেকে অন্য কম্পিউটারে সরিয়ে নিতে চায়। তারা ক্রমাগত তাদের প্রকল্পগুলি দেখায় এবং জিজ্ঞাসা করছে যে কীভাবে তারা আরও আরও আরও উন্নত করতে পারে এবং তার জন্য তাদের এটিকে অন্য কম্পিউটারে সরিয়ে নেওয়া বা সহকর্মীর কাছে প্রেরণ করা প্রয়োজন। তবে আপনাকে কীভাবে একটি অ্যান্ড্রয়েড স্টুডিও প্রকল্পটি সঠিক উপায়ে রফতানি করতে হবে তা জানতে হবে।

প্রকল্পগুলি সমস্ত কম্পিউটারে কাজ করে না। আপনি যদি কোনও প্রকল্পটি সঠিকভাবে না সরান, এটি কোনও লক্ষ্যযুক্ত কম্পিউটারে কাজ নাও করতে পারে। সে কারণেই আমরা কীভাবে এটি করব সে সম্পর্কে পদক্ষেপ গাইড দ্বারা একটি ছোট পদক্ষেপ লেখার সিদ্ধান্ত নিয়েছি। প্রকল্পগুলি সমস্ত কম্পিউটারে কাজ করে না। আপনি যদি কোনও প্রকল্পটি সঠিকভাবে না সরান, এটি কোনও লক্ষ্যযুক্ত কম্পিউটারে কাজ নাও করতে পারে। ফলস্বরূপ, এজন্যই আমরা কীভাবে এটি করব সে সম্পর্কে পদক্ষেপ গাইড দ্বারা একটি ছোট পদক্ষেপ লেখার সিদ্ধান্ত নিয়েছি।

# অ্যান্ড্রয়েড স্টুডিও প্রকল্প রফতানি সম্পর্কে জানুন:

কীভাবে কোনও সরঞ্জাম ব্যবহার করবেন: জিপ ফাইলে রফতানি করুন…
ম্যানুয়ালি অ্যান্ড্রয়েড স্টুডিও প্রকল্প রফতানি করুন
প্রকল্পের ফোল্ডারটি কীভাবে সনাক্ত করা যায়
সংক্ষিপ্ত রপ্তানি আকারের জন্য ফোল্ডারটি কীভাবে পরিষ্কার করবেন
একটি জিপ বা একটি প্যাকেজ তৈরি করুন
 

যদি আপনি শুরু করছেন এবং অ্যান্ড্রয়েড স্টুডিও নাও পেয়ে থাকেন তবে আপনি এটি বিনামূল্যে ডাউনলোড করতে পারেন। সব মিলিয়ে, আপনি যদি আপনার বন্ধুকে আপনার সাথে একটি প্রকল্প ভাগ করে নিতে বলেন তবে একটি প্রকল্প রফতানি করা নতুনদের জন্য শুরু করার এক ভাল উপায়। এইভাবে, আপনি কীভাবে শুরু করবেন এবং কোডটি কীভাবে দেখায় তা দেখুন। অন্যদের জন্য, এটি আপনার জ্ঞান ভাগ করার একটি উপায়।

# সমাধান: জিপ ফাইলে রফতানি করুন ... (অ্যান্ড্রয়েড স্টুডিও প্রকল্প রফতানির নতুন উপায়)
জিপ ফাইলে রফতানি করা ... অ্যান্ড্রয়েড স্টুডিও 3.0.০ এর পরে আমাদের জন্য একটি নতুন সরঞ্জাম উপলব্ধ। আপনি এটি মেনু: ফাইল | এর মাধ্যমে ব্যবহার করতে পারেন জিপ ফাইলে রফতানি করুন…

আপনি কীভাবে একটি অ্যান্ড্রয়েড অ্যাপ্লিকেশন বানাবেন সে সম্পর্কে ব্লগ পোস্ট থেকে আপনি কীভাবে আমাদের লাভ ক্যালকুলেটরের জন্য একটি Android প্রকল্প রপ্তানি করতে পারেন তার একটি উদাহরণ এখানে।
প্রথমে ফাইল মেনু থেকে জিপ ফাইলে রফতানি চয়ন করুন:
একটি অ্যান্ড্রয়েড প্রকল্প রফতানি করুন - জিপে রফতানি করুন
এর পরে, গন্তব্য এবং ফাইলের নাম চয়ন করুন:
একটি অ্যান্ড্রয়েড প্রকল্প রফতানি করুন - গন্তব্য চয়ন করুন
আপনার যা করতে হবে তা হ'ল আপনার জিপ ফাইলটি ভাগ করে নেওয়া।

# ম্যানুয়ালি একটি অ্যান্ড্রয়েড স্টুডিও প্রকল্প রফতানি করুন
আমরা এখন বলতে পারি যে কোনও প্রকল্পকে ম্যানুয়ালি রফতানি করা আমাদের প্রকল্পগুলি রফতানির পুরানো উপায়। আসলে, অ্যান্ড্রয়েড স্টুডিওতে কোনও সরঞ্জাম না থাকায় অ্যানড্রইড স্টুডিওর (৩.০ এর আগে) পুরানো সংস্করণগুলির মধ্যে ম্যানুয়াল রফতানি ছিল একমাত্র উপায় the এর পিছনে যুক্তি আরও ভালভাবে বুঝতে আপনার জন্য আমরা একটি উইন্ডোজ এবং ম্যাক সংস্করণ প্রস্তুত করেছি।

# কীভাবে একটি অ্যান্ড্রয়েড স্টুডিও প্রকল্প রফতানি করা যায় এবং উইন্ডোজে একটি জিপ ফাইল তৈরি করা যায়
 
# উইন্ডোজে অ্যান্ড্রয়েড স্টুডিও প্রকল্প ফোল্ডারটি সন্ধান করুন
উইন্ডোজ এবং ম্যাকের উপর ভিউগুলি কিছুটা আলাদা this তাই আপনার জন্য আমাদের উভয় স্ক্রিনশট রয়েছে। এই পদক্ষেপগুলি উইন্ডোজের জন্য

প্রকল্প সরঞ্জাম উইন্ডোতে, আপনি নির্বাচিত ভিউ মোড অনুযায়ী আপনার সাধারণত দুটি উপায় থাকে। আপনি যদি প্রকল্পের ভিউতে থাকেন তবে অ্যাপের নাম তালিকার প্রথম আইটেম। অ্যান্ড্রয়েড ভিউতে “অ্যাপ্লিকেশন” প্রথম আইটেম। নীচের দুটি বিকল্প দেখুন:

আপনার প্রকল্পের সমস্ত ফাইল সহ একটি ফোল্ডার সন্ধান করতে অ্যাপ্লিকেশন নাম বা "অ্যাপ" এ ডান ক্লিক করুন।

উইন্ডোজে, আপনার কাছে "এক্সপ্লোরার-এ দেখান" বিকল্পটি রয়েছে (ম্যাকোজে এটি "ফাইন্ডারে অনুসন্ধানকারী")।


# উইন্ডোজে একটি জিপ ফাইল (একটি অ্যান্ড্রয়েড স্টুডিও প্রকল্পের) কীভাবে তৈরি করা যায়

একবার অ্যান্ড্রয়েড স্টুডিও আপনার জন্য ফোল্ডারটি নির্বাচন করে, এটি একটি এক্সপ্লোরার খোলে এবং আপনার প্রকল্প ফোল্ডারের মধ্যে একটি ফোল্ডার নির্বাচন করে। একটি জিপ তৈরি করতে আপনাকে এটিতে ডান ক্লিক করতে হবে এবং নির্বাচন করুন: "প্রেরণ / সংকুচিত (জিপড) ফোল্ডার"।

একটি অ্যান্ড্রয়েড প্রকল্প রফতানি করুন - সংকুচিতকে প্রেরণ করুন

এটির সাথে, আপনি একটি ".zip" ফাইল পাবেন যা আপনি নিজের সাথে নিতে পারেন, মেল পাঠাতে, ভাগ করতে পারেন ... আপনি জিড্রাইভার, ড্রপবক্স, ওয়ানড্রাইভ বা অন্য কোনও ধরণের ক্লাউড ড্রাইভও ব্যবহার করতে পারেন।

কীভাবে একটি অ্যান্ড্রয়েড স্টুডিও প্রকল্প রফতানি করতে এবং ম্যাকটিতে জিপ তৈরি করা যায়


প্রজেক্ট সরঞ্জাম উইন্ডোতে, আপনি নির্বাচিত ভিউ মোড অনুযায়ী আপনার সাধারণত দুটি উপায় থাকে। আপনি যদি প্রকল্প ভিউতে থাকেন তবে অ্যাপের নাম তালিকার প্রথম আইটেম। অ্যান্ড্রয়েড ভিউতে “অ্যাপ্লিকেশন” প্রথম আইটেম। নীচের দুটি বিকল্প দেখুন:

আপনার প্রকল্পের সমস্ত ফাইল সহ একটি ফোল্ডার সন্ধান করতে অ্যাপ্লিকেশন নাম বা "অ্যাপ" এ ডান ক্লিক করুন। প্রসঙ্গ মেনু থেকে ফাইন্ডারে প্রকাশিত ব্যবহার করুন (অ্যাপ ফোল্ডারে ডান ক্লিক করুন)
MacOS এ জিপ - ফাইন্ডারে প্রকাশ করুন

একবার অ্যান্ড্রয়েড স্টুডিও আপনার জন্য ফাইলগুলি সন্ধান করে এবং আপনার জন্য অনুসন্ধানকারী খোলে, প্রসঙ্গ মেনু থেকে সংক্ষেপ "..." বিকল্পটি চয়ন করুন। এটি আপনার জন্য একটি জিপ ফাইল তৈরি করে।

রফতানি প্রকল্পের আকার হ্রাস করতে ফোল্ডারটি সাফ করুন

মুখ্য ফোল্ডার ফাইলগুলি আপনি মুছতে পারেন: আকার হ্রাস করতে। অ্যাপ ফোল্ডার ফাইলগুলি আপনি মুছতে পারেন: অ্যাপ ফোল্ডার ফাইলগুলি সরান। সাধারণ প্রকল্পগুলির জন্য আপনি প্রকল্পের জিপ আকারকে কিছুটা হ্রাস করেন, উদাহরণস্বরূপ: 5.2MB -> 0.4MB

আরও উন্নত ব্যবহারকারীদের জন্য আপনি এর দৈর্ঘ্য হ্রাস করতে আপনার জিপ ফাইলটি পরিষ্কার করতে পারেন। প্রথম স্থানে, আপনি "বিল্ড" ফোল্ডারগুলি সরান। প্রথমটি মূল ফোল্ডারে এবং দ্বিতীয়টি "অ্যাপ" ফোল্ডারে। এছাড়াও, আপনি .iml ফাইলগুলিও সরিয়ে ফেলতে পারেন (এই ফাইলগুলি কম্পিউটারের সাথে সম্পর্কিত পাথের সাথে যুক্ত এবং অন্যান্য কম্পিউটারে স্বয়ংক্রিয়ভাবে তৈরি করা হয়)।

 

# উপসংহার

অ্যান্ড্রয়েড স্টুডিও প্রজেক্টটি কীভাবে রফতানি করতে হবে তা জেনে রাখা যখন আপনাকে মেইলের মাধ্যমে অন্য কম্পিউটারে ফাইল এবং কোড সরানো বা অন্য কোনও উপায়ে ভাগ করা প্রয়োজন। তদুপরি, এর মতো প্রকল্পগুলি ভাগ করে নেওয়া নতুনদের জন্য সহযোগিতার এক সঠিক উপায় হতে পারে। সমানভাবে গুরুত্বপূর্ণ, একটি বৃহত প্রকল্পে কাজ করার সময় প্রকল্পগুলি ভাগ করে নেওয়ার আরও ভাল উপায় রয়েছে, আপনি বেশিরভাগই জিআইটির মতো সংস্করণ নিয়ন্ত্রণ ব্যবস্থা ব্যবহার করেন (অগ্রাধিকার হিসাবে বিটবাকেট, গিটহাব, ... বা স্থানীয় প্রয়োজন মতো স্থানীয় মেঘ সমাধানে; সরল গিট বা এর মতো কিছু) গিটল্যাব ।

উপসংহারে, একটি প্রকল্প রফতানি করা এবং জিআইটি ব্যবহার করা আপনার অ্যান্ড্রয়েড বিকাশকারী হওয়ার জন্য প্রয়োজনীয় দক্ষতার মধ্যে একটি, অ্যান্ড্রয়েড বিকাশকারী হওয়ার জন্য প্রয়োজনীয় সমস্ত দক্ষতা সম্পর্কে আমাদের ব্লগ পোস্টে আরও পড়ুন।

কোড সহ মজাদার কোডিং সফ্টওয়্যার সমাধান করুন।
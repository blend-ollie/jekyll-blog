---
layout: post
title:  "Apache Cordova"
date:   2020-03-13 09:55:00 +0000
categories: knowledge-sharing
---

### Overview

Cordova is an open-source mobile development framework. It allows you to use HTML5 to build mobile apps without having to use the mobile platforms native language.

For example, native iOS apps are built using Objective-C or Swift. Cordova allows you to build an app in HTML5, CSS, Javascript, etc. without having to use the iOS native languages and then compile the app to a device.

Another great feature when using Cordova is that you can compile to multiple platforms (e.g. iOS, Android, Windows) and work in only one codebase. It's really simple to do this too. Once you've created the app, if you wanted to compile to iOS, you'd run `cordova platform add ios`, or compile to Android with `cordova platform add android`.

### Examples of use

I worked as a frontend developer at Oi Digital, whose clients were in the pharmaceutical industry. An example of a project where I used Cordova was the PainDetect App.

The client asked us to build an app that would be available in both the Apple App and Google Play Stores. After conducting some research, I found that we could easily build a HTML5 app which could be compiled to both iOS and Android using a framework called Cordova. As very few people in the agency had any experience using Objective-C/Swift (iOS) or Java (Android), this seemed like the perfect tool.

So I created a HTML5 app and once completed, I used Cordova to compile it to both iOS and Android. This meant I could work in one codebase and not have to worry about changing specific code to work in either native language.

### How to install Cordova

There are plenty of tutorials on how to install Cordova, the best one being on the actual Cordova site ([Create your first Cordova app][cordova-create-app]). But to give you a brief overview, here's how to quickly create a Cordova app:

#### 1. Install Node.js
Download the latest version of Node.js [here][node-install]

#### 2. Install Cordova
Install Cordova using npm:

{% highlight console %}
$ sudo npm install -g cordova
{% endhighlight %}

#### 3. Create an app
Go to the directory where you maintain your source code and using the Cordova CLI, create a Cordova project named HelloWorld in a directory named hello:

{% highlight console %}
$ cordova create hello com.yourname.hello HelloWorld
{% endhighlight %}

#### 4. Add platforms
Go to the directory that you've just created:

{% highlight console %}
$ cd hello
{% endhighlight %}

And add the platforms that you wish to compile your code too e.g. iOS:

{% highlight console %}
$ cordova platform add ios
{% endhighlight %}

#### 5. Build the app

Run the following command to build to all platforms:

{% highlight console %}
$ cordova build
{% endhighlight %}

Or you can build to a specific platform by running the following:

{% highlight console %}
$ cordova build ios
{% endhighlight %}

You'll need to run this command each time you want to compile your codebase to your platforms.


[cordova-create-app]: https://cordova.apache.org/docs/en/latest/guide/cli/index.html
[node-install]: https://nodejs.org/en/download/
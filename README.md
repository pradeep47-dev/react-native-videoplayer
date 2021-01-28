Android Videos Player
=======================================
Helper View to play videos using Facebook Embedded Videos API

Resources : 
[https://developers.facebook.com/docs/plugins/embedded-video-player/api](https://developers.facebook.com/docs/plugins/embedded-video-player/api)

How to use
----------
Gradle:

```gradle
 repositories {
  jcenter()
  maven {
    url 'https://dl.bintray.com/zeattacker/maven/'
  }
}

dependencies {
  compile 'com.ramazeta:fb-android-videoplayer:0.0.2'
}
```

Maven:

```xml
<dependency>
  <groupId>com.ramazeta</groupId>
  <artifactId>fb-android-videoplayer</artifactId>
  <version>0.0.2</version>
  <type>pom</type>
</dependency>
```


How to use FB Video Player
--------------------------
Detail of usage : [MainActivity.java][1].

Example :
* XML

```xml
    <com.ramazeta.fbvideoplayer.FacebookPlayer
        android:id="@+id/fbPlayerView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

```

* JAVA

```java
        // get id from XML
        FacebookPlayer fbPlayerView = (FacebookPlayer) findViewById(R.id.fbPlayerView);

       // auto heights
        fbPlayerView.setAutoPlayerHeight(this);
        // init with app_id and video_url
        fbPlayerView.initialize("app_fb_id", "video_url");
        
        //play video
        fbPlayerView.play();
        
        //pause video
        fbPlayerView.pause();
        
        //mute video
        fbPlayerView.mute();
        
        //unmute video
        fbPlayerView.unmute();
        

```


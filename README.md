Android-Learning-Note
=====================

這個筆記大部分都是由這篇`A Deep Dive into Open Source Android Development`整理出來的，後續會慢慢整理這些Open Source怎麼安裝與使用的筆記，如果有錯誤在請大家指正。

* [Youtube]
* [Slide]

[Youtube]: http://www.youtube.com/watch?v=gwB8xkTckKc&hd=1http://taybenlor.com/2013/05/21/designing-for-ios.html
[Slide]: http://www.slideshare.net/wuman/a-deep-dive-into-open-source-android-development


#UI and Compatibility
##ActionBarSherlock

* 網址 - <http://actionbarsherlock.com/>
* 描述 - Action bar是android 3.0才開始有的功能，而ActionBarSherlock則是把該功能支援到先前的Android版本。
    * Split Action Bar - 當你的actionBarButton太多的時候，會自動轉成tab
    * Contextual Action Bars - 根據User的動作(狀態)，改變actionBar給的樣式

##HoloEverywhere
* 網址 - <https://github.com/Prototik/HoloEverywhere>
* 描述 - Holo是Jelly Bean才開始有的功能，這邊讓先前版本也支援Holo theme

##NineOldAndroids
* 網址 - <http://nineoldandroids.com>
* 描述 -原本3.0才有的Animation,支援先前版本


``ObjectAnimator.foFloat(myObject, "translationY", -myObject.getHeight()).start();``


##UnifiedPreference
* 網址 - <https://github.com/saik0/UnifiedPreference#how-to-use>
* 描述 -支援3.0之前有設定頁

##Android Support Package
Google自己提供的向下相容元件

* Fragment
* ViewPager, PagerTileStrip, PageTabStrip
* Notification - 更多樣式的notification
* Loader
* LruCache

##Android MenuDrawer
* 網址 - <https://github.com/SimonVT/android-menudrawer>
* 描述 - 用貝氏曲線實作的Menu

##SimpleMenuDrawer
* 網址 - <https://github.com/adamrocker/simple-side-drawer>
* 描述 - 簡單的.jar檔使用，非常輕量化，支援左右menu，


```java
在Activity.onCreate 設定物件
mSlidingMenu = new SimpleSideDrawer( this );
mSlidingMenu.setLeftBehindContentView( R.layout.behind_menu_left );

//宣告右側menu
mSlidingMenu.setRightBehindContentView( R.layout.behind_menu_right )

//開關menu
mSlidingMenu.toggleDrawer();
```

##Android-PullToRefresh
* 網址 - <https://github.com/chrisbanes/Android-PullToRefresh>

##Polaris
* 網址 - <https://github.com/cyrilmottier/Polaris>
* 描述 - map用的

##Crouton
* 網址 - <https://github.com/neofoniemobile/Crouton>
* 描述 - 類似toast的錯誤訊息，but inside app content.

##Android-Query
* 網址 - <https://code.google.com/p/android-query/>
* 描述 - Enables easier UI manipulation via method chaining, 就像jQuery的chain


#Caching and Network
##DisLruCache
* 描述 - 本來只有3.0以後才有

##Two Level Lru Cache
* 網址 - <http://wuman.github.io/TwoLevelLruCache/>

##Android Image Loader
* 網址 - <http://wuman.github.io/AndroidImageLoader/>

##Http Response Cache
* 網址 - <https://github.com/candrews/HttpResponseCache>

##Http-Request
* 網址 - <https://github.com/kevinsawicki/http-request>

* 描述 - HttpURLConnection 超難用

``HttpRequest.get("http://google.com").receive(System.out);``




#Concurrency and Communication
##Tape
* 網址 - <http://square.github.io/tape/>
* 描述 - 把task queue放到disk裡面，保證任務會執行

##Otto
* 網址 - <http://square.github.io/otto/>
* 描述 - An event bus forked from `EventBus` of Google Guava targeting the Android Platform.
* 範例 - <http://asherson.wordpress.com/2013/02/20/otto-event-bus-for-android/>

#Data Representation and Processing
##GSON
* 網址 - <https://code.google.com/p/google-gson/>
* 描述 - Java object <--> Json object

##Jackson JSON Processor
* 網址 - <http://wiki.fasterxml.com/JacksonHome>
* 描述 - Facebook有再用，聽說比原生快很多

##Json-Path
* 網址 - <https://code.google.com/p/json-path/>
* 描述 - 類似Css的selector

``String author = JsonPath.read(json, "$.store.book[1].author);``

##jOOX - Java Object Oriented XML
* 網址 - <https://github.com/jOOQ/jOOX>

##JSoup
* 網址 - <http://jsoup.org/>

##OrmLite
* 網址 - <http://ormlite.com/>
* 描述 - 把物件轉成SQlite

##Google Guava
* 網址 - <https://code.google.com/p/guava-libraries/>


#Dependency Injection
##Android Annotations
* 網址 - <http://androidannotations.org/>

##RoboGuice
* 網址 - <https://github.com/roboguice/roboguice>
* 描述 - 比較多人用

##Dagger
* 網址 - <http://square.github.io/dagger/>
* 描述 - 在compile-time去檢查dependency injection (binding validation) for Android

#Testing
##Android Test Framework
* 網址 - <http://developer.android.com/tools/testing/index.html>
* AndroidTestCase
* Instrumentation
* monkey

##Robotium
* 網址 - <https://code.google.com/p/robotium/>
* <http://www.vogella.com/articles/AndroidTesting/article.html>
* 描述 - 黑盒子測試，不需要知道程式怎麼寫的
* 可以側兩個activity之間的互動

##Mochito
* 網址 - <https://code.google.com/p/mockito/>
* 描述 - 做一個假的物件取代

##Robolectric
* 網址 - <http://pivotal.github.io/robolectric/>
* 描述 - 測試非ui部分在jvm上面跑

#User Feedback
##ACRA
* 網址 - <http://acra.ch/>
* 描述 - 詳細的錯誤報告資訊

##BugSense/Crittercism
* 網址 - <http://www.bugsense.com/docs/android#acra>
* 描述 - 把Bug彙總成issue

##Google Analytics for Android
* 網址 - <https://developers.google.com/analytics/devguides/collection/android/v2/>

#Bootstrap Project Generator
##Android Bootstrap
* 網址 - <http://www.androidbootstrap.com/>

##AndroidKickStartR
* 網址 - <http://androidkickstartr.com>


#Tools
##Android Asset Studio
* 網址 - <http://android-ui-utils.googlecode.com/hg/asset-studio/dist/index.html>
* 描述 - 產生圖

##Subtle Patterns
* 網址 - <http://subtlepatterns.com/>
* 描述 - 背景圖材質

##Charles
* 網址 - <http://www.charlesproxy.com/>
* 描述 - 看Http的api

#Others
* App Dev Wiki <http://appdevwiki.com/wiki/show/HomePage>
* The Ultimate Android Library<http://www.theultimateandroidlibrary.com/>
* AppBrain Android Developer Tools <http://www.appbrain.com/stats/libraries/dev>

Library Project Directory Structure

* org.apche.maven.archetypes/maven-archetype-quickstart
* de.akquient.android.archetypes/androi-release


#Why open source?
##Code Quality and Style

##Inclusion of Examples

##Documentation
* maven-javadoc-plogin

##Continuous Integration

##Site Setup
* 網址 - <http://documentup.com/>

##Downloadable Published Packages
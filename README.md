FABProgressCircle
=================
Android library to provide a material progress circle around your FloatingActionButton. This component is **compatible with any existent FAB**.

[![FABProgressCircle video](http://img.youtube.com/vi/sP-Ng7e8k6g/0.jpg)](http://www.youtube.com/watch?v=sP-Ng7e8k6g)
 
`FABProgressCircle` follows material guidelines at 100%. Links to Google samples of this behavior:

* [Video sample from Google][material-sample-1]
* [Another video sample from Google][material-sample-2]

How to use
----------
You can use the `FABProgressCircle` to wrap any existent FAB. Here it is an example wrapping the Google FloatingActionButton from the brand
new [Design Support Library][google-design-support].
```xml
<com.github.jorgecastilloprz.FABProgressCircle
    android:id="@+id/fabProgressCircle"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    >

  <android.support.design.widget.FloatingActionButton
      android:id="@+id/fab"
      android:layout_width="wrap_content"
      android:layout_height="wrap_content"
      android:src="@drawable/ic_upload"
      app:rippleColor="@color/fab_ripple"
      app:elevation="@dimen/fab_elevation"
      app:borderWidth="0dp"
      />

</com.github.jorgecastilloprz.FABProgressCircle>
```
When the `FloatingActionButton` gets clicked, the progress circle will appear and the animation will start automatically. The progress animation will be
indeterminate at the beginning, as you can't really know how long is the asynchronous call going to take to complete.

To play the completing animation, you will need to call
```java
fabProgressCircle.beginStopAnimation();
```

Mini Size
---------
Mini size is totally supported, so feel free to use the `app:fabSize="mini"` custom attribute on the Google FAB, or the corresponding `mini` custom
attribute of the fab library you are using.

Contributions
-------------
Feel free to send `Pull Requests` to this repository if you feel that it lacks some functionality. I will be pleased to accept or discuss about them.
However, **Material Design guidelines will be required**.

Developed By
------------
* Jorge Castillo Pérez - <jorge.castillo.prz@gmail.com>

<a href="https://www.linkedin.com/in/jorgecastilloprz">
  <img alt="Add me to Linkedin" src="https://github.com/JorgeCastilloPrz/EasyMVP/blob/master/art/linkedin.png" />
</a>

License
-------

    Copyright 2015 Jorge Castillo Pérez

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.

[material-sample-1]: http://material-design.storage.googleapis.com/publish/material_v_4/material_ext_publish/0B0NGgBg38lWWbTlSaHdQZEMtalk/components-progressactivity-typesofindicators-061101_Circular_Aspirational_xhdpi_002.webm
[material-sample-2]: http://material-design.storage.googleapis.com/publish/material_v_4/material_ext_publish/0B6Okdz75tqQsa0QwVnd6NVlvWkk/components-progressactivity-typesofindicators-Circular_wFab_xhdpi_003.webm
[google-design-support]: http://developer.android.com/tools/support-library/features.html#design
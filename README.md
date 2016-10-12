# psandroidfundastyletheme
##3. Styling Views
###1 Overview
```
StateListDrawable
ColorStateList
```

###2 Project Setup and Overview of Default Values Directory Files
Empty Activity->activity_main.xml:  
TextView layout_gravity vs LinearLayout center.
```
<LinearLayout android:gravity="center">
  <TextView:layout_gravity="center_horizontal"/>

</LinearLayout>
```

###3 Defining Styles for Views
```
<TextView android:fontFamily="monospace" android:textStyle="italic"/>
```

###4 Defining Styles for Views Continued
```
<TextView style="@style/AppSmallText"
```
styles.xml, we can define font attribute in it
```
<style name="AppSmallText">
  <item name="android:fontFamily">monospace</item>
  <item name="android:textColor">#616161</item>
</style>
```

###6 Selector: Styling Views Based on Their State
StateListDrawable (change button bg color)
ColorStateList (change text color)

###7

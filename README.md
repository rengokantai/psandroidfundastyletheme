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

###7 Implementing Selector Using StateListDrawable
create button_background_selector.xml
```
<selector>
<item android:state_pressed="true" android:drawable="@drawable/pressed"/>   <!--omit extension, such as jpeg-->
<item android:drawable="@drawabledefault"/>  <!-- default case-->
</selector>
```
activity_main.xml
```
<Button android:background="@drawable/button_background_selector"../>
```
###8 Code Snippet: StateListDrawable Selector
other possible states:  
state_focused  
state_hovered  

###9 Implementing Selector Using ColorStateList
create color/button_color_selector.xml
```
<selector xmlns:...
  <item android:state_pressed="true" android:color="#000"/>
  <item android:color="#FFF"/>
</selector>
```
activity_mail.xml
```
<Button android:textColor="@color/button_color_selector"..
```
###10 Applying Gradient and Shadow to the Views
MainActivity.java
```
TextView txvGradient = (TextView)findViewById(R.id.txvGradient);
//new LinearGradient(x1,y1,x2,y2,color0,color1,TileMode tile)
LinearGradient linearGradient = new LinearGradient(0,0,txvGradient.getTextSize(),0,Color.GRAY,COlor.RED,TileMode.MIRROR)

txvGradient.getPaint().setShader(linearGradient);
```

shadow
```
<TextView android:shadowDx="100" android:shadowDy="100" android:shadowRadius="10"/>
```

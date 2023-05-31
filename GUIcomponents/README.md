# Ex.No: 2 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project. 
Step 2: Then type the Application name as HelloWorld and click Next. 
Step 3: Then select the Minimum SDK as shown below and click Next. 
Step 4: Then select the Empty Activity and click Next. Finally click Finish. 
Step 5: Design layout in activity_main.xml 
Step 6: Display message give in MainActivity file. 
Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “GUIcomponent”.
Developed by:Vaishnavi M
Registeration Number :212221040175
*/
```
## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android"
xmlns:app="http://schemas.android.com/apk/res-auto"
xmlns:tools="http://schemas.android.com/tools"
android:layout_width="match_parent"
android:layout_height="match_parent"
tools:context=".MainActivity">
 <TextView
 android:id="@+id/textView"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_margin="30dp"
 android:layout_marginTop="296dp"
 android:gravity="center"
 android:text="Hello World!"
 android:textSize="25sp"
 android:textStyle="bold"
 app:layout_constraintBottom_toTopOf="@+id/button1"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.266"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 tools:ignore="MissingConstraints" />
 <Button
 android:id="@+id/button1"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_margin="20dp"
 android:layout_marginBottom="48dp"
 android:gravity="center"
 android:text="Change font size"
 android:textSize="25sp"
 app:layout_constraintBottom_toTopOf="@+id/button2"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.25"
 app:layout_constraintStart_toStartOf="parent"
 tools:ignore="MissingConstraints" />
 <Button
 android:id="@+id/button2"
 android:layout_width="match_parent"
 android:layout_height="wrap_content"
 android:layout_margin="20dp"
 android:gravity="center"
 android:text="Change color"
 android:textSize="25sp"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.4"
 app:layout_constraintStart_toStartOf="parent"
 tools:ignore="MissingConstraints" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java
```
package com.example.ex2;
import androidx.appcompat.app.AppCompatActivity;
import android.graphics.Color;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;
public class MainActivity extends AppCompatActivity {
 int ch=1;
 float font=30;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 final TextView t = (TextView) findViewById(R.id.textView);
 Button b1 = (Button) findViewById(R.id.button1);
 b1.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View v) {
 t.setTextSize(font);
 font = font + 5;
 if (font == 50)
 font = 30;
 }
 });
 Button b2 = (Button) findViewById(R.id.button2);
 b2.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View v) {
 switch (ch) {
 case 1:
 t.setTextColor(Color.RED);
 break;
 case 2:
 t.setTextColor(Color.GREEN);
 break;
 case 3:
 t.setTextColor(Color.BLUE);
 break;
 case 4:
 t.setTextColor(Color.CYAN);
 break;
 case 5:
 t.setTextColor(Color.YELLOW);
 break;
 case 6:
 t.setTextColor(Color.MAGENTA);
 break;
 }
 ch++;
 if (ch == 7)
 ch = 1;
 }
 });
 } }
```
## OUTPUT
![WhatsApp Image 2023-05-30 at 14 13 13 (2)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/957f1012-7919-4f46-948d-44cc7b7dd8c3)
![WhatsApp Image 2023-05-30 at 14 13 13](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/41b5b123-d241-42d7-9e51-70fa4e3ced32)
![WhatsApp Image 2023-05-30 at 14 13 14](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/7d38b0ab-808e-4467-8a90-9239ae15410a)
![WhatsApp Image 2023-05-30 at 14 13 09](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/6f3abf72-78b9-4bbf-b031-18310e4f4893)

## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.



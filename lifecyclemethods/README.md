# Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.


## AIM:

To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “Hello World”.
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
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="Hello World!"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 android:textSize="25dp"/>
</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java
```
package com.example.ex1;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.widget.Toast;
public class MainActivity extends AppCompatActivity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 Toast.makeText(this, "onCreate Called", Toast.LENGTH_SHORT).show();
 }
 @Override
 protected void onRestart(){
 Toast.makeText(this, "onRestart Called", Toast.LENGTH_SHORT).show();
 super.onRestart();
 }
 @Override
 protected void onStart(){
 Toast.makeText(this, "onStart Called", Toast.LENGTH_SHORT).show();
 super.onStart();
 }
 @Override
 protected void onResume(){
 Toast.makeText(this, "onResume Called", Toast.LENGTH_SHORT).show();
 super.onResume();
 }
 @Override
 protected void onPause(){
 Toast.makeText(this, "onPause Called", Toast.LENGTH_SHORT).show();
 super.onPause();
 }
 @Override
 protected void onStop(){
 Toast.makeText(this, "onStop Called", Toast.LENGTH_SHORT).show();
 super.onStop();
 }
 @Override
 protected void onDestroy(){
 Toast.makeText(this, "onDestroy Called", Toast.LENGTH_SHORT).show();
 super.onDestroy();
 } }
```
## OUTPUT
![2023-05-31 (18)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/2b0265ca-f164-41a4-9d5f-4628ae552b3d)
![2023-05-31 (17)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/ed342a3a-05e9-4e7c-8566-baa421d1fc44)
![2023-05-30 (7)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/204a6d72-de3c-42f5-9f1a-36083305407e)
![2023-05-30 (6)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/f96eea10-caff-436a-ba95-b13a001e152f)
![2023-05-30 (4)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/501f935e-cfcb-4fba-8479-c9c27df7ac2c)
![2023-05-30 (3)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/f1d42bc0-e581-453e-b0a0-a720d9c3b342)

## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.

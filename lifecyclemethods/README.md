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

## OUTPUT

![2023-05-31 (17)](https://github.com/suryacse05/Mobile-Application-Development/assets/135130074/6af28cc5-f7c4-41d7-a550-854fc73ba18d)

![2023-05-31 (18)](https://github.com/suryacse05/Mobile-Application-Development/assets/135130074/514d16ff-0542-41da-b2a5-adcf1ddefdf5)

![2023-05-30 (3)](https://github.com/suryacse05/Mobile-Application-Development/assets/135130074/9ad28811-4e27-4965-b367-468207f7e9ba)

![2023-05-30 (4)](https://github.com/suryacse05/Mobile-Application-Development/assets/135130074/a6b677b7-3f7b-4189-b35f-72c2c3036b65)

![2023-05-30 (6)](https://github.com/suryacse05/Mobile-Application-Development/assets/135130074/2687d593-f969-4a89-831e-075f52a20b06)

![2023-05-30 (7)](https://github.com/suryacse05/Mobile-Application-Development/assets/135130074/f084ba3d-2073-40eb-9c6f-414f648a6e41)

## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.

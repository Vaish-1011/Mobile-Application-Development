# Ex.No:4 To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## AIM:

To create a two screens , first screen will take one number input from user. After click on Factorial button, second screen will open and it should display factorial of the same number using Explicit Intents.


## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project. 
Step 2: Then type the Application name as HelloWorld and click Next. 
Step 3: Then select the Minimum SDK as shown below and click Next. 
Step 4: Then select the Empty Activity and click Next. Finally click Finish. 
Step 5: Design layout in activity_main.xml 
Step 6: Display message give in MainActivity file. 
Step 7: Save and run the application
## PROGRAM:
```
/*
Program to print the text “ExplicitIntent”.
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
 android:id="@+id/maintxt"
 android:layout_width="317dp"
 android:layout_height="38dp"
 android:layout_marginTop="152dp"
 android:text="FACTORIAL CALCULATOR"
 android:textAlignment="center"
 android:textColor="@color/black"
 android:textSize="25sp"
 app:layout_constraintBottom_toTopOf="@+id/text1"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent" />
 <TextView
 android:id="@+id/text1"
 android:layout_width="156dp"
 android:layout_height="32dp"
 android:layout_marginTop="252dp"
 android:text="Enter a Number"
 android:textColor="@color/black"
 android:textSize="20sp"
 app:layout_constraintBottom_toTopOf="@+id/n1"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.58"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.403" />
 <EditText
 android:id="@+id/n1"
 android:layout_width="50dp"
 android:layout_height="50dp"
 android:layout_alignRight="@+id/text1"
 android:layout_marginTop="340dp"
 android:textColor="#EA80FC"
 app:layout_constraintBottom_toTopOf="@+id/btn1"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent" />
 <Button
 android:id="@+id/btn1"
 android:layout_width="164dp"
 android:layout_height="51dp"
 android:background="#F44336"
 android:text="Calculate"
 android:textColor="@color/white"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.497"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.714" />
 <TextView
 android:id="@+id/resum"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_marginLeft="150dp"
 tools:ignore="MissingConstraints" />
</androidx.constraintlayout.widget.ConstraintLayout>
```

## MainActivity.java
```
package com.example.explicitintent;
import androidx.appcompat.app.AppCompatActivity;
import android.annotation.SuppressLint;
import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;
public class MainActivity extends AppCompatActivity {
 public static String Send_Result;
 EditText num1;
 TextView txtrslt;
 Button btn;
 double n,i=1,fact=1;
 @SuppressLint("MissingInflatedId")
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 num1 = (EditText) findViewById(R.id.n1);
 txtrslt = (TextView) findViewById(R.id.resum);
 btn = (Button) findViewById(R.id.btn1);
 btn.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View view) {
 n = Double.parseDouble(num1.getText().toString());
 while (i<=n)
 {
 fact=fact*i;
 i++;
 }
 String message = Double.toString(fact);
 Intent myIntent = new Intent(MainActivity.this, MainActivity2.class);
 myIntent.putExtra(Send_Result, message);
 startActivity(myIntent);
 }
 });
 } }
````
## activity_main2.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout 
xmlns:android="http://schemas.android.com/apk/res/android"
 xmlns:app="http://schemas.android.com/apk/res-auto"
 xmlns:tools="http://schemas.android.com/tools"
 android:layout_width="match_parent"
 android:layout_height="match_parent"
 tools:context=".MainActivity2">
 <TextView
 android:id="@+id/textView"
 android:layout_width="137dp"
 android:layout_height="47dp"
 android:text="RESULT : "
 android:textColor="@color/black"
 android:textSize="34sp"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.318" />
 <TextView
 android:id="@+id/reslt"
 android:layout_width="96dp"
 android:layout_height="70dp"
 android:text="00.00"
 android:textColor="#F44336"
 android:textSize="38sp"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.498"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.465" />
</androidx.constraintlayout.widget.ConstraintLayout>
```

## MainActivity2.java
```
package com.example.explicitintent;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.widget.TextView;
public class MainActivity2 extends AppCompatActivity {
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main2);
 Intent intent = getIntent();
 M VAISHNAVI 212221040175
 String message = intent.getStringExtra(MainActivity.Send_Result);
 TextView textView = findViewById(R.id.reslt);
 textView.setText(message);
 } }
````
## OUTPUT
![2023-05-31 (11)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/a84350dd-a862-4cc4-a007-a40f2c2f1cfa)
![2023-05-31 (12)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/e17b44ab-441a-4371-a2fd-704d2048bea5)
![2023-05-31 (13)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/723fe8aa-d016-443c-b072-5005b99154e8)
![2023-05-31 (14)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/8c1808d7-4de1-4cc5-b4e5-e66172e25ed4)
![2023-05-31 (15)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/44c943f3-3c9e-4580-aaaa-bf6afd0bac35)
![2023-05-31 (16)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/930c6731-279b-47b5-8075-f47a3b484697)


## RESULT
Thus a Simple Android Application create a Explicit Intents using Android Studio is developed and executed successfully.




# Ex.No:6 Design an android application Send SMS using Intent.


## AIM:

To create and design an android application Send SMS using Intent using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as smsintent and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Send SMS and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to create and design an android application Send SMS using Intent.
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
 <EditText
 android:id="@+id/number"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:ems="10"
 android:inputType="phone"
 android:text="Phone Number"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.497"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.307" />
 <EditText
 android:id="@+id/message"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:layout_marginTop="36dp"
 android:ems="10"
 android:inputType="text"
 android:text="Type Message"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.497"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toBottomOf="@+id/number"
 app:layout_constraintVertical_bias="0.032" />
 <Button
 android:id="@+id/send"
 android:layout_width="100dp"
 android:layout_height="57dp"
 android:text="SEND"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.472"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.606" />
 <TextView
 android:id="@+id/textView2"
 android:layout_width="wrap_content"
 android:layout_height="wrap_content"
 android:text="SEND SMS"
 android:textColor="@color/black"
 android:textSize="24sp"
 app:layout_constraintBottom_toBottomOf="parent"
 app:layout_constraintEnd_toEndOf="parent"
 app:layout_constraintHorizontal_bias="0.498"
 app:layout_constraintStart_toStartOf="parent"
 app:layout_constraintTop_toTopOf="parent"
 app:layout_constraintVertical_bias="0.121" />
</androidx.constraintlayout.widget.ConstraintLayout>
```

## MainActivity.java
```
package com.example.smsintent;
import androidx.appcompat.app.AppCompatActivity;
import android.Manifest;
import android.content.pm.PackageManager;
import android.os.Build;
import android.os.Bundle;
import android.telephony.SmsManager;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;
public class MainActivity extends AppCompatActivity {
 private EditText number, message;
 private Button send;
 @Override
 protected void onCreate(Bundle savedInstanceState) {
 super.onCreate(savedInstanceState);
 setContentView(R.layout.activity_main);
 number = findViewById(R.id.number);
 message = findViewById(R.id.message);
 send = findViewById(R.id.send);
 send.setOnClickListener(new View.OnClickListener() {
 @Override
 public void onClick(View view) {
 if (Build.VERSION.SDK_INT >= Build.VERSION_CODES.M) {
 if (checkSelfPermission(Manifest.permission.SEND_SMS) ==
 PackageManager.PERMISSION_GRANTED) {
 sendSMS();
 } else {
 requestPermissions(new String[]{Manifest.permission.SEND_SMS}, 1);
 }
 }
 }
 private void sendSMS() {
 }
 });
 }
 private void sendSMS(){
 String phoneNo = number.getText().toString().trim();
 String SMS = message.getText().toString().trim();
 try {
 SmsManager smsManager = SmsManager.getDefault();
 smsManager.sendTextMessage(phoneNo, null, SMS, null, null);
 Toast.makeText(this, "Message is sent", Toast.LENGTH_SHORT).show();
 } catch (Exception e) {
 e.printStackTrace();
 Toast.makeText(this, "Failed to send message", Toast.LENGTH_SHORT).show();
 }
 }
 }
```
## OUTPUT
![2023-05-31 (23)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/92d21de2-2f45-4beb-8882-6a6ad3eb3c3c)
![2023-05-31 (24)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/2e06736c-1ec4-4c4a-a22a-3536b99d494b)
![2023-05-31 (25)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/1ef083db-d784-4cf0-8e60-25fe611c8ba4)
![2023-05-31 (26)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/4172ca21-f478-4017-b5fd-35ae49782a25)
![2023-05-31 (27)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/bd7a884a-0c3b-4cde-bed6-24953ec9df5c)
![2023-05-31 (30)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/124a1a52-7adc-40d5-a435-506336f3a45b)






## RESULT
Thus a Simple Android Application create and design an android application Send SMS using Intent using Android Studio is developed and executed successfully.

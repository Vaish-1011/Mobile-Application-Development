# Ex.No:10 To create a option menu to display menu items.


## AIM:

To create a option menu to display menu items.
## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.
Step 2: Then type the Application name as “option menu” and click Next. 
Step 3: Then select the Minimum SDK as shown below and click Next.
Step 4: Then select the Empty Activity and click Next. Finally click Finish.
Step 5: Design layout in activity_main.xml.
Step 6: Get contacts details and Display details give in MainActivity file.
Step 7: Save and run the application.. 



## PROGRAM:
```
/*
Program to print the text “optionmenu”.
Developed by:Vaishnavi M
Registeration Number :212221040175
*/
```
## activity_main.xml
```<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
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
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>

```
## MainActivity.java
```
package com.example.optionmenu;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.Menu;
import android.view.MenuInflater;
public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
    @Override
    public boolean onCreateOptionsMenu(Menu menu) {
        MenuInflater m = getMenuInflater();
        m.inflate(R.menu.option,menu);
        return true;
    }
}
```
## option.xml
```
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">
    <item android:title="Item 1" />
    <item android:title="Item 2" />
    <item android:title="Item 3" />
</menu>
```

## OUTPUT
![2023-06-07 (3)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/1f21eb15-2f3d-46e5-8850-44d44bb11dcb)
![2023-06-07 (2)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/05f61cc1-79ec-4e6f-b234-05e707c7d059)
![2023-06-07 (4)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/1b9f2d53-8906-46f6-9969-d472386828a4)
![2023-06-07 (1)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/78df1d90-2275-4020-86e4-08a996457833)


## RESULT
Thus a Simple Android Application to create a option menu to display menu items using Android Studio is developed and executed successfully.



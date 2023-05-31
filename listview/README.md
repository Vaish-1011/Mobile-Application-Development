
# Ex.No:7 Develop an android application to display the place name with image using list view in android studio.


## AIM:

To create and develop the application to display the place name with image using list view in android studio

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as “listview″ and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Get contacts details and Display details give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the list of item.
Developed by:Vaishnavi M
Registeration Number :212221040175
*/
```
## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <ListView
    android:id="@+id/list"
    android:layout_width="409dp"
    android:layout_height="729dp"
    app:layout_constraintBottom_toBottomOf="parent"
    app:layout_constraintEnd_toEndOf="parent"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
## MainActivity.java
```
package com.example.listview;
import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ListView;
import android.widget.Toast;
public class MainActivity extends AppCompatActivity {
    ListView list;
    String[] maintitle ={
            "MERCURY","VENUS",
            "EARTH","MARS",
            "JUPITER","SATURN",
            "URANUS","NEPTUNE"
    };
    Integer[] imgid={
            R.drawable.mercury,R.drawable.venus,
            R.drawable.earth,R.drawable.mars,
            R.drawable.jupiter,R.drawable.saturn,
            R.drawable.uranus,R.drawable.neptune
    };
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        MyListAdapter adapter=new MyListAdapter(this, maintitle,imgid);
        list=(ListView)findViewById(R.id.list);
        list.setAdapter(adapter);
        list.setOnItemClickListener(new AdapterView.OnItemClickListener() {
            @Override
            public void onItemClick(AdapterView<?> parent, View view, int position, long id) {
                if(position == 0) {
                    //code specific to first list item
                    Toast.makeText(getApplicationContext(),"Place Your First Option Code",Toast.LENGTH_SHORT).show();
                }
                else if(position == 1) {
                    //code specific to 2nd list item
                    Toast.makeText(getApplicationContext(),"Place Your Second Option Code",Toast.LENGTH_SHORT).show();
                }
                else if(position == 2) {
                    Toast.makeText(getApplicationContext(),"Place Your Third Option Code",Toast.LENGTH_SHORT).show();
                }
                else if(position == 3) {
                    Toast.makeText(getApplicationContext(),"Place Your Forth Option Code",Toast.LENGTH_SHORT).show();
                }
                else if(position == 4) {
                    Toast.makeText(getApplicationContext(),"Place Your Fifth Option Code",Toast.LENGTH_SHORT).show();
                }
            }
        });
    }

```
## mylist.xml
``<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    xmlns:app="http://schemas.android.com/apk/res-auto">

    <ImageView
        android:id="@+id/icon"
        android:layout_width="60dp"
        android:layout_height="60dp"
        android:padding="5dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.076"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.053" />
    <LinearLayout
        android:id="@+id/linearLayout"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:orientation="vertical"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.382"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.063">

    </LinearLayout>

    <TextView
        android:id="@+id/title"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginLeft="10dp"
        android:layout_marginTop="5dp"
        android:padding="2dp"
        android:text="Medium Text"
        android:textAppearance="?android:attr/textAppearanceMedium"
        android:textColor="#4d4d4d"
        android:textStyle="bold" />
`
</LinearLayout>
```
## MyListAdapter.java
```
package com.example.listview;
import android.app.Activity;
import android.view.LayoutInflater;
import android.view.View;
import android.view.ViewGroup;
import android.widget.ArrayAdapter;
import android.widget.ImageView;
import android.widget.TextView;
public class MyListAdapter extends ArrayAdapter<String> {
private final Activity context;
private final String[] maintitle;
private final Integer[] imgid;
public MyListAdapter(Activity context, String[] maintitle, Integer[] imgid) {
        super(context, R.layout.mylist, maintitle);
        this.context=context;
        this.maintitle=maintitle;
        this.imgid=imgid;
        }
public View getView(int position,View view,ViewGroup parent) {
        LayoutInflater inflater=context.getLayoutInflater();
        View rowView=inflater.inflate(R.layout.mylist, null,true);
        TextView titleText = (TextView) rowView.findViewById(R.id.title);
        ImageView imageView = (ImageView) rowView.findViewById(R.id.icon);
        titleText.setText(maintitle[position]);
        imageView.setImageResource(imgid[position]);
        return rowView;
        };
}

```
## OUTPUT
![2023-06-01 (7)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/5030f59a-47e0-4b19-843f-aa1c89a4edb0)
![2023-06-01 (8)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/3b4f81a4-04bc-44f5-ae6c-dd3259dfca83)
![2023-06-01 (9)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/bf2b308c-6158-4a14-ac70-c6bc693ba994)
![2023-06-01 (10)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/dd0760a4-e0a7-43e4-ac2e-37a16b7dea28)
![2023-06-01 (11)](https://github.com/Vaish-1011/Mobile-Application-Development/assets/135130074/64964404-2ba5-4fbe-add6-75a1b204f9ac)

## RESULT
Thus a Simple Android Application to create and develop the application to display the place name with image using list view in android studio is developed and executed successfully.

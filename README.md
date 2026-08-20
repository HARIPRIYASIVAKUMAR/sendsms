
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
Developed by: HARI PRIYA S
Register Number : 212223220029
*/
```

## MainActivity.java
```
package com.example.smsintent;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText editPhone, editMessage;
    Button buttonSend;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        editPhone = findViewById(R.id.editPhone);
        editMessage = findViewById(R.id.editMessage);
        buttonSend = findViewById(R.id.buttonSend);

        buttonSend.setOnClickListener(view -> {

            String phone = editPhone.getText().toString();
            String message = editMessage.getText().toString();

            Intent intent = new Intent(Intent.ACTION_VIEW);

            intent.setData(Uri.parse("sms:" + phone));

            intent.putExtra("sms_body", message);

            startActivity(intent);

        });

    }
}
```

## Activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center"
    android:padding="20dp">

    <EditText
        android:id="@+id/editPhone"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Mobile Number"
        android:inputType="phone" />

    <EditText
        android:id="@+id/editMessage"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Message"
        android:inputType="text"
        android:layout_marginTop="15dp" />

    <Button
        android:id="@+id/buttonSend"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Send SMS"
        android:layout_marginTop="20dp" />

</LinearLayout>
```

## OUTPUT
<img width="1915" height="1015" alt="Screenshot 2026-08-07 211554" src="https://github.com/user-attachments/assets/aacd63dc-492b-4d43-b45d-3bb9f5d54af9" />
<img width="1917" height="1020" alt="Screenshot 2026-08-07 211611" src="https://github.com/user-attachments/assets/1866f105-c8b9-4118-83a4-9569b100ed98" />

## RESULT
Thus a Simple Android Application create and design an android application Send SMS using Intent using Android Studio is developed and executed successfully.

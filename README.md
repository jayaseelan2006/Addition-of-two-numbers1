## WORKSHOP 01 — Addition of Two Numbers
## Android Studio — Java
## 1. AIM

To develop an Android application using Android Studio and Java to add two numbers entered by the user and display the result.

## 2. ALGORITHM
Start the application.
Create two input fields to enter the numbers.
Create an ADD button.
Read the first number from the first EditText.
Read the second number from the second EditText.
Convert the input values into integers.
Add the two numbers.
Display the sum in a TextView.
Stop.
## 3. PROGRAM
```
MainActivity.java
package com.example.addition;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2;
    Button addButton;
    TextView result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        addButton = findViewById(R.id.addButton);
        result = findViewById(R.id.result);

        addButton.setOnClickListener(v -> {

            int a = Integer.parseInt(num1.getText().toString());
            int b = Integer.parseInt(num2.getText().toString());

            int sum = a + b;

            result.setText("Result = " + sum);
        });
    }
}
```
## activity_main.xml
```
<?xml version="1.0" encoding="utf-8"?>

<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="30dp">

    <EditText
        android:id="@+id/num1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter first number"
        android:inputType="number" />

    <EditText
        android:id="@+id/num2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter second number"
        android:inputType="number" />

    <Button
        android:id="@+id/addButton"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="ADD" />

    <TextView
        android:id="@+id/result"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Result = "
        android:textSize="22sp"
        android:padding="20dp" />

</LinearLayout>
```
## 4. OUTPUT

Input:
<img width="959" height="539" alt="Screenshot 2026-09-20 175458" src="https://github.com/user-attachments/assets/17ba155e-0c90-475e-b7ef-beb69a0f04f2" />


Enter first number: 20
Enter second number: 80

## After clicking ADD:
<img width="959" height="539" alt="Screenshot 2026-09-20 175433" src="https://github.com/user-attachments/assets/d282fe09-bdcb-435a-b4f9-fd10e4eed67e" />


Result = 100.0
## 5. RESULT

Thus, the Android application for addition of two numbers was successfully developed and executed using Android Studio and Java.

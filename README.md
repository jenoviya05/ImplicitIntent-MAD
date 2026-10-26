# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
1.Create Layout – Add an EditText for URL input and a Button labeled "Navigate".
2.Initialize Components – Link EditText and Button with findViewById().
3.Set Listener – Attach onClickListener to the "Navigate" button.
4.Get Input – Read the text from EditText when button is clicked.
5.Create Intent – Use Intent.ACTION_VIEW with Uri.parse() of the entered URL.
6.Start Activity – Call startActivity(intent) to open the browser page.


## PROGRAM:
```
Program to print the text “Implicitintent”.
Developed by:JENOVIYA D
Registeration Number : 212225040151
```
## MAINACTIVITY.JAVA
~~~
package com.example.activity2;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;

import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        EditText editText;
        Button button;

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.button);
        editText = (EditText) findViewById(R.id.editTextText);

        button.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View view) {
                String url = editText.getText().toString();
                Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
                startActivity(intent);
            }
        });
    }
}
~~~

## ACTIVITY_MAIN.XML
~~~
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#D8B5DE"
    android:backgroundTint="#CBBDCE"
    tools:context=".MainActivity">

    <TextView
        android:id="@+id/textView"
        android:layout_width="215dp"
        android:layout_height="90dp"
        android:fontFamily="sans-serif-black"
        android:text="IMPLICIT INTENT"
        android:textSize="24sp"
        app:layout_constraintBottom_toTopOf="@+id/editTextText"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.602"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.637" />

    <EditText
        android:id="@+id/editTextText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="216dp"
        android:ems="10"
        android:inputType="text"
        android:text="Enter the URL"
        app:layout_constraintBottom_toTopOf="@+id/button"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="136dp"
        android:text="Search"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.498"
        app:layout_constraintStart_toStartOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
~~~



## OUTPUT
<img width="1917" height="1078" alt="Screenshot 2026-10-23 091301" src="https://github.com/user-attachments/assets/a5d6a3a6-26e9-41ec-b1b7-b9a7038cbf3d" />

<img width="1917" height="1078" alt="Screenshot 2026-10-23 091324" src="https://github.com/user-attachments/assets/f935e670-0928-4cca-8d57-588e62816f88" />

<img width="1917" height="1078" alt="Screenshot 2026-10-23 091338" src="https://github.com/user-attachments/assets/47d4e4a3-d5ba-4818-a70a-e6601446e0e0" />



## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.



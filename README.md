# Ex.No:3a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.
## DATE : 27.10.26

## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

1. **Create Layout** – Add an `EditText` for URL input and a `Button` labeled "Navigate".
2. **Initialize Components** – Link `EditText` and `Button` with `findViewById()`.
3. **Set Listener** – Attach `onClickListener` to the "Navigate" button.
4. **Get Input** – Read the text from `EditText` when button is clicked.
5. **Create Intent** – Use `Intent.ACTION_VIEW` with `Uri.parse()` of the entered URL.
6. **Start Activity** – Call `startActivity(intent)` to open the browser page.



## PROGRAM:
```
Program to print the text “Implicitintent”.
Developed by: GURUPARAN G
Registeration Number : 212224220030
```

## MAINACTIVITY:

```
package com.example.mydocs;

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

import com.example.mydocs.R;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        EditText editText;
        Button button;

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        button = findViewById(R.id.btn);
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
```



## ACTIVITY_MAIN.XML:

```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="#99E91E58"
    tools:context=".MainActivity">


    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:fontFamily="sans-serif-condensed-medium"
        android:text="IMPLICIT ACTIVITY"
        android:textSize="48sp"
        app:layout_constraintBottom_toTopOf="@+id/editTextText"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.459"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.363" />

    <EditText
        android:id="@+id/editTextText"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="160dp"
        android:backgroundTint="#EFE91E63"
        android:ems="10"
        android:fontFamily="sans-serif-condensed-medium"
        android:inputType="text"
        android:text="ENTER THE URL"
        android:textSize="20sp"
        app:layout_constraintBottom_toTopOf="@+id/btn"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.6"
        app:layout_constraintStart_toStartOf="parent" />

    <Button
        android:id="@+id/btn"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginBottom="76dp"
        android:backgroundTint="#FA261E1E"
        android:text="SEARCH"
        android:textSize="20sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>

```

## OUTPUT


## MAINACTIVITY:
<img width="1916" height="1198" alt="Screenshot 2026-10-27 000929" src="https://github.com/user-attachments/assets/4d32ac69-d18a-4591-abf6-6d6a7e811485" />



## ACTIVITY_MAIN.XML:
<img width="1917" height="1198" alt="Screenshot 2026-10-27 004759" src="https://github.com/user-attachments/assets/1863fb7f-c15d-4daf-910e-6df57665fd08" />



## DESGINING:
<img width="1917" height="1198" alt="Screenshot 2026-10-27 004855" src="https://github.com/user-attachments/assets/a4ebde2b-0010-44cb-ad92-2d45e7ae0d96" />






## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.



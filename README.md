# Ex.No: 2 To develop an application that uses GUI Components with Fonts and Colors. 
Note: Create button for colors and fonts while clicking color or font button should change 


## AIM:

To create an application that uses GUI Components with Fonts and Colors using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message given in MainActivity file.

Step 7: Save and run the application.


## PROGRAM:
```
/*
Program to print the text “GUIcomponent”.
Developed by: A.Sanjay
Registeration Number :212221040145
*/
```
```
XML FILE:

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
  xmlns:app="http://schemas.android.com/apk/res-auto"
  xmlns:tools="http://schemas.android.com/tools"
  android:layout_width="match_parent"
  android:layout_height="match_parent"
  tools:context=".MainActivity">

<Button
    android:id="@+id/colbut"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginStart="128dp"
    android:layout_marginTop="120dp"
    android:backgroundTint="#FFC107"
    android:text="Change Color"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toTopOf="parent" />

<Button
    android:id="@+id/fonbut"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginStart="132dp"
    android:layout_marginTop="48dp"
    android:backgroundTint="#FF5722"
    android:text="Change Font"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toBottomOf="@+id/colbut" />

<TextView
    android:id="@+id/textView"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:layout_marginStart="48dp"
    android:layout_marginTop="152dp"
    android:text="PRIME PLAYS"
    android:textSize="40dp"
    app:layout_constraintStart_toStartOf="parent"
    app:layout_constraintTop_toBottomOf="@+id/fonbut" />
</androidx.constraintlayout.widget.ConstraintLayout>
```
```
MAINACTIVITY:

package com.example.guicomps;

import androidx.appcompat.app.AppCompatActivity;

import android.content.res.AssetManager;
import android.graphics.Color;
import android.graphics.Typeface;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;

import java.io.IOException;
import java.io.InputStream;

public class MainActivity extends AppCompatActivity implements View.OnClickListener {

private TextView textView;
private Button colorButton;
private Button fontButton;

@Override
protected void onCreate(Bundle savedInstanceState) {
    super.onCreate(savedInstanceState);
    setContentView(R.layout.activity_main);

    textView = findViewById(R.id.textView);
    colorButton = findViewById(R.id.colbut);
    fontButton = findViewById(R.id.fonbut);

    colorButton.setOnClickListener(this);
    fontButton.setOnClickListener(this);
}

@Override
public void onClick(View view) {
    switch (view.getId()) {
        case R.id.colbut:
            changeTextColor();
            break;
        case R.id.fonbut:
            changeFont();
            break;
    }
}

private void changeTextColor() {
    int randomColor = generateRandomColor();
    textView.setTextColor(randomColor);
}

private void changeFont() {
    Typeface newFont = Typeface.createFromAsset(getAssets(), "font/pacifico.ttf");
    textView.setTypeface(newFont);
}

private int generateRandomColor() {
    int red = (int) (Math.random() * 256);
    int green = (int) (Math.random() * 256);
    int blue = (int) (Math.random() * 256);
    return Color.rgb(red, green, blue);
}
}
```
## OUTPUT
![240196753-a9d93852-9167-4979-83bd-113e30a3de00](https://github.com/MilitantVlr/EXP2/assets/121683193/c3f8aaa5-00a9-4194-91db-9d983ee727b7)
![240197186-0a2161d3-b710-4d9f-b68b-a6c6da46c6d4](https://github.com/MilitantVlr/EXP2/assets/121683193/ebb804fa-4ab5-4405-9878-abcaefc628c6)
![240198282-b8b0f459-6f99-4f93-8eb6-7bb3bedea355](https://github.com/MilitantVlr/EXP2/assets/121683193/e3a38b66-38aa-4e7e-a896-20e57bda6133)
![240198349-d1c087eb-2ecd-4232-be79-060657466d7e](https://github.com/MilitantVlr/EXP2/assets/121683193/dbb5731f-327a-4271-b31b-eb80064681a9)
![240198494-f7cbe2f7-2997-4fe1-8584-8d205737c6d9](https://github.com/MilitantVlr/EXP2/assets/121683193/674e767c-3e59-4b33-8394-865aca8da14f)
![240198641-f674f5b4-273d-44ba-aff0-dd5a79bf838c](https://github.com/MilitantVlr/EXP2/assets/121683193/1dcfdcd0-4e63-46c1-a737-7e22629416b5)
![240198848-1f7b7c03-4498-4c5c-81d7-1a81ea59c420](https://github.com/MilitantVlr/EXP2/assets/121683193/f0cec105-9a4c-4c38-a5eb-868c021e2e6c)




## RESULT
Thus a Simple Android Application that uses GUI Components with Fonts and Colors using Android Studio is developed and executed successfully.

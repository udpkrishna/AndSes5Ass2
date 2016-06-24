# AndSes5Ass2

Main Activity.java
package me.rk.andses5ass2;

import android.content.Intent;
import android.provider.ContactsContract;
import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;

public class MainActivity extends AppCompatActivity implements View.OnClickListener{

    private Button mContactbutton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        mContactbutton = (Button) findViewById(R.id.contactButton);
        mContactbutton.setOnClickListener(this);
    }

    @Override
    public void onClick(View v) {
        Intent intentcontact=new Intent();
        intentcontact.setData(ContactsContract.Contacts.CONTENT_URI);
        startActivity(intentcontact);
    }
}


activity_main.xml
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:paddingBottom="@dimen/activity_vertical_margin"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    tools:context="me.rk.andses5ass2.MainActivity">

    <Button
        android:id="@+id/contactButton"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Open Contacts"
        android:layout_centerHorizontal="true"/>
</RelativeLayout>

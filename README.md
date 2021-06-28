# ChatApp

implementation 'com.google.firebase:firebase-core:16.0.8'
    implementation 'com.google.firebase:firebase-auth:16.2.1'
    implementation 'com.google.android.gms:play-services-auth:16.0.1'
    implementation 'com.google.firebase:firebase-database:16.1.0'
    implementation 'com.firebaseui:firebase-ui:0.6.2'
    
    
    
    <?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:background="@color/colorPrimary">

    <TextView
        android:id="@+id/title"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="8dp"
        android:layout_marginTop="156dp"
        android:layout_marginEnd="8dp"
        android:fontFamily="monospace"
        android:text="AndroidDvlpr\nChat Room"
        android:textAlignment="center"
        android:textColor="@color/colorAccent"
        android:textSize="50sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <EditText
        android:id="@+id/editText"
        android:layout_width="300dp"
        android:layout_height="wrap_content"
        android:layout_marginTop="50dp"
        android:layout_marginStart="8dp"
        android:layout_marginEnd="8dp"
        android:hint="Enter a random username"
        android:textAlignment="center"
        android:textColor="#FFF"
        android:textColorHint="#7AFFFFFF"
        android:textSize="20sp"
        app:layout_constraintTop_toBottomOf="@id/title"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.496"
        app:layout_constraintStart_toStartOf="parent"
        tools:layout_editor_absoluteY="204dp" />

    <com.google.android.gms.common.SignInButton
        android:id="@+id/signInBtn"
        android:layout_width="300dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="8dp"
        android:layout_marginTop="20dp"
        android:layout_marginEnd="8dp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.494"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editText" />

</androidx.constraintlayout.widget.ConstraintLayout>

<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".ChatActivity">

    <ListView
        android:id="@+id/list_message"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:layout_marginBottom="50dp"
        app:layout_constraintBottom_toTopOf="@+id/linearLayout"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        android:stackFromBottom="true"
        android:transcriptMode="alwaysScroll"
        android:dividerHeight="16dp"
        android:divider="@android:color/transparent"
        />

    <LinearLayout
        android:id="@+id/linearLayout"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:orientation="horizontal"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent">

        <EditText
            android:id="@+id/user_message"
            android:layout_width="match_parent"
            android:layout_height="50dp"
            android:layout_weight="1" />

        <ImageView
            android:id="@+id/send_image"
            android:padding="7dp"
            android:tint="@color/colorAccent"
            android:layout_width="match_parent"
            android:layout_height="50dp"
            android:layout_gravity="center"
            android:layout_weight="5"
            android:src="@drawable/ic_send" />

    </LinearLayout>

</androidx.constraintlayout.widget.ConstraintLayout>



<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <TextView
        android:layout_alignParentTop="true"
        android:layout_alignParentStart="true"
        android:id="@+id/message_user"
        android:textStyle="normal|bold"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" />

    <TextView
        android:layout_alignParentBottom="@+id/message_user"
        android:layout_alignParentEnd="true"
        android:id="@+id/message_time"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" />

    <TextView
        android:layout_alignParentStart="true"
        android:layout_marginTop="5dp"
        android:layout_below="@id/message_user"
        android:textAppearance="@style/TextAppearance.AppCompat.Body1"
        android:textColor="#FFF"
        android:textSize="18sp"
        android:id="@+id/message_text"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:padding="10dp"
        />

</RelativeLayout>

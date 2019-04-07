实验二：Android布局
（1）使用LinearLayout布局实现界面
   activity_main.xml
<?xml version="1.0" encoding="utf-8"?>

<LinearLayout
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    tools:context=".MainActivity">

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="30dp">

        <TextView
            android:layout_width="93dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="one,one" />

        <TextView
            android:layout_width="109dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="one,two" />

        <TextView
            android:layout_width="119dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="one,three" />

        <TextView
            android:layout_width="87dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="one,four" />

    </LinearLayout>
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="30dp">

        <TextView
            android:layout_width="102dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="two,one" />

        <TextView
            android:layout_width="113dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="two,two" />

        <TextView
            android:layout_width="119dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="two,three" />

        <TextView
            android:layout_width="70dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="two,four" />

    </LinearLayout>
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="30dp">

        <TextView
            android:layout_width="98dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="three,one" />

        <TextView
            android:layout_width="108dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="three,two" />

        <TextView
            android:layout_width="102dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="three,three" />

        <TextView
            android:layout_width="96dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="three,four" />

    </LinearLayout>
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="30dp">

        <TextView
            android:layout_width="70dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="four,one" />

        <TextView
            android:layout_width="131dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="four,two" />

        <TextView
            android:layout_width="133dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="four,three" />

        <TextView
            android:layout_width="70dp"
            android:layout_height="match_parent"
            android:gravity="center"
            android:text="four,four" />

    </LinearLayout>

    <Button
        android:id="@+id/button"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="next" />
</LinearLayout>

### MainActivity.java
public class MainActivity extends AppCompatActivity {

    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        Button btn;
        btn = (Button) findViewById(R.id.button);
        btn.setOnClickListener(new View.OnClickListener() {
            public void onClick(View v) {
                Intent intent = new Intent(MainActivity.this, Main2Activity.class);
                startActivity(intent);
            }
        });
    }
}
截图：
![Image text](https://raw.githubusercontent.com/695400861/Layout/master/image/X~N)%5BMNJPGQGA%5B%24AG)2OI5T.png)




（2）使用ConstraintLayout布局实现界面
   activity_main2.xml：
<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".Main3Activity">

    <TextView
        android:id="@+id/RED"
        android:layout_width="79dp"
        android:layout_height="44dp"
        android:layout_marginStart="24dp"
        android:layout_marginLeft="24dp"
        android:layout_marginTop="24dp"
        android:background="#FD0000"
        android:gravity="center"
        android:lineSpacingExtra="8sp"
        android:text="RED"
        android:textColor="@color/colorAccent"
        android:typeface="normal"
        android:visibility="visible"
        app:fontFamily="sans-serif"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        tools:text="RED" />

    <TextView
        android:id="@+id/YELLOW"
        android:layout_width="79dp"
        android:layout_height="44dp"
        android:layout_marginTop="24dp"
        android:layout_marginEnd="24dp"
        android:layout_marginRight="24dp"
        android:background="#FFF300"
        android:gravity="center"
        android:text="YELLOW"
        android:textColor="@color/colorAccent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        tools:text="YELLOW" />

    <TextView
        android:id="@+id/VIOLET"
        android:layout_width="403dp"
        android:layout_height="47dp"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:layout_marginBottom="8dp"
        android:background="#E175F3"
        android:gravity="center"
        android:text="VIOLET"
        android:textColor="@color/colorAccent"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.275"
        tools:text="VIOLET" />

    <TextView
        android:id="@+id/BLUE"
        android:layout_width="79dp"
        android:layout_height="44dp"
        android:layout_marginStart="24dp"
        android:layout_marginLeft="24dp"
        android:layout_marginTop="24dp"
        android:layout_marginBottom="24dp"
        android:background="#2196F3"
        android:gravity="center"
        android:text="BLUE"
        android:textColor="@color/colorAccent"
        app:layout_constraintBottom_toTopOf="@+id/VIOLET"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.461"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/ORANGE"
        app:layout_constraintVertical_bias="0.0"
        tools:text="BLUE" />

    <TextView
        android:id="@+id/GREEN"
        android:layout_width="79dp"
        android:layout_height="44dp"
        android:layout_marginStart="24dp"
        android:layout_marginLeft="24dp"
        android:layout_marginTop="96dp"
        android:layout_marginEnd="20dp"
        android:layout_marginRight="20dp"
        android:background="#4CAF50"
        android:gravity="center"
        android:text="GREEN"
        android:textColor="@color/colorAccent"
        app:layout_constraintEnd_toStartOf="@+id/BLUE"
        app:layout_constraintHorizontal_bias="1.0"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        tools:text="GREEN" />

    <TextView
        android:id="@+id/INDIGO"
        android:layout_width="79dp"
        android:layout_height="44dp"
        android:layout_marginStart="24dp"
        android:layout_marginLeft="24dp"
        android:layout_marginTop="96dp"
        android:layout_marginEnd="24dp"
        android:layout_marginRight="24dp"
        android:background="#3F51B5"
        android:gravity="center"
        android:text="INDIGO"
        android:textColor="@color/colorAccent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toEndOf="@+id/BLUE"
        app:layout_constraintTop_toTopOf="parent"
        tools:text="INDIGO" />

    <TextView
        android:id="@+id/ORANGE"
        android:layout_width="79dp"
        android:layout_height="44dp"
        android:layout_marginStart="24dp"
        android:layout_marginLeft="24dp"
        android:layout_marginTop="24dp"
        android:layout_marginEnd="24dp"
        android:layout_marginRight="24dp"
        android:background="#FF9800"
        android:gravity="center"
        android:text="ORANGE"
        android:textColor="@color/colorAccent"
        app:layout_constraintEnd_toStartOf="@+id/YELLOW"
        app:layout_constraintStart_toEndOf="@+id/RED"
        app:layout_constraintTop_toTopOf="parent"
        tools:text="ORANGE" />

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="8dp"
        android:layout_marginLeft="8dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:layout_marginBottom="8dp"
        android:text="next"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.514"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.4" />


</android.support.constraint.ConstraintLayout>

  Main2Activity.java
public class Main2Activity extends AppCompatActivity {
   private Button b2;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);

        b2 = (Button) findViewById(R.id.button2);
        b2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                Intent intent=new Intent(Main2Activity.this,Main3Activity.class);
                startActivity(intent);

            }
        });
    }
}
截图：
![Image text](https://raw.githubusercontent.com/695400861/Layout/master/image/BLA51KQWL65HWM4I~%40Q%7D_CX.png)

（3）使用TableLayout布局实现界面
   activity_main3.xml
<?xml version="1.0" encoding="utf-8"?>
<TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".Main3Activity">


    <TableRow
        android:layout_width="match_parent"
        android:layout_height="match_parent">


        <TextView
            android:id="@+id/textView"
            android:layout_width="225dp"
            android:layout_height="wrap_content"
            android:text="    Open..." />

        <TextView
            android:id="@+id/textView3"
            android:layout_width="133dp"
            android:layout_height="match_parent"
            android:layout_gravity="right"
            android:text="Ctrl-O" />
    </TableRow>

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="match_parent" >

        <TextView
            android:id="@+id/textView4"
            android:layout_width="280dp"
            android:layout_height="wrap_content"
            android:text="    Save..." />

        <TextView
            android:id="@+id/textView6"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="right"
            android:text="Ctrl-S" />
    </TableRow>

    <TableRow
        android:layout_width="425dp"
        android:layout_height="match_parent">

        <TextView
            android:id="@+id/textView7"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="    Save As..." />

        <TextView
            android:id="@+id/textView9"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="right"
            android:text="Ctrl-Shift-S" />
    </TableRow>

    <TextView
    android:layout_width="match_parent"
    android:layout_height="1dp"
    android:background="#000000"/>

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="match_parent" >

        <TextView
            android:id="@+id/textView10"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="X Import..." />

        <TextView
            android:id="@+id/textView2"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content" />

    </TableRow>

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="match_parent" >

        <TextView
            android:id="@+id/textView8"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="X Export..." />

        <TextView
            android:id="@+id/textView11"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_gravity="right"
            android:text="Ctrl-E" />
    </TableRow>

    <TextView
        android:layout_width="match_parent"
        android:layout_height="1dp"
        android:background="#000000"/>

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="match_parent" >

        <TextView
            android:id="@+id/textView12"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="    Quit" />
    </TableRow><![CDATA[
    =/>

]]>
</TableLayout>
截图：
![Image text](https://raw.githubusercontent.com/695400861/Layout/master/image/SZ%7D3~YGNH4%25%7BX4%60_5D%40U025.png)


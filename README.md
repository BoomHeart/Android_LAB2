# LAB2实验报告

## 一、实验要求
1、利用线性布局实现界面

2、利用ConstraintLayout实现界面

3、利用表格布局实现界面

## 二、实验步骤

### 1、利用线性布局实现界面代码
```java
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical">
    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0">
        
        <Button
            android:id="@+id/one_one"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="one,one" />

        <Button
            android:id="@+id/one_two"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="one,two" />

        <Button
            android:id="@+id/one_three"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="one,three" />

        <Button
            android:id="@+id/one_four"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="one,four" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0">

        <Button
            android:id="@+id/two_one"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="two,one" />

        <Button
            android:id="@+id/two_two"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="two,two" />

        <Button
            android:id="@+id/two_three"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="two,three" />

        <Button
            android:id="@+id/two_four"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="two,four" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0">

        <Button
            android:id="@+id/three_one"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="three,one" />

        <Button
            android:id="@+id/three_two"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="three,two" />

        <Button
            android:id="@+id/three_three"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="three,three" />

        <Button
            android:id="@+id/three_four"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="three,four" />
    </LinearLayout>

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_weight="0">

        <Button
            android:id="@+id/four_one"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="four,one" />

        <Button
            android:id="@+id/four_two"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="four,two" />

        <Button
            android:id="@+id/four_three"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="four,three" />

        <Button
            android:id="@+id/four_four"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="four,four" />
    </LinearLayout>
</LinearLayout>
```
运行结果：

![](https://github.com/BoomHeart/Android_LAB2/blob/master/1.png)

### 2、利用ConstraintLayout实现界面

代码：

```java
<?xml version="1.0" encoding="utf-8"?>
<android.support.constraint.ConstraintLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:layout_width="match_parent"
    android:layout_height="match_parent">


    <Button android:id="@+id/ButtonA"
        android:layout_width="100dp"
        android:layout_height="50dp"
        android:text="RED"
        android:background="#FF0000"/>
    <Button android:id="@+id/ButtonB"
        android:layout_width="100dp"
        android:layout_height="50dp"
        android:text="ORANGE"
        android:background="#FFA500"
        app:layout_constraintLeft_toRightOf="@id/ButtonA"
        android:layout_margin="50dp"/>
    <Button android:id="@+id/ButtonC"
        android:layout_width="100dp"
        android:layout_height="50dp"
        android:text="YELLOW"
        android:background="#FFFF00"
        app:layout_constraintLeft_toRightOf="@id/ButtonB"
        android:layout_margin="50dp"/>
    <Button android:id="@+id/ButtonD"
        android:layout_width="100dp"
        android:layout_height="50dp"
        android:text="BLUE"
        android:background="#0000FF"
        app:layout_constraintTop_toBottomOf="@id/ButtonA"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        android:layout_margin="30dp"/>
    <Button
        android:layout_width="100dp"
        android:layout_height="50dp"
        android:text="GREEN"
        android:background="#008000"
        app:layout_constraintRight_toLeftOf="@id/ButtonD"
        android:layout_marginRight="10dp"
        app:layout_constraintTop_toBottomOf="@id/ButtonA"
        android:layout_marginTop="30dp"
        />
    <Button
        android:layout_width="100dp"
        android:layout_height="50dp"
        android:text="INDIGO"
        android:background="#4B0082"
        app:layout_constraintLeft_toRightOf="@id/ButtonD"
        android:layout_marginLeft="10dp"
        app:layout_constraintTop_toBottomOf="@id/ButtonA"
        android:layout_marginTop="30dp"
        />
    <Button android:id="@+id/ButtonG"
        android:layout_width="match_parent"
        android:layout_height="70dp"
        android:text="VIOLET"
        android:background="#C71585"
        app:layout_constraintBottom_toBottomOf="parent"
        />
</android.support.constraint.ConstraintLayout>
```

运行结果:

![](https://github.com/BoomHeart/Android_LAB2/blob/master/2.png)

### 3、利用表格布局实现界面

代码:

```java
<?xml version="1.0" encoding="utf-8"?>
<TableLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:stretchColumns="1">
    <TableRow
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="1"
            android:text="Open..." />

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_column="2"
            android:layout_gravity="right"
            android:text="Ctrl-O" />
    </TableRow>
    <TableRow
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:showDividers="end">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="1"
            android:text="Save..." />

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_column="2"
            android:layout_gravity="right"
            android:text="Ctrl-S" />
    </TableRow>

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="1"
            android:text="Save As..." />

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_column="2"
            android:layout_gravity="right"
            android:text="Ctrl-Shift-S" />
    </TableRow>

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="0"
            android:text="X " />

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="1"
            android:text="Import..." />
    </TableRow>

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:showDividers="end">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="0"
            android:text="X " />

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="1"
            android:text="Export..." />

        <TextView
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:layout_column="2"
            android:layout_gravity="right"
            android:text="Ctrl-E" />
    </TableRow>

    <TableRow
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_column="1"
            android:text="Quit" />
    </TableRow>
    >
</TableLayout>
```

运行结果：

![](https://github.com/BoomHeart/Android_LAB2/blob/master/3.png)

添加了分割线代码

```java
android:showDividers="end"
```

但是不知为何没有显示

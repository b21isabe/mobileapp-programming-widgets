
# Rapport

För att skapa en constraint-view använde jag mig utav designläget där jag drog en constraintview
till komponent trädet, sedan drog jag även dit en edittext view, en image view och en button.

Kodexempel 1
```
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    ...
    <ImageView
    ...
    />
    <EditText
    ...
    />
    <Button
    ...
    />
</androidx.constraintlayout.widget.ConstraintLayout>

```


Jag importerade sedan en public domain bild som jag länkade till min imageview.
https://www.flickr.com/photos/watts_photos/20800849988/

Kodexempel 2
```
    <ImageView
        app:srcCompat="@drawable/panda"
```

Efter detta justerade jag mina views constraints i designläget, dvs jag satte constraints för imageviewen till dess förälder till toppen, botten höger och vänster av bildskärmen.
Jag skapade sedan en kedja mellan min edittext och min button och satte constraints så att toppen av de kedjade viewsen hade constraints till botten av bilden, och sidorna och botten hade constraints till deras parent.
Kodexempel 3
```
    <EditText
        ...
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toStartOf="@+id/button"
        app:layout_constraintHorizontal_chainStyle="spread"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/imageView"
        ...
```

Till sist flyttade jag på viewsens position i designläget så att de var placerade högre upp på sidan och gav alla views en margin på 25dp.
Kodexempel 4
```
    <ImageView
        ...
        app:layout_constraintHorizontal_bias="0.497"
        ...
        app:layout_constraintVertical_bias="0.233"
        ...
        android:layout_margin="25dp"/>
        ...
```



![](sc.png)

# Sann-apk
Generate ai
<uses-permission android:name="android.permission.INTERNET" />
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp">

    <EditText
        android:id="@+id/promptInput"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Masukkan deskripsi gambar" />

    <Spinner
        android:id="@+id/styleSpinner"
        android:layout_width="match_parent"
        android:layout_height="wrap_content" />

    <Button
        android:id="@+id/generateButton"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Generate" />

    <ImageView
        android:id="@+id/imageResult"
        android:layout_width="match_parent"
        android:layout_height="300dp"
        android:scaleType="centerCrop"
        android:layout_marginTop="16dp"/>
</LinearLayout>
val styles = listOf("Realistic", "Anime", "Pixel Art", "Cyberpunk", "Logo")
val adapter = ArrayAdapter(this, android.R.layout.simple_spinner_item, styles)
adapter.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item)
styleSpinner.adapter = adapter

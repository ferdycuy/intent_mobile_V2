# intent_mobile_V2

  Nama    : Ferdyana Eka Prasetya</br>
  NIM     : 312210121</br>
  Kelas   : TI.22.A.1</br>
  Dosen   : Donny Maulana, S.Kom., M.M.S.I.</br>

  **Aplikasi versi kedua, dengan perubahan tombol text menjadi ICON**

  ## Tugas
Buatlah tampilan menu Versi 02 dari project-project yang sudah dibuat sebelumnya<br>

dengan tampilan sebagai berikut :<br>
  ![image](https://github.com/ferdycuy/intent_mobile_V2/assets/115714443/7ccd29a0-66da-4c6f-b746-c099c5278e6d)

  ## Langkah-langkah yang harus dilakukan
- Pertama, kita buat dulu sebuah drawable resource file. Kita beri nama file nya 'backgroundicon.xml' dengan root elementnya adalah shape.
> Klik kanan>new>drawable resource file>isi nama file & root>ok
*Didalam backgroundicon.xml kita tambahkan code berikut:*

```
<?xml version="1.0" encoding="utf-8"?>
<shape xmlns:android="http://schemas.android.com/apk/res/android">
  <solid android:color="@color/colorPrimaryDark"/>
  <corners android:radius="80dp"/>
  <size android:width="80dp" android:height="80dp"/>
</shape>
```

- Selanjutnya untuk icon, kali ini kita bisa pakai icon yang sudah disediakan oleh android studio biar lebih mudah, Caranya adalah dengan menambah vector asset pada drawable file. kalian juga bisa menggunakan icon yang kalian punya.
> Klik kanan>new>vector asset>clip art>pilih icon yang ingin digunakan>next>finish
**NOTE**: Sesuaikan nama dan ukuran dengan kebutuhan kalian

*Oke, jika sudah selesai melakukan semua hal diatas, selanjutnya kita akan edit 'acitivy_main.xml' nya, untuk mengganti tombol yang awal nya button menjadi image button, yang bertujuan untuk merubah dari tombol teks menjadi icon. Pertama kita menghapus terlebih dulu semua button kecuali imageview untuk background, namun disarankan salin code button sebelumnya karena akan dipakai lagi nantinya.*

- Silahkan masukkan source code di'acitivy_main.xml' sebagai berikut:
```
    <ImageView
        android:id="@+id/background"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:adjustViewBounds="true"
        android:scaleType="centerCrop"
        android:src="@drawable/bg_mainbutterfly" />

    <LinearLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:orientation="vertical"
        android:gravity="center_horizontal">

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            android:gravity="center">

            <ImageButton
                android:id="@+id/btnHelloWorld"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnHelloWorld"
                android:src="@drawable/icon_hello"
                tools:ignore="UsingOnClickInXml,SpeakableTextPresentCheck" />

            <ImageButton
                android:id="@+id/btnProjectCount"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnCount"
                android:src="@drawable/icon_count"
                tools:ignore="UsingOnClickInXml,SpeakableTextPresentCheck" />

            <ImageButton
                android:id="@+id/btnProjectSianida"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnSianida"
                android:src="@drawable/icon_sianida"
                tools:ignore="UsingOnClickInXml,SpeakableTextPresentCheck" />
        </LinearLayout>

        <LinearLayout
            android:layout_width="match_parent"
            android:layout_height="wrap_content"
            android:orientation="horizontal"
            android:gravity="center">

            <ImageButton
                android:id="@+id/btnPesanActivity"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnPesanActivity"
                android:src="@drawable/icon_pesan"
                tools:ignore="UsingOnClickInXml, SpeakableTextPresentCheck" />

            <ImageButton
                android:id="@+id/btnSetAlarm"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnSetAlarm"
                android:src="@drawable/icon_alarm"
                tools:ignore="UsingOnClickInXml,SpeakableTextPresentCheck" />

            <ImageButton
                android:id="@+id/btnShowMap"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_margin="20dp"
                android:background="@drawable/backgroundicon"
                android:onClick="btnShowMap"
                android:src="@drawable/icon_lokasi"
                tools:ignore="UsingOnClickInXml,SpeakableTextPresentCheck" />
        </LinearLayout>
    </LinearLayout>
```
- **PENJELASAN**
- Penambahan '<linear layout'  dengan orientasi vertical untuk dasar dari penempatan tombol.
  ~ Lalu, didalam LinearLayout vertical ini. Kita tambahkan lagi LinearLayout, tapi dengan orentasi horizontal agar tombol berjejer kesamping.

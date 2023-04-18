
# Rapport

I denna uppgiften så var kravet att lägga in 3 egna "widgets" eller views på en ny app-template. Jag valde att lägga in en bild, 
en textview som ser ut som en bildtext samt två knappar för yes/no som inte har någon funktion än. Detta gjorde jag med en 
constraintlayout vilket innebär att alla elementen har constraints som bestämmer deras positioner vilket gör positionerna blir 
samma hela tiden då de är constrainade till olika element.

Min constraint layout täcker upp i princip hela skärmen med en bredd på 409dp och 729dp och med constraints till parent som blir hela skärmen.
    <androidx.constraintlayout.widget.ConstraintLayout
        android:layout_width="409dp"
        android:layout_height="729dp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent">

Mina två knappar använder sig av wrap content för både höjd och bredd vilket innebär att den anpassas för att få plats med innehållet i knapparna.
        <Button
            android:id="@+id/button3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:layout_marginStart="4dp"
            android:layout_marginLeft="4dp"
            android:layout_marginBottom="32dp"
            android:text="Yes"
            app:layout_constraintBottom_toBottomOf="parent"
            app:layout_constraintStart_toStartOf="parent" />

Bilden som jag har lagt in använder samma princip då det är en widget som innehåller en bild, bilden är constrainad till 
parent vilket är constraintlayout. Bilden har även en beskrivning.
        <ImageView
            android:id="@+id/imageView3"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:contentDescription="Bild"
            app:layout_constraintBottom_toTopOf="@+id/guideline"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toTopOf="parent"
            app:srcCompat="@android:drawable/sym_def_app_icon" />

För att sedan ha en typ av bildtext så la jag till en textview som alignas i mitten av skärmen med hjälp av constraints åt sidorna.
        <TextView
            android:id="@+id/textView"
            android:layout_width="112dp"
            android:layout_height="18dp"
            android:text="      Android guy"
            app:layout_constraintEnd_toEndOf="parent"
            app:layout_constraintStart_toStartOf="parent"
            app:layout_constraintTop_toBottomOf="@+id/imageView3" />

## Följande grundsyn gäller dugga-svar:

- Ett kortfattat svar är att föredra. Svar som är längre än en sida text (skärmdumpar och programkod exkluderat) är onödigt långt.
- Svaret skall ha minst en snutt programkod.
- Svaret skall inkludera en kort övergripande förklarande text som redogör för vad respektive snutt programkod gör eller som svarar på annan teorifråga.
- Svaret skall ha minst en skärmdump. Skärmdumpar skall illustrera exekvering av relevant programkod. Eventuell text i skärmdumpar måste vara läsbar.
- I de fall detta efterfrågas, dela upp delar av ditt svar i för- och nackdelar. Dina för- respektive nackdelar skall vara i form av punktlistor med kortare stycken (3-4 meningar).

Programkod ska se ut som exemplet nedan. Koden måste vara korrekt indenterad då den blir lättare att läsa vilket gör det lättare att hitta syntaktiska fel.

```
function errorCallback(error) {
    switch(error.code) {
        case error.PERMISSION_DENIED:
            // Geolocation API stöds inte, gör något
            break;
        case error.POSITION_UNAVAILABLE:
            // Misslyckat positionsanrop, gör något
            break;
        case error.UNKNOWN_ERROR:
            // Okänt fel, gör något
            break;
    }
}
```

Bilder läggs i samma mapp som markdown-filen.

![](android.png)

Läs gärna:

- Boulos, M.N.K., Warren, J., Gong, J. & Yue, P. (2010) Web GIS in practice VIII: HTML5 and the canvas element for interactive online mapping. International journal of health geographics 9, 14. Shin, Y. &
- Wunsche, B.C. (2013) A smartphone-based golf simulation exercise game for supporting arthritis patients. 2013 28th International Conference of Image and Vision Computing New Zealand (IVCNZ), IEEE, pp. 459–464.
- Wohlin, C., Runeson, P., Höst, M., Ohlsson, M.C., Regnell, B., Wesslén, A. (2012) Experimentation in Software Engineering, Berlin, Heidelberg: Springer Berlin Heidelberg.

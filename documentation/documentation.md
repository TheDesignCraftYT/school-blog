<!--- To view this file in the right layout, please open https://github.com/TheDesignCraftYT/school-blog/blob/main/documentation/documentation.md -->

<img align="right" src="https://github.com/TheDesignCraftYT/school-blog/blob/main/documentation/layout.png?raw=true" width="320" height="180" alt="Layout Image">

# Dokumentation
Das Ziel dieses Projekts war es, eine vom Layout her an MacOS angelehnte, fiktive Blog-Website zu erstellen.
Um sich eine Liste an Änderungen des Projekts mit den jeweiligen Änderungszeitpunkten anzuschauen, klicke [hier](https://github.com/TheDesignCraftYT/school-blog/commits).

## Probleme & Lösungen
### Problem: Zu faul zum copy & pasten --> Lösung: Iframes
Da ich zu faul war, Inhalte, die auf jeden / mehreren Seiten zu sehen sein sollen überall neu einzufügen bei jeder kleinen Änderung, habe ich `<iframe>`s benutzt.
Iframes sind im Grunde genommen einfach nur Fenster, die auf eine andere Seite zeigen. Das hat den Vorteil, dass man die Inhalte nur an einer Stelle ändern muss, um sie überall zu ändern.
Dazu habe ich für jeden Inhalt, der auf mehreren Seiten zu sehen sein soll, eine eigene HTML-Datei erstellt, die dann in den Iframes eingebunden wird.
Diese HTML-Dateien, die nur zum Einbinden gedacht sind, habe ich in den Ordner [`/iframes`](https://github.com/TheDesignCraftYT/school-blog/tree/main/iframes) gepackt.
So wurden Inhalte, wie z.B. die [Menü-Leiste](https://github.com/TheDesignCraftYT/school-blog/blob/main/iframes/menu.html) einfach einmal geschrieben und dann nur noch überall eingebettet.

### Problem: Darstellung verschiedener Browser
Da verschiedene Browser Seiten anders darstellen, und dadurch z.B. die Menü-Leiste über die Bildschirmbreite hinausgezogen wurde, habe ich das vertikale Scrollen deaktiviert:
```css
body {
    overflow-y: hidden;
}
```

### Problem: Bilder laden zu langsam --> Lösung: Anderes Bildformat
Da die Bilder, die ich verwendet habe, meistens im .png Format waren, habe ich diese in .webp umgewandelt, da diese Bilder extra für Webseiten und Browser ausgelegt sind und so schneller geladen werden können.
# Rick and Morty Vue App

### Açıklama
```
Proje Vue ile geliştirilip Cordova'ya entegre edilmiştir. cmd ortamında ya da IDE terminalde
"npm install" yaptığımızda gerekli olan tüm eklentileri kuracaktır.
Projenin Cordova ile mobil ortamda çalışması için sanal bir cihaza ihtyiaç vardır.
Android Studio üzerinden bir sanal cihaz ile çalıştırabilirsiniz.

Not: Eğer bilgisayarınızın dili Türkçe ve proje dosyanız masaüstünüzde ise "gradle.build" hatası alabilirsiniz.
Hatanın sebebi dosyanın bulunduğu url'de Türkçe karakter "Masaüstü" bulunmasından
kaynaklı uygulamayı direkt Yerel Disk:C içerisinde çalıştırmanız tercih edilir.
```

## Proje için gerekli olan tüm eklentileri kurmak için
```
npm install
```

### Projeyi tarayıcı üzerinde çalıştırmak için
```
npm run serve
```
### Projeyi emülatör üzerinde çalıştırmak için
```
$ npm run cordova-serve-android 
```

### Customize configuration
See [Configuration Reference](https://cli.vuejs.org/config/).

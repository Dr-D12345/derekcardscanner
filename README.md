
![LOGO](https://github.com/Dr-D12345/Link-N-Connect/blob/master/AndroidApp/app/src/main/res/mipmap-hdpi/ic_launcher.png)
# Link'N Connect
This Android app uses https request and Google Camera Api's OCR function to analyze bussiness cards in search of emails, names and other text.

# How
### Android
Requring Camera, Gallery and Internet permissions, the App allows for selections of a template, choosing a card from the gallery and/or taking a picture of a new card. Once a the user chooses to pick a new card and Android Image Intent fires off returning a picture that is saved to internal storage.From there the card is sent to firebase storage to have a public domain
### Firebase
Using Firebase's Storage function, the app allows the picture to optain a public url. Once uploaded the URL is returned to the device to be URLENCODED and sent as a parameter to the node js server
### Node JS
The Server has a listener listening for a picture request. From there it downloads the picture based on the url givin in the parameter. Once downloaded using google services API it returns a string result of all the text recieved from the API that is returned to the device to be parsed

*BE WARNED RECENTLY THE API HAS BEEN TURNED OFF AND WILL NOT BE RETURNING API RESULTS*


# References
**Http Request** [AnalyzeActivity.java](https://github.com/Dr-D12345/Link-N-Connect/blob/master/app/src/main/java/com/google/sample/cloudvision/AnalyzeActivity.java)

**Node js URL** [https://derekcardscanner.herokuapp.com/](https://derekcardscanner.herokuapp.com/)

**API Practices**
```
https://derekcardscanner.herokuapp.com/pic/(ENTERENCODEDURLHERE)
```
# TO-DO
- Auth for URL Requests
- Add Static Page for Server








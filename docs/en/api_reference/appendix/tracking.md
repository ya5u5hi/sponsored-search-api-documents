# Tracking Parameters
Retrieving the information on which type of ads are clicked will be possible from Sponsored Search API tracking parameters. <br>
This functions can easily confirm the effect of ads, which it may leads to a better advertisement.<br>
Tracking parameteres available on Sponsored Search API are as follows.<br>
<br>
[Note]<br>
This function is designed for third party tool providers who use the Sponsored Search API. <br>
Third party tool providers are allowed to use the tracking data only for effectiveness measurement on their own system. <br>
Providers are not allowed to provide, transfer, or sell the raw tracking data to their customers (advertisers).<br>
<br>
Conversion Analytics on Mobile App Download ads is available for Android App only. And it can count a download event by user when he/she directly goes to download via 'Google Play Store App' from your ad, but a download occurred on 'Google Play Store' browser edition cannot be a conersion counted.<br>
<br>

Parameter | Description | Sample URL Format
---------- | ------------------- | ----------------------
creative |Displays Ad Tracking ID (adTrackID).<br>* An unique ID given to each ad. It differs from Ad ID (adId).| http://www.example.com/?creative={creative} 
keyword | Displays bidding keyword.| http://www.example.com/?keyword={keyword} 
matchtype | Displays match type of keyword.<br> Details are below.<br> - e: Exact Match<br> - p: Phrase Match<br> - b：Broad Match|http://www.example.com/?matchtype={matchtype} 
device | Displays the device clicked from. <br>Details are below.<br> - m: Smartphone and WAP phone (feature phone)<br> - t: Tablet<br> - c: PC | http://www.example.com/?device={device}<br>
ifmobile | Any value can be appended to the URL when ads are clicked from Smartphone, if you enable this parameter. It will allow you to convert it to Smartphone URL and to add parameters.<br>* Available for Landing Page URL, Tracking URL and Custom parameters.| http://www.example.com/?ifmobile={ifmobile:[value]}
ifnotmobile| Any value can be appended to the URL when ads are clicked from PC/Tablet, if you enable this parameter. It will allow you to convert it to PC/Tablet URL and to add parameters.<br>*  Available for Landing Page URL, Tracking URL and Custom parameters.| http://www.example.com/?ifnotmobile={ifnotmobile:[value]}
lpurl | It inserts Landing Page URL into the position specified. Can use for setting to Tracking URL. | Landing Page URL<br>http://www.yahoo.co.jp/?param=1<br>Tracking URL<br>http://www.yahoo.co.jp/?lp={lpurl}<br>Delivered URL by click on ad<br>http://www.yahoo.co.jp/?lp=http://www.yahoo.co.jp/%3Fparam%3D1
lpurl+2 | The Tracking URL including 'lpurl' (Landing Page URL), and it is available in the case when requires double encoding of symbols, "?", "=", """, "#", "\t", "'" and single space.| Landing Page URL<br>http://www.yahoo.co.jp/?param=1<br>Tracking URL<br>http://www.yahoo.co.jp/?lp={lpurl+2}<br>Delivered URL by click on ad<br>http://www.yahoo.co.jp/?lp=http://www.yahoo.co.jp/%253Fparam%253D1
lpurl+3 | The Tracking URL including 'lpurl' (Landing Page URL), and it is available in the case when requires triple encoding of symbols, "?", "=", """, "#", "\t", "'" and single space.| Landing Page URL<br>http://www.yahoo.co.jp/?param=1<br>Tracking URL<br>http://www.yahoo.co.jp/?lp={lpurl+3}<br>Delivered URL by click on ad<br>http://www.yahoo.co.jp/?lp=http://www.yahoo.co.jp/%25253Fparam%25253D1
unescapedlpurl | The Tracking URL The Tracking URL including 'lpurl' (Landing Page URL), and it is available in the case when requires no encoding of lpurl. You can enable it only at the beginning of your URL. | Landing Page URL<br>http://www.yahoo.co.jp/?param=1<br>Tracking URL<br>{unescapedlpurl}&param2=2<br>Delivered URL by click on ad<br>http://www.yahoo.co.jp/?param=1&param2=2
escapedlpurl | The Tracking URL including 'lpurl' (Landing Page URL), and available in the case of encoding symbols of ":", "/", "?", "=", "%".| Landing Page URL<br>http://www.yahoo.co.jp/?param=1<br>Tracking URL<br>http://www.yahoo.co.jp/?lp={escapedlpurl}<br>Delivered URL by click on ad <br>http://www.yahoo.co.jp/?lp=http:%3A%2F%2Fwww.yahoo.co.jp%2F%3Fparam%3D1
escapedlpurl+2 | The Tracking URL including 'lpurl' (Landing Page URL), and available in the case of double encoding symbols of ":", "/", "?", "=", "%".| Landing Page URL<br>http://www.yahoo.co.jp/?param=1<br>Tracking URL<br>http://www.yahoo.co.jp/?lp={escapedlpurl+2}<br>Delivered URL by click on ad<br>http://www.yahoo.co.jp/?lp=http:%253A%252F%252Fwww.yahoo.co.jp%252F%253Fparam%253D1 
escapedlpurl+3 | The Tracking URL including 'lpurl' (Landing Page URL), and available in the case of triple encoding symbols of ":", "/", "?", "=", "%".| Landing Page URL<br>http://www.yahoo.co.jp/?param=1<br>Tracking URL<br>http://www.yahoo.co.jp/?lp={escapedlpurl+3}<br>Delivered URL by click on ad<br>http://www.yahoo.co.jp/?lp=http:%25253A%25252F%25252Fwww.yahoo.co.jp%25252F%25253Fparam%25253D1

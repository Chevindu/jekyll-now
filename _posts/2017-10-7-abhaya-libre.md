---
layout: post
title: Abhaya Libre භාවිතා කරන අයුරු
tags: abhaya libre sinhala unicode font usage
---

Abhaya Libre කියන්නේ අපි හැමෝම වගේ දැකලා තියෙන, පුෂ්පානන්ද ඒකනායක මහතාගෙ නිර්මාණයක් වන, **FM Abhaya** අකුරු මුහුණත පදනම් කරගත් නිර්මාණයක්. සිංහල යුනිකෝඩ් අක්ෂර වලට සහය දක්වන මේ අකුරු මුහුණත අපේ වෙබ්අඩවි වලට නොමිලේ, පහසුවෙන් සම්බන්ධ කරගන්න පුළුවන්. ඔයා දැන් කියවන මේ ලිපියේ භාවිතා වෙන්නෙත් Abhaya Libre අකුරු මුහුණත.

සාමාන්‍ය වෙබ්අඩවි සඳහා
---

Abhaya Libre සක්‍රිය කරගන්න ඕන වෙබ් පිටුවේ `<head>` ටැග් එක ඇතුළට, පහළ කේතනය පිටපත් කරන්න.

```html
<link href="https://fonts.googleapis.com/css?family=Abhaya+Libre" rel="stylesheet">
```
ඒ වෙබ් පිටුවට අදාළ CSS ගොනුවේ පහළ කේතනය පිටපත් කරන්න. `.sinhalapara` කියන සිලෙක්ටර් එක තමන්ට අවශ්‍ය පරිදි වෙනස්කරගන්න.

```css
body {
	font-family: 'Abhaya Libre', serif;
}
```

WordPress සඳහා
---

අද පාවිච්චි වෙන ගොඩක් තේමා (themes) වල Theme Options වලින්, අපිට අව‍ශ්‍ය Google Fonts මොනවද කියලා තෝරගන්න පුළුවන්. එහෙම පහසුකමක් තේමාවේ නැත්නම් අපිට ප්ලගිනයක් (plugin) හරහා මේ වැඩේ කරගන්නත් පුළුවන්. මම මෙතන පැහැදිලි කරන්නේ ප්ලගින පාවිච්චි නොකර, WordPress බ්ලොග් එකක Abhaya Libre ස්ථාපනය කරගන්න ක්‍රමය.

පළමු උපදෙස තමයි කවදාවත් සක්‍රියව තියෙන තේමාවක් edit කරන්න යන්නෙපා. මොකද එතකොට අපේ අතින් සුළු වැරැද්දක් වුණත් ඒක හරිගස්සන්න ගොඩක් අමාරුයි. ඒ නිසා සේරටම කලින් Child Theme එකක්[^first] හදාගෙන සක්‍රිය කරගන්න. 

Child theme එකක තියෙන ප්‍රධාන ගොනු දෙක තමයි `style.css` සහ `functions.php`. පළවෙනි වැඩේ මේ `functions.php` ගොනුව වෙනස් කිරීම. ඒක තියෙන්නේ **`wp-content > themes > your-theme`** කියන තැන. cPanel එක හරහා හෝ වෙනත් ක්‍රමයකින් විවෘත කරලා, මේ කේතනය `functions.php` ගොනුවට එක්කරන්න.

```php
function custom_google_fonts() {
	wp_enqueue_style( 'custom-google-fonts', 'https://fonts.googleapis.com/css?family=Abhaya+Libre:300,700', false );
 }
add_action( 'wp_enqueue_scripts', 'custom_google_fonts' );
``` 
ගොනුව save කරන්න අමතක කරන්නෙපා. 

දෙවෙනි වැඩේ `style.css` ගොනුව වෙනස්කිරීම. ඒක තියෙන්නෙත් `functions.php` තිබුණ තැනමයි. පහත කේතනය `style.css` වල යටින්ම එක්කරන්න.

```css
body {
	font: 20px 'Abhaya Libre', bodyfont, serif;
}
```
මේකත් save කරන්න.

දැන් වැඩේ ඉවරයි. මීට වඩා ලේසියෙන් Google Fonts ස්ථාපනය කරගන්න පුළුවන් ප්ලගිනයක් පාවිච්චි කළා නම්. හැබැයි සමහර ප්ලගින් Abhaya Libre වලට සහය දක්වන්නෙ නැහැ, මොකද ඒක මෑතකදි එක්කරපු අකුරු මුහුණතක් නිසා.




[^first]: Child themes සාදාගන්නා අයුරු [මෙතැනින්](https://premium.wpmudev.org/blog/how-to-create-wordpress-child-theme/) ඉගෙනගන්න.
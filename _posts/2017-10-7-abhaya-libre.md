---
layout: post
title: Abhaya Libre භාවිතා කරන අයුරු
tags: abhaya libre sinhala unicode font usage websites wordpress jekyll
lang: si_LK
---

Abhaya Libre කියන්නේ අපි හැමෝම වගේ දැකලා තියෙන, පුෂ්පානන්ද ඒකනායක මහතාගෙ නිර්මාණයක් වන, **FM Abhaya** අකුරු මුහුණත පදනම් කරගත් නිර්මාණයක්. සිංහල යුනිකෝඩ් අක්ෂර වලට සහය දක්වන මේ අකුරු මුහුණත අපේ වෙබ්අඩවි වලට නොමිලේ, පහසුවෙන් සම්බන්ධ කරගන්න පුළුවන්. ඔයා දැන් කියවන මේ ලිපියේ භාවිතා වෙන්නෙත් Abhaya Libre අකුරු මුහුණත.

මේ ලිපියට ප්‍රධාන කොටස් තුනයි:<br />
&nbsp;&nbsp;&nbsp;&nbsp;1. [සාමාන්‍ය වෙබ්අඩවි සඳහා](#සාමාන්ය-වෙබ්අඩවි-සඳහා)<br />
&nbsp;&nbsp;&nbsp;&nbsp;2. [WordPress සඳහා](#wordpress-සඳහා)<br />
&nbsp;&nbsp;&nbsp;&nbsp;3. [Jekyll සඳහා](#jekyll-සඳහා)

සාමාන්‍ය වෙබ්අඩවි සඳහා
---

Abhaya Libre සක්‍රිය කරගන්න ඕන HTML පිටුවේ `<head>` ටැග් එක ඇතුළට, පහළ කේතනය පිටපත් කරන්න.

{% highlight html %}
<link href="https://fonts.googleapis.com/css?family=Abhaya+Libre" rel="stylesheet">
{% endhighlight %}

ඒ වෙබ් පිටුවට අදාළ CSS ගොනුවේ පහළ කේතනය පිටපත් කරන්න.

{% highlight css %}
body {
	font-family: 'Abhaya Libre', serif;
}
{% endhighlight %}

WordPress සඳහා
---

අද පාවිච්චි වෙන ගොඩක් තේමා (themes) වල Theme Options වලින්, අපිට අව‍ශ්‍ය Google Fonts මොනවද කියලා තෝරගන්න පුළුවන්. එහෙම පහසුකමක් තේමාවේ නැත්නම් අපිට ප්ලගිනයක් (plugin) හරහා මේ වැඩේ කරගන්නත් පුළුවන්. මම මෙතන පැහැදිලි කරන්නේ ප්ලගින පාවිච්චි නොකර, WordPress බ්ලොග් එකක Abhaya Libre ස්ථාපනය කරගන්න ක්‍රමය.

පළමු උපදෙස තමයි කවදාවත් සක්‍රියව තියෙන තේමාවක් edit කරන්න යන්නෙපා. මොකද එතකොට අපේ අතින් සුළු වැරැද්දක් වුණත් ඒක හරිගස්සන්න ගොඩක් අමාරුයි. ඒ නිසා සේරටම කලින් Child Theme එකක් [ [^first] ] හදාගෙන සක්‍රිය කරගන්න. 

Child theme එකක තියෙන ප්‍රධාන ගොනු දෙක තමයි `style.css` සහ `functions.php`. පළවෙනි වැඩේ මේ `functions.php` ගොනුව වෙනස් කිරීම. ඒක තියෙන්නේ **`wp-content > themes > your-theme`** කියන තැන. cPanel එක හරහා හෝ වෙනත් ක්‍රමයකින් විවෘත කරලා, මේ කේතනය `functions.php` ගොනුවට එක්කරන්න.

{% highlight php %}
function custom_google_fonts() {
	wp_enqueue_style( 'custom-google-fonts', 'https://fonts.googleapis.com/css?family=Abhaya+Libre:300,700', false );
 }
add_action( 'wp_enqueue_scripts', 'custom_google_fonts' );
{% endhighlight %} 
ගොනුව save කරන්න අමතක කරන්නෙපා. 

දෙවෙනි වැඩේ `style.css` ගොනුව වෙනස්කිරීම. ඒක තියෙන්නෙත් `functions.php` තිබුණ තැනමයි. පහත කේතනය `style.css` වල යටින්ම එක්කරන්න.

{% highlight css %}
body {
	font: 20px 'Abhaya Libre', bodyfont, serif;
}
{% endhighlight %}

මේකත් save කරන්න.

දැන් වැඩේ ඉවරයි. මීට වඩා ලේසියෙන් Google Fonts ස්ථාපනය කරගන්න පුළුවන් ප්ලගිනයක් පාවිච්චි කළා නම්. හැබැයි සමහර ප්ලගින් Abhaya Libre වලට සහය දක්වන්නෙ නැහැ, මොකද ඒක මෑතකදි එක්කරපු අකුරු මුහුණතක් නිසා. මම පැහැදිලි කරපු ක්‍රමය අසාර්ථක නම්, පහලින් කොමෙන්ට් එකක් දාන්න.

Jekyll සඳහා
---

මගේ මේ බ්ලොග් එක GitHub Pages වල හොස්ට් කරපු, Jekyll හරහා ක්‍රියාකරන බ්ලොග් එකක්. මම මේකෙ Abhaya Libre පාවිච්චි කරපු විදිහ දැන් පැහැදිලි කරන්නම්.


මුල්ම වැඩේ `default.html` ගොනුව වෙනස්කිරීම. ඒක තියෙන්නෙ **`_layouts > default.html`** කියන තැන. `default.html` වල `<head>` ටැග් එක ඇතුළට මේ කේතය එකතුකරන්න.

{% highlight html %}
<link href='https://fonts.googleapis.com/css?family=Abhaya+Libre:400,700&amp;subset=sinhala' rel='stylesheet' type='text/css'>
{% endhighlight %}

ඊළඟ වැඩේ අපේ අකුරු මුහුණතට variable එකක් වෙන්කරගන්න එක. ඒක කරන්න **`_sass > _variables.scss`** වල තියෙන `_variables.scss` ගොනුවට මේ පේළිය එකතුකරන්න.

{% highlight scss %}
$abhaya: 'Abhaya Libre', serif;
{% endhighlight %}

දැන් අපිට කැමති විදිහට Abhaya Libre අකුරු මුහුණත පාවිච්චි කරන්න පුළුවන්. ඒ නිසා `style.scss` ගොනුවේ කැමති තැනකට අපි අර්ථදක්වපු variable එක පාවිච්චි කරන්න.
*උදා:*

{% highlight scss %}
body {
	background: $white;
	font: 18px/1.4 $abhaya;
	color: $darkGray;
}
{% endhighlight %}

Jekyll සඳහා මම අනුගමනය කළ පියවරවල් වැඩිය පැහැදිලි කරන්න උත්සාහ කළේ නැහැ, මොකද මමත් තාම අත-පත ගාන නිසා. හැබැයි කාටහරි දැනගන්න ඕන නම් ඒවා කළේ ඇයි කියලා, කොමෙන්ට් එකක් දාන්න. මම මේ ලිපිය විස්තරාත්මක කරන්නම්.

ජය! ✌️


[^first]: WordPress වල Child themes හදාගන්න විදිහ [මෙතැනින්](https://premium.wpmudev.org/blog/how-to-create-wordpress-child-theme/) ඉගෙනගන්න.
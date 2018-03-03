# Custom Outputs

<p>You can customise the default output styles that are registered by Delightful Downloads using the <code>dedo_get_styles</code> filter. This will allow you to add or remove output styles that are used by the <code>&#91;ddownload&#93;</code> shortcode and will also affect which output styles are shown by the shortcode generator. In addition, any custom outputs can be selected as the default style in the <em>Settings</em> screen under the <em>Shortcodes</em> tab.</p>

![]({{ "/images/custom-outputs-shortcodes.jpg" | absolute_url }})

![]({{ "/images/custom-outputs-settings.jpg" | absolute_url }})

<p>The following output styles are registered by default:</p>

{% gist dbbaebf7c9d8e69d43c8 defaults.php %}

<p>You will notice that various wildcards are used to enter dynamic content such as <code>%url%</code> and <code>%text%</code>. A full list of the available wildcards can be found <a title="Wildcards" href="{{ "/documentation/wildcards" | absolute_url }}">here</a>.</p>

<h2>Add Outputs</h2>

<p>To add a new output style to those already registered by Delightful Downloads simply add a new key to the <code>$styles</code> array:</p>

{% gist dbbaebf7c9d8e69d43c8 add.php %}

<p>To completely replace the default output styles simply overwrite the <code>$styles</code> array:</p>

{% gist dbbaebf7c9d8e69d43c8 overwrite.php %}

<p>You use a custom output like so, <code>&#91;ddownload id="123" style="icon_link"&#93;</code>.</p>

<h2>Remove Outputs</h2>

<p>Existing outputs can be removed by simply unsetting them. The following snippet will remove the plain text output:</p>

{% gist dbbaebf7c9d8e69d43c8 remove.php %}

<p>All of the above code snippets should be added to your theme's <code>function.php</code> file.</p>

<a href="{{ site.github.url }}">&lt; Back</a>
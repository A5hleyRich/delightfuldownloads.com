# Custom Buttons

<p>You can customize the default buttons that are registered by Delightful Downloads using the <code>dedo_get_buttons</code> filter. This will allow you to add or remove button styles that are used by the <code>&#91;ddownload&#93;</code> shortcode and will also affect which buttons are shown by the shortcode generator. In addition, any custom buttons can be selected as the default button style in the <em>Settings</em> screen under the <em>Shortcodes</em> tab.</p>

![Custom Lists Settings Screen]({{ "/images/custom-buttons-shortcodes.jpg" | absolute_url }})

![Custom Lists Settings Screen]({{ "/images/custom-buttons-settings.jpg" | absolute_url }})

<p>The following buttons are registered by default:</p>

{% gist 87d446a3ea9f577fc9ce defaults.php %}

<h2>Add Buttons</h2>

<p>To add a new button to those already registered by Delightful Downloads simply add a new key to the <code>$buttons</code> array:</p>

{% gist 87d446a3ea9f577fc9ce add.php %}

<p>To completely replace the default buttons simply overwrite the <code>$buttons</code> array:</p>

{% gist 87d446a3ea9f577fc9ce overwrite.php %}

<p>You use a custom button like so, <code>&#91;ddownload id="123" style="button" button="bright_pink"&#93;</code>. Remember that you will need to style the button using CSS and the class name <code>button-bright-pink</code>.</p>

<h2>Remove Buttons</h2>
<p>Existing buttons can be removed by simply unsetting them. The following snippet will remove the red and yellow buttons:</p>

{% gist 87d446a3ea9f577fc9ce remove.php %}

<p>All of the above code snippets should be added to your theme's <code>function.php</code> file.</p>
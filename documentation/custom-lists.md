# Custom Lists

You can customise the default list styles that are registered by Delightful Downloads using the <code>dedo_get_lists</code> filter. This will allow you to add or remove list styles that are used by the <code>[ddownload_list]</code> shortcode and will also affect which list styles can be selected as the default list style in the <em>Settings</em> screen under the <em>Shortcodes</em> tab.

<img src="https://delightfuldownloads.com/wp-content/uploads/2014/02/custom-list-settings.jpg" alt="Custom Lists Settings Screen" />
![Custom Lists Settings Screen](images/custom-list-settings.jpg)

The following list styles are registered by default:

{% gist ccbb933c1a62332b0f9c defaults.php %}

You will notice that various wildcards are used to enter dynamic content such as <code>%url%</code>, <code>%title%</code> and <code>%date%</code>. A full list of the available wildcards can be found <a title="Wildcards" href="documentation/wildcards">here</a>.

<h2>Add Lists</h2>
To add a new list style to those already registered by Delightful Downloads simply add a new key to the <code>$lists</code> array:

{% gist ccbb933c1a62332b0f9c add.php %}

To completely replace the default output styles simply overwrite the <code>$lists</code> array:

{% gist ccbb933c1a62332b0f9c overwrite.php %}

You use a custom list like so, <code>[ddownload_list style="icon_date"]</code>.

<h2>Remove Lists</h2>
Existing lists can be removed by simply unsetting them. The following snippet will remove the Title (File Size) list style:

{% gist ccbb933c1a62332b0f9c remove.php %}

All of the above code snippets should be added to your theme's <code>function.php</code> file.
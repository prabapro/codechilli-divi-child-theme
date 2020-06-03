## About this Child Theme
This is a child theme produced by the Elegant Market Place child theme maker. It is solely produced to work with the Divi theme by Elegant Themes.

#### v1.0. Social Icons:

Additional Social Icons for the header and footer can be optionally added to the four icons now controlled by the Divi theme. These additional icons are controlled within the Theme Customizer and `Divi Theme Options > General` in WP Admin.

To add addtional Social Icons to those offered in this child theme, the `includes/social_icons.php` can be edited by inserting additional code to that now appearing in this file. As an example, insert the following at a location of your choosing.

```
<?php endif; ?>

	<li class="et-social-icon et-social-newsocial">
		<a href="#" class="icon">
			<span>New Social</span>
		</a>
	</li>

<?php if ( 'on' === et_get_option( 'divi_show_tumblr_icon', 'on' ) ) : ?>
```

Substitute `newsocial` and `New Social` with appropriate naming. You will also need to create needed CSS to display the icon of choice. Currently, all social icons as displayed in this context are font glyphs. There are glyphs within the Divi Module font library that are not currently utilized in this context. You may choose from the following:

```
Tumbleupon	\e098
Wordpress	\e099
DeviantArt	\e09f
Share		\e0a0
Picassa		\e0a4
GoogleDrive	\e0a5
Blogger		\e0a7
Spotify		\e0a8
Delicious	\e0a9
```

To use any of the above, you'll need to insert the following and change `newsocial` to match what you've added above to the `style.css` file.
```
.et-social-newsocial a.icon:before {
	content: "\e0xx";
}
```

#### v1.1. No Sidebar

The `style.css` contains the snippet to remove sidebar from all the pages (`line 16 -30`). You may comment it out or remove if you need sidebar enabled.

#### v1.2. Removed "Enter coupon" prompt

"Enter Coupon" prompt will be removed from the Woocommerce check out page if the coupon is already been applied.

To disable this feature, remove/uncomment `lines 163-176` from `functions.php` file.

#### v1.3. Woocommerce CSS Fixes

Adjusted few Woocommerce elements (i,e, Buttons, Coupon field height etc) to go with the theme.
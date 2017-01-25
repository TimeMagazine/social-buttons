Social Microshare Buttons
==============

v0.0.5

Customizable social media buttons for microsharing content on Twitter, Facebook, LinkedIn and Pinterest, compiled with Browserify.

First, install this repo as a Node module:

	npm install TimeMagazine/social-buttons

	var social = require("social-buttons");

	var fb = social.facebook(_your_facebook_app_id_);
	var tw = social.twitter();
	var li = social.linkedin();
	var pn = social.pinterest();

You can either make your own buttons or use the ones in the [template.html](https://github.com/TimeMagazine/social-buttons/blob/master/template.html), which include [some styling](https://github.com/TimeMagazine/social-buttons/blob/master/styles.less);

### Custom share example

	$("body").on("click", "#fbbutton", function() {
		fb.share({
			title: "I got Carmela on this @TIME quiz!",
			description: "See which member of the Sopranos you are.",
			image: "https://upload.wikimedia.org/wikipedia/en/2/25/CarmelaSoprano.jpg"
			link: "http://time.com/sopranosquiz" // not a real thing
		});
	});

Every social function takes a `title` argument and an optional `link` argument. *The URL to the page will automatically be used for `link`  if none is otherwise provided.* Facebook and LinkedIn can take a `description` field as well while Facebook and Pinterest require an `image` argument as a URL.
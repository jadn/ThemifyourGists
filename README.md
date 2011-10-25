#Gist-Embed-CSS-Themes
>What I am hoping to create are stylesheets overriding the colors of embedded Gists.

>-Izzy

##Bored of the usual syntax highlighting theme of embedded Gists?
We have got some alternative solutions for your embedded Gists. Currently there are **7** themes:

+	Oblivion
+	black 'n' white* 
+	fruity*
+	monokai*
+	native*
+	pastie*
+	tango*

But as always you are free to contribute to/fork the project. Any help is appreciated!

*borrowed from [Pygment](http://pygments.org/ "")

##Getting started
Just put this script tag at the end of the body:

	<script type="text/javascript">
	var newthemeurl = "raw.github.com/iglvzx/Gist-Embed-CSS-Themes/master/Gist.Oblivion.css",
    	giststandardtheme, newgistheme;

	function embeddedGistheme(newthemeurl) {
    	giststandardtheme = "<link rel='stylesheet' href='https://gist.github.com/stylesheets/gist/embed.css'/>";
    	newgistheme = giststandardtheme.replace(/gist.github.com\/stylesheets\/gist\/embed.css/g, newthemeurl);

    	document.write(newgistheme);
	}
	embeddedGistheme(newthemeurl);
	</script>
And you are ready to go.. oh, wait. Maybe you would like to use another theme then Oblivion? That's a piece of cake, replace your URL *yourURL.com/mygistheme.css* with *newthemeurl* and delete *newthemeurl = raw.github[…],*!

Now it should look like this:
	
	var giststandardtheme, newgistheme;

	function embeddedGistheme(newthemeurl) {
    	giststandardtheme = "<link rel='stylesheet' href='https://gist.github.com/stylesheets/gist/embed.css'/>";
    	newgistheme = giststandardtheme.replace(/gist.github.com\/stylesheets\/gist\/embed.css/g, newthemeurl);

    	document.write(newgistheme);
	}
	embeddedGistheme("yourURL.com/mygistheme.css");

**Ta-da!** It's all done.

##In the future
The *founder* of this project, Izzy, primarily wishes to port existing GtkSourceView themes and Vim themes to the Gist embed.css stucture.

Myself would like to have only **ONE** JavaScript file instead of this one and the one served from *Github->Embed*. Because presently it is rather a hack than a serious solution.

-Geeky Robo
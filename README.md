# CSS-and-JS

Contains CSS and JS files hopefully do some useful stuff. 

## MAL List: 
**File:** [MALTable/malTable.css](MALTable/malTable.css)

**Description:** A CSS copy of the [My Anime List's](http://myanimelist.net/) original table for a user's list of animes. A sample of what it imitates can be found [here](MALTable/MALImage.png). A sample file *using* the CSS can be found [here](MALTable/sample_for_malTable.html).

Right now, My Anime List allows users to generate custom themes. However, I liked the original theme and I created the `malTable.css` file so that I could use it for any `<table>` that I make.

**To Use: For Noobs**

To include, basically add to your `index.html` file: 

	<link rel="stylesheet" href="malTable.css">

e.g.

```
<html>
	<head>
		<link rel="stylesheet" href="malTable.css">
		...
	</head>
	...
</html>

```
Obviously, this only works if you put it in the root directory (the same directory as your `.html` file. Change the `href` value based on where you place the file.

**Tips:** 

1. The CSS will overwrite tags such as `<html>`, `<body>` , `<table>`, `<p>`, `<a>`, `<tr>`, `<td>` and `<th>`. 

2. You should therefore use it on a separate `.html` page. Otherwise, you will have to modify the CSS to make a `#section` or prefix it under a class. Not worth the effort.

3. For the table's title, use the `table-title` class:
	
		<p class="table-title">The Table Title</p>

4. The div that *contains* the table, use the `tdiv` class: 

		<div align="center" class="tdiv">	

5. The table tag *should* have `cellspacing` and `cellpadding` manually added to it: 

		<table cellspacing="0" cellpadding="0">

6. You can modify the [sample](MALTable/sample_for_malTable.html) file after downloading the project.
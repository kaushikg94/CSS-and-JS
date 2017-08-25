# CSS-and-JS

Contains CSS and JS files that do things that I find useful.

##### Table of Contents  
* [MAL List](##MAL-List)  
* [Programming Langague SVGs](##Programming-Langague-SVGs)  
* [Incomplete](#Incomplete)


## MAL List: 
**File:** [MALTable/malTable.css](MALTable/malTable.css)

**Description:** A CSS copy of the [My Anime List's](http://myanimelist.net/) original table for a user's list of animes. A sample of what it intends to imitate can be found [here](MALTable/MALImage.png). A sample file *using* the CSS can be found [here](MALTable/sample_for_malTable.html).

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

## Programming Language SVGs: 

**Folder:** [PLangSVGs/svg](PLangSVGs/svg)

**Description:** A file containing SVGs for different programming languages and file types. They are square in size, with a black fill and transparent content. A sample file using the SVGs is available [here](PLangSVGs/sample_for_PLangSVGs.html).

I create them to use for my [personal website](http://kaushikg94.github.io). They replace the text containing the list of programming languages used in my [--projects list](http://kaushikg94.github.io/projects.html). 

**Story Time:**

* My initial goal was to create font icons (the `<i>...</i>` stuff). They're very popular, easy to use and are available on any [bootstrap](http://getbootstrap.com) based website. 
* However, I am not using bootstrap, and my preference (and the preference of any web developer) is to use local resources (or at least have a copy of them on your local server).
* Therefore, I decided to create my own icon, and make font icons out of them. The process seemed tedious, and reliant on external websites: 
	* I had to make an `.svg` file.
	* Upload the file to a [website](https://icomoon.io) that created the font.
	* Download the font from them.
	* Include a CSS file (that contained the `@fontface` information).
* Everytime I wanted to add an icon to the existing set, I would have to go through this process and upload the *whole* set of `.svg` files!
* Since `.svg` files could be included directly in to the `.html` file as a tag, I decided to use them directly with the `<object>` tag. The `.svg` files can be created and added standalone when needed.
* However, `.svg` files can be tricky to use. Changing colors and using `font-weight` on them doesnt' work unless their paths are grouped. 
* My website is using a black-and-white theme, and this isn't a problem (yet).

**To Use: For Noobs**

I've included a [sample file](PLangSVGs/sample_for_PLangSVGs.html) that uses most of the SVGs I've created. You can skip right to it and see how it's done.

There are many ways to include `.svg` files in HTML. 

* One way is to use the `<svg>..</svg>` tags directly on the page.
* However, I prefer using them in the `<objects>` tag instead. 
	* Using this, you can save the `.svg` files in a separate location (hint: inside a folder named svg), and call them when needed. 
	* It keeps the `.html` file clean whth only the necessary content being shown.  

Here's how to do it: 

```
<html>
    <head>...</head>
    ...
	<body>
		<object
			data = "location/of/the/file.svg"
			width = "width of the svg so it doesn't oveflow the page"
		</object>
	</body>

</html>

```
That's pretty much it.


#Incomplete

## Projects List: 

**File:** Not there

## Using SheetJS's JS-XLSX to Table

**File:** Not there

**Description:** [SheetJS/JS-XLSX]() is a library that can take an MS Excel workbook (`.xls`, `.xlsx`) and generate a JS object. This JS object can be queried and modified, in turn modifying the worbook. 

I have used this **amazing** library to act as a data source and fill in tables, lists, etc. on my [personal webpage](). I'm sharing the functions.

**Story Time:** 

* I obtained the idea when I wanted to be able to make tables in Excel and use them in my [personal webpage](). 
* I stumbled upon [SheetJS/JS-XLS](), a precursor to the XLSX library, where a clear and easy example to query an MS Excel sheet was given.
* I then made some [simple functions]() that took the Excel Sheet and based on the Row/Column info, and placed it where I wanted on my HTML page.

**Why:**

* The use of `.xlsx` file format makes it easier to create, store and modify data using MS Excel GUI. Basically, everybody can use MS Excel. 
* The `.xlsx` format is also more suited to editing than `.json` and `.xml` which are suited for data transfer.
* An alternative to using files were to write every table, row and column in HTML tags. I could have used one of many webpages that give you a `<table>` UI. You fill in the content, and it spits out HTML `<table`> code. This will become tedious to edit and also make me rely on 3rd party websites. 
* Another alternative is to make a server with a SQL database. This is probably the most popular, industry used method. It requires learning how to setup and use SQL. It seems live overkill for a small-to-medium sized website (which is what I expect to be building as a lone developer).

**To Use: For Noobs**
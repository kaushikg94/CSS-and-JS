# CSS-and-JS

Contains CSS and JS files that do things that I find useful.

#Completed

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

#Incomplete

## Projects List: 

**File:** Not there

## Square-Box Programming Language Icons: 

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
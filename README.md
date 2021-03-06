hoisin.scss
===========

A simple responsive mini framework to kick start your project, written in Sass. Please note that this project does not include any predefined styling or premade components. We aim to create an organised base from you can create your own library instead of a one-size-fits-all solution.

We did not include a reset since we believe they are not necessary, we encourage you to define the styles you need for your project, and leave the unstyled elements to the browser.

## Usage
Open the _vars.scss file and add your variables to it, including the size of your base grid. You can add any variables you will be using like colors, font files, sizes, etc.

	// Grid
	$col-qty: 			12;   // Amount of columns
	$col-width: 		60px; // Width of column
	$gutter:			20px; // Width of gutters

### Grid
By default we use a 12 column grid with 60px columns and 20px gutters. The spans have simple names like `".col4"`. There are helper classes like `".colr"` to pull a span to the right, and `".pre1"` to `".pre10"` as well as `".suf1"` to `".suf10"` for offset spans.

Tablet and mobile spans can be altered by using extra helper classes depending on the layout requirements, we've included classes for full, half one third and two thirds (widths) which override default column behaviour. We also added a `".clear"` helper class for browsers that can't clear themselves out.

Example of a typical layout:

	<div class="container">
	    <div class="col8 two-third-tab">
	    	<p>Your content here</p>
	    </div>
	    <div class="col4 one-third-tab">
	    	<p>Your sidebar here</p>
	    </div>	    
	<div>

See index.html file for more examples.

### Mixins
We have included a mixins file with all common mixins we use everyday. This file doesn't output anything by itself, so it's safe to include in every file so the mixins are always available.

### File structure
We advise to create one file for each individual section / size and place it in ts respective folder. All files will compile to two main stylesheets and a IE fallback stylesheet that should include all desktop size styles.

To keep it organised, you can add one file for each section, and add common styles for each device to the base.scss file of each device folder. Common styles across the site should go in styles.scss.
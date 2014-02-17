Semantic grid helper mixins
===========================

Responsive layout Less helper mixins, to be used with [Semantic grid system][ref1].

##Demo

A simple responsive example with column widths changing at different breakpoints.

[Demo][ref2]

##Requirements

These mixins are to be used with [Semantic grid system][ref1]. 

[Less css][ref3] is also required.

## Mixins

All mixins are namespaced in `#grid`.

**.setGridWidths(largeColUnits, desktopColUnits, tabletColUnits, mobileColUnits)**

Sets the column units for four common breakpoints using predefined column widths, gutter widths and column numbers.

Example:

	// Sets column units for 4 breakpoints. 
	// 6 columns, 8 columns, 1 columns & 3 columns.
    .col1 {
		#grid > .setGridWidths(6, 8, 1, 3); 
    }

**.extraLargeGrid(units, pushOffset, pullOffset)**

Sets the column units, push and pull offset for the predefined `extra large` mediaquery breakpoint.

Example:

	// Sets column units for extra large breakpoint.
	// 3 columns, push offset 1, pull offset 0.
	.col1 {
		#grid > .extraLargeGrid(3, 1, 0);
	}

**.desktopGrid(units, pushOffset, pullOffset)**

Sets the column units, push and pull offset for the predefined `desktop` mediaquery breakpoint.

Example:

	// Sets column units for desktop breakpoint.
	// 3 columns, push offset 1, pull offset 0.
	.col1 {
		#grid > .desktopGrid(3, 1, 0);
	}

**.tabletGrid(units, pushOffset, pullOffset)**

Sets the column units, push and pull offset for the predefined `tablet` mediaquery breakpoint.

Example: 

	// Sets column units for tablet breakpoint.
	// 3 columns, push offset 1, pull offset 0.
	.col1 {
		#grid > .tabletGrid(3, 1, 0);
	}

**.mobileGrid(units, pushOffset, pullOffset)**

Example:

	// Sets column units for mobile breakpoint.
	// 3 columns, push offset 1, pull offset 0.
	.col1 {
		#grid > .mobileGrid(3, 1, 0);
	}

**.customGrid(mediaQuery, columnWidth, gutterWidth, units, pushOffset, pullOffset)**

Allows you to define the column width, gutter width and breakpoint as well as the column units, push and pull offset.

	// Sets column units and widths for a custom breakpoint.	
	@mq: ~"only screen and (max-width: 350px)";
	.col1 {		
		#grid > .customGrid(@mq, 32, 10, 8, 0, 0);
	}

[ref1]:http://semantic.gs/
[ref2]:http://demo.iambacon.co.uk/semantic-grid-helper/demo
[ref3]:http://lesscss.org/
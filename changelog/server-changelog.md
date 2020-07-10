# Server Changelog

## 1.1

### 1.1.0 (2020/07/13)

Important changes and new features:

* Formula can use other formula columns
* Add favorite category to list starred bases
* Link columns and formula columns can be used in filters and groupbys
* Forms support conditional fields and required fields

Improvements and fixes:

* Support use multiple numeric columns in a single chart
* Support importing new data to an existing table
* Many other UI fixes and improvements

## 1.0

### 1.0.0 (2020/06/02)

Important changes and new features:

* Function column can show a specific column of a linked row
* Function column support rollup a specific column linked rows, for example, you can display the average number or maximum number of linked rows
* You can create multiple columns in the same table to link the same other table multiple
* Support using function column for grouping, filter and sort
* You can specify the decimal separator and thousand separator for number columns (for example, 100.000.000,00 in European way)

Improvements and fixes:

* The summary column in the bottom of the page can show the average, minimum, maximum of the corresponding columns
* Support using a custom URL for external links
* Support setting expire time and password for invitation links
* Support add images in comments
* Show image thumbnails in file column
* Support drag and drop multiple files in file column
* Support use arrows to select an item in select column, multi-select column, collaborator column and link column
* Other UI fixes

## 0.9

### 0.9.8 (2020/05/10)

Important changes and new features:

* Column type conversion improvement: After converting the type, try to save the data of the previous type, and you can undo (Ctrl + z) to return to the previous step.
* Long text improvements:
  * Preview can display the number of task list.
  * Solved the problem that when the long text content has only one picture, the mouse cannot move below the picture.
  * Removed the occasional asterisk in the long text preview display.
  * Fixed the problem of enlarged display of pictures in long texts.  
  * Solved the problem of missing line breaks when copying and pasting from Notepad into a long text editor.
  * Fix the problem of copying a link in long text.
* Added the function of dragging and filling (similar to the function in Excel).
* Support sharing a base to a group.
* More shortcut keys have been added, and help documentation for shortcut keys has also been added.
* Optimized grouping rendering, now if there are hundreds of entries in a group, it will not cause slow display.

Improvements and fixes:

* You can filter and group "Creator" type columns and "Address" type columns. 
* Provide the function of rotating the picture, which is used to correct the problem that the photos uploaded by some mobile phones are displayed upside down.
* Fixed the problem of importing CSV files.
* Added date calculation function, such as getting a date + 3 days later (dateadd function).
* You can star a base (in the download menu of the base).
* The number of comments in the last three days is directly displayed at the edge of each row in the table. Click to open the comment sidebar.
* You can create a link column that link to the same table the link column in.
* Other UI fixes

### 0.9.7 (2020/04/09)

Important changes and new features:

* Change terms: "table" to "base", and "sub-table" to "table"
* Search in all tables
* Formula column improvement: Add available formula list and examples when creating a formula column
* Comments improvement:  Now there is a right side panel for commenting a row. '@' will popup a candidates list, and the people in the collaboration fields of that row will appear at the top of the list.
* Support putting a plugin to top toolbar and installing plugin from plugin market

Improvements and fixes:

* Add smart copy feature, when you copy from one table to another, columns will be copied to the columns with same name and type regardless of the orders 
* Add hint for the first column that the column can't be deleted or moved
* Enable inserting column at the right side or left side of current column
* Add "mark all as read" in notification popup 
* Import data via CSV
* Add a new formula 'Value' to calculate a number from a string
* \[chart] Show the corresponding records when click an item in pivot table or chart
* \[chart] Enable stack mode in bar chart
* Improve handing of large file uploading
* Sort, filter and group by last modified time column
* Add share button in  **base** page
* \[fix] Fix linking to other records when converting a column type to link
* Enable getting notification about the table changes
* Add sharing links management in admin panel
* Improve number column format when exporting to excel
* Group members now can't create/rename/delete a base
* Python API now support getting notifications when a base changed

### 0.9.6 (2020/03/12)

New features

* External links for tables
* Two new column types: Last modifier and last modified time

Improvements and fixes

* Performance improvements when scrolling in a table
* Admin can restore deleted tables within 30 days
* Table can be copied to another group
* \[form] Automatically save form settings
* \[form] Remove column icons to make the UI clean
* \[form] Support add note to the form
* \[form] Fix support for selection column
* Support group/filter/sort by create time column
* \[fix] Fix viewing of a snapshot
* \[fix] Fix search
* \[fix] Fix table horizon scroll in iOS Safari
* \[fix] Fix editing of check column type

### 0.9.5 (2020/02/18)

Improvements and fixes

* \[form] Support getting notifications when forms are submitted
* \[form] Support restrict forms to accessed only by login users or specific group members
* \[chart] Support grouping in chart
* \[chart] Support using function field in chart or pivot table
* \[chart] Support export pivot table into a new sub-table
* \[chart] A chart or a pivot table can be expanded to be shown in a larger dialog
* \[chart] Automatically saving chart settings in chart dialog instead of manually click "save" button
* \[Calendar] Support year view
* Support deleting a group
* Improved exporting to Excel
* Using thumbnails of images in grid view instead of using the original images to improve loading speed
* Support setting a description for a table
* Docker image improvement and fixes
* Other bug fixes and UI improvements

New features

* UI plugins
* A feature called common datasets
* Row comments and modification history
* Two new column types: Creator and Created time
* Export a table to .dtable format and import a table from a .dtable file

### 0.9.4 (2020/01/08)

* Support export to Excel
* Support add record in calendar view
* List dtable snapshots
* Form improvement
* Improve activities
* Improve system admin functions 
* Other UI improvements and bug fixes

### 0.9.3 (2019/12/26)

* Initial release



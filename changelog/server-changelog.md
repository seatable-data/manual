# Server Changelog

## 1.4

### 1.4.0 (2020/11/10)

* [Added] “Help and resources” in the navigation
* [Added] Allow user to copy a base into the current group
* [Added] Auto fill and reminding function in form for several previous submissions
* [Added] Base description (if not empty) is displayed on first time opening of a base
* [Added] Column related operations to the Python API
* [Added] Computing indirectly linked records
* [Added] Customizable sharing permission (API)
* [Added] Delete current record function on mobile row details page
* [Added] Delimiter detection by CSV import
* [Added] Group admin can modify group members’ roles
* [Added] Help button on the top right corner of the base editor
* [Added] Illegal symbol replacement by Excel export
* [Added] Link to user manual in the Help and Help and resources menu
* [Added] Number of Sorts
* [Added] Role permission to run Python scripts
* [Added] Scripts can be created in JavaScript or Python
* [Added] Scripts import support for Python file
* [Added] Single select options quotation in the formula
* [Added] Sort for the collaborator column type
* [Added] URL column type
* [Added] Webhook support
* [Added] Function hour() to calculate time difference in hours
* [Fixed] Auto number sequence problem when using Shift+Enter to create new rows
* [Fixed] Conflict between Timeline plug-in and other plug-ins
* [Fixed] Current cell won’t be updated when a related row has been updated
* [Fixed] Display problem with vertical scroll bar
* [Fixed] Feedback wording error when submitting a form in English
* [Fixed] File unzip problem after downloading all images
* [Fixed] Formula column and number column format display problem on mobile devices
* [Fixed] Formula column display problem on row details page
* [Fixed] Frozen first column ‘shakes’ when scrolling left and right
* [Fixed] Key combination Ctrl+F triggers browser search instead of base editor search
* [Fixed] Missing decimal and thousands separator in number and formula column settings on mobile devices
* [Fixed] month() function problem under European time format
* [Fixed] No results displayed when adding new numeric columns in statistics
* [Fixed] Notification triggered by rules not displayed on mobile devices
* [Fixed] Problem with the focus when a row is changed in a filtered table
* [Fixed] Row displacement problem when modifiying long text while another record is added/removed
* [Fixed ]Scroll and select problem with table elements
* [Fixed] Search field functionality and width problem
* [Fixed] Spaces removal before and after text when submitting a form entry
* [Fixed] Removed Limitation of 99 images when uploading via copy & paste
* [Updated] Changed ‘===’ in the if() formula into ‘=’
* [Updated] Error handling (e.g. illegal symbol replacement) when exporting to Excel
* [Updated] Improved cell and grid rendering
* [Updated] Line break inside a table cell in the long text editor disabled
* [Updated] Modification notification via email improved
* [Updated] networkdays(startDate, endDate) function now includes ‘endDate’ in the result
* [Updated] Newly built Activities
* [Updated] Real-time display of messages in the row comment window
* [Updated] Searching and choosing mode of linked records
* [Updated] UI improvements for the + button in image and file cells

## 1.3

### 1.3.0 (2020/09/23)

Important changes and new features:

* You can write scripts in JavaScript to handling data in a base
* **Conditional formatting**: On the view control panel, there’s a new button: Color. You can set row colors according to a single select column or your own conditions and rules.
* **Print function**: Now you can print your SeaTable base or a single row in a much more elegant and compact way.
* **Auto number column type**: Set up a rule and let SeaTable number this column automatically.

Improvements and fixes:

* Collapse and expand all groupbys with one click
* Customizable SeaTable docker gunicorn configuration
* Groups listed in the bases library navigation
* More view modals for mobile terminal (Grid view and cards view)
* URLs in long text columns clickable in grid view
* \[fix] Bug when filtering over formula and link column and when filter condition is OR
* \[fix] Content of linked fields cannot be copy-pasted
* \[fix] Copy & paste, and drag & drop compatibility problem under Firefox
* \[fix] Form note content loss after hiding and unhiding
* \[fix] Formula column content update problem on the row details page
* \[fix] Locked table headers become unlocked when restarting server
* \[fix] Minus before formula result if result is decimal
* \[fix] Unintended focus switching in form view
* Date dialog in form with minutes automatically quits after selecting date and minutes
* Improved descriptions of round, roundup and rounddown formulas
* Monday will be the first day of a week in the sort/groupby conditions
* Forms can be exported, imported and copied with a base
* Form “submit” button changed into spiral after clicking to prevent resubmission
* A group can only be deleted when there’s no bases in it
* Remove “Unselect rows”, as clicking outside the selection cancels the selection
* Font blur problem in Chrome engine browsers under Windows
* Buttons to switch to previous/next row on the row details popover
* Functions findMax and findMin
* Notification when a user is added as a collaborator

## 1.2

### 1.2.0 (2020/08/18)

Important changes and new features:

* Calendar is re-implemented as a plugin
* You can change the color and icon for a base now
* Performance improvement when there are 40+ columns in a table

Improvements and fixes:

* Allow to duplicate views just like the tables
* Zip download files in a column
* Fix notification rules
* Plugin dialogs now have unique URLs for sharing
* You can set number format for formula columns that have results of number type
* Fix UI issues for forms
* Add rate limit for API calls
* Fix more bugs when exporting a view as an Excel
* You can now export/import options for a label column
* Other UI improvements

## 1.1

### 1.1.0 (2020/07/13)

Important changes and new features:

* Plugin system are redesigned. Plugins are now installed by system admins and users can choose which plugins to active for their bases. Normal users can not install plugins directly.
* Formula can use other formula columns
* Link columns and formula columns can be used in filters and groupbys
* Forms support conditional fields and required fields

Improvements and fixes:

* Support use multiple numeric columns in a single chart
* Support importing new data to an existing table
* Add favorite category to list starred bases
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



## 2/6 ~ 2/10

- [Firefox]
	- [UI feedback] [Bug 285836](https://bugzilla.mozilla.org/show_bug.cgi?id=285836) - Make "Remove All Cookies Now" undoable
		- Got UX feedback, will make a few changes to the patch

- [Date-time Picker]
	- [Bug 1283381](https://bugzilla.mozilla.org/show_bug.cgi?id=1283381) - [meta] Implement UI for date time input types
		- [Bug 1320647](https://bugzilla.mozilla.org/show_bug.cgi?id=1320647) -  [DateTimePicker] Add min/max and step support to date picker
			- UX spec changed, editing patch to align with new behaviors before asking for review
		- [Bug 1328219](https://bugzilla.mozilla.org/show_bug.cgi?id=1328219) - [DateTimePicker] Add browser chrome test for date picker
			- Based on master schedule plans, will work on this after features have been landed.
		- [Bug 1329927](https://bugzilla.mozilla.org/show_bug.cgi?id=1329927) - [DateTimePicker] Get localized calendar terms for date picker using Intl.getDisplayNames
			- r? for :mconley
			- r+ from :gandalf
		- [Bug 1337319](https://bugzilla.mozilla.org/show_bug.cgi?id=1337319) - [DateTimePicker] The order of year and month on date picker should depend on locale datetime format
- [Form Autofill]
	-  [Bug 1304306](https://bugzilla.mozilla.org/show_bug.cgi?id=1304306) - Need to have a place in the Preference -> Setting for users to launch the profile list add/edit/remove dialog
		-  landed
	-  [Bug 1299819](https://bugzilla.mozilla.org/show_bug.cgi?id=1299819) - [Form Autofill] Allow users to manually add form autofill profiles
		- exploring different options for making nested subdialogs in preferences
	- Investigating on making profile preview work

#### Date Time Pickers Tasks:

- General features
	- [Done] Passing data between input field and pickers
	- [Hold] Keyboard Controls
		- To be implemented in follow up bugs
		- Input box handles keyboard events most of the time, until user triggers shifting "visual focus" to picker
- Month picker
	- [Done] Spinner component (basic functionalities)
	- [Hold] Spinners are combined when indivisible step is used
		- UX considering removing this from the spec
- Time picker
	- [Done] AM/PM component
	- [Done] Spinner cycle feature
	- [Done] Spinner scroll snap even with few items
	- [Done] Extract time state handling into a module
	- [Done] Changed how updates are handled to make sure it works for years
	- [Done] Integrate with input boxes
	- [Done] Out of range items are displayed but greyed out
	- [Done] Fix panel arrow position
- Date picker
	- [Done] Basic calendar component
		- Display calendar in 6 week rows
		- First day of the week & weekends configurable
		- Apply basic styling
	- [Done] Add max and min features
		- Dates earlier than min or later than max are greyed out
		- Out of range years are not displayed, and months are greyed out
	- Add step features
		- Off step items are greyed out
	- Transition animation
		- Animation for previous and next month
		- Animation for opening picker
- Week picker
	- Calendar week feature
- Datetime picker
	- Combining date picker and time picker

- Full L10n support
	- Getting localized strings with Intl API
	- Get calendar info with Intl API
	- Spinner orders depend on locale
- Full a11y support
	- Tab focus
	- Alt text & ARIA

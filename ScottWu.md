## 2/20 ~ 2/24

- [Firefox]
	- [UI feedback] [Bug 285836](https://bugzilla.mozilla.org/show_bug.cgi?id=285836) - Make "Remove All Cookies Now" undoable
		- Got UX feedback, will make a few changes to the patch

- [Date-time Picker]
	- [Bug 1283381](https://bugzilla.mozilla.org/show_bug.cgi?id=1283381) - [meta] Implement UI for date time input types
		- [Bug 1320647](https://bugzilla.mozilla.org/show_bug.cgi?id=1320647) -  [DateTimePicker] Add min/max and step support to date picker
			- UX spec changed, editing patch to align with new behaviors before asking for review
		- [Bug 1328219](https://bugzilla.mozilla.org/show_bug.cgi?id=1328219) - [DateTimePicker] Add browser chrome test for date picker
			- Based on master schedule plans, will work on this after features have been landed.
		- [Bug 1320880](https://bugzilla.mozilla.org/show_bug.cgi?id=1320880) - [DateTimePicker] Add RTL support to date picker
			- r+ from :mconley
			- landed
- [Form Autofill]
	- [Bug 1019471](https://bugzilla.mozilla.org/show_bug.cgi?id=1019471) - (fx-autofill-profile-edit) Dialog to add/edit/view an autofill profile
		- r? MattN
		- addressed issues from first review
	- [Bug 1019483](https://bugzilla.mozilla.org/show_bug.cgi?id=1019483) - (fx-autofill-profile-mgmt) Interface to manage autofill profiles
		- Working on the manage profiles interface while waiting for Bug 1019471 review
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
	- [done] Getting localized strings with Intl API
	- [done] Get calendar info with Intl API
	- [done] Spinner orders depend on locale
- Full a11y support
	- Tab focus
	- Alt text & ARIA

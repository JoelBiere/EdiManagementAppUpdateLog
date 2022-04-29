# EdiManagementAppUpdateLog# Edi Management App V.1.1

## New Feature: Rules!

In the UI navigate to the new Admin Dashboard where -- if you have admin status -- we'll have a page of goodies.



A new sidebar will host navigation between these goodies. We have plans to make many of these new tools and features functioning pages -- but currently the only functioning goodie is the **Auto-Complete** rule. Though there are plans to add new rules such as *Auto-validate* and *Auto-Assign*.

![image](https://user-images.githubusercontent.com/76972193/165984730-92ecf0f2-83be-447f-91aa-3788f929ff0c.png)


Rules will operate much in the same way that your Microsoft Outlook Rules do. They help to automate the massive amounts of incoming messages that we get. We are going to catch incoming errors sent to the management on the front end and take an action on them -- before they even populate our database. 

Each rule type is given its own page and will populate a table of existing rules that we have in our database of that rule type. You can take actions on each rule including

- Run Now
    - This will execute that rule on existing errors that match the rules conditions
- Activate/Deactivate
    - This will turn a rule off and on. If the rule is off -- the actions will not be taken on incoming errors
- Delete
    - self-explanitory

### Add a rule



To add a rule click the _Add Rule_ button

1. Provide the error message of the errors you'd like this rule to apply to **IMORTANT
This must be an exact string match.**

2. Give it a rule-type. What action are we going to be taking on these error messages?

3. Flip the active/deactive switch to what you'd like it to be. 

4. Your username is going to be attached to the rule (we are tracking you :wink: )

![AddRule](https://user-images.githubusercontent.com/76972193/165984534-8ac6fc50-642b-4fbf-8296-27dc2792b1b1.gif)

After adding the rule -- you'll see it populated in the table and incoming errors that match an activated rule will have the rule executed on it.

## Other Changes
- Errors in the dashboard are now default sorted by most recent at the top
- Added a filtering criteria of _DOES NOT CONTAIN_ for string-based fields
- Added filtering/sorting abilites for the **Customer Reference** , **Duplicate Count**, and **Has Validation** fields.
- Added a copy button for error messages to copy messages to your clipboard
- If a duplicate error was posted but its original was marked as solved - the incoming duplicate is treated as a new unsolved error and DOES NOT increment the duplicate count of the original.

## Bug Fixes
- Fixed an issue where error metrics were not updating when switching OpCos
- Fixed an *Index Out of Bounds* issue where if there were 0 matching errors Java was doing unneccessary work

Update log for the edi-managmeent-app

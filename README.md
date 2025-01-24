# Dynamic (re)binding of variable

CreateBinding built-in function is used to dnyamically rebind control (PLC) variable, to a param_1 property of a custom element, [hmi/UserControls/demo_control.usercontrol]().
Action is triggered by TcHmiCombobox_2 element's onSelectionChanged action on [hmi/Pages/StartPage.content](). Action simply gets currently selected value from the dropdown and via a case structure binds a new variable using [CreateBinding](https://infosys.beckhoff.com/english.php?content=../content/1033/te2000_tc3_hmi_engineering/5097942027.html&id=)

# Localization of the Back button in navigation menu

"Back" button on the navigation menu is only localized to de and en by default. In order to add a new language, following steps must be taken:
* Edit the "language" node of the json file of the hmi package itself - [Packages/Beckhoff.TwinCAT.HMI.BaseTemplate.12.762.46/runtimes/native1.12-tchmi/TcHmiNavigation/Description.json]() to add the "sl": "Lang/sl.json" key for sl language
* Add the sl.json file inside Lang subfolder, copying any of existing should do.
(none of those files are included in this repo, as it is ignored, sample is for version )


# Tested

Tested on 1.12.762.46 , other versions will have to have the Packages folder changed.

--install:
sudo python3 setup.py install --prefix=/usr


--for test:
meld /home/tatiana/projects/github/meld/examples/c_v11.lang /home/tatiana/projects/github/meld/examples/c_v12.lang
meld /home/tatiana/projects/github/meld/examples/c_v21.lang /home/tatiana/projects/github/meld/examples/c_v22.lang


-------------------------------------------------------
--rename file-filter items:

--ui:
CustomFilterMenu				-> FileFilterMenu
CustomPopup						-> FileFilterPopup
FilterButtons					-> <not used>

--code:
(func)	on_custom_filter_menu_toggled	-> on_file_filter_menu_toggled
(func)	create_name_filters				-> create_file_filters
(var)	name_filters					-> file_filters
(var)	custom_popup					-> file_filter_popup
(var)	filter_menu_button				-> file_filter_menu_button
(var)	custom_merge_id					-> file_filter_merge_id
(var)	popup_deactivate_id				-> (common var) popup_deactivate_id
(var)	filter_ui						-> file_filter_ui
(var)	filter_actiongroup				-> file_filter_actiongroup
(func)	_cleanup_filter_menu_button		-> need extend for text-filters
(func)	_create_filter_menu_button		-> need extend for text-filters
(str)	DirdiffFilterActions			-> FileFilterActions
(ui)	Filters							-> File filters
(ui)	Set active filters				-> Set active file filters
(pot)	msgid "Filters"					-> msgid "File filters"
(pot)	msgid "Set active filters"		-> msgid "Set active file filters"

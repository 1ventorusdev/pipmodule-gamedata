========
gamedta
========
*creation of game, manage data of file.gdta*
the file.gdta are a dictionary of python saved into file

Install and import
------------------

- For install gamedta : pip install gamedta
- For import gamedta : from gamedta import 

Functions
---------

gamedta is a tool for simplify the game creation, it manage the data and have a many function for create game

gamedta using principal function :

- with Gopen(name of file in .gdta) as dta:
        - dta.open("r/m/c+/a")  # r for read data, m for modify data, c+ for create file, a for add data !it's obligatory for use other function!
        - dta["namedata"] = value # for save value with m, c+ or a
        - value = dta["namedata"] # for load value with r
        - dta.save() # for save data in  file
        - dta.create_dico(name_of_dico) # for create data since a dico
        - dta.delete(name_of_data) # for delete the data in file
        - dta.import_data(other_file, format_of_file) # for copy since other file.json or file.csv a data (experimental)
        - dta.export_data(other_file, format_of_file) # for copy into other file.json or file.csv a data (experimental)
        - dta.import_item(other_file, list_of_import_data) # for copy since other file.gdta a data (experimental)
        - dta.export_item(other_file, list_of_import_data) # for copy into other file.gdta a data (experimental)
        - dta.move_item(name_of_data, quantity, other_file.gdta) # for move data in other file.gdta (experimental)
        - dta.check_data_integrity() # for verify if data are good wrote (experimental)

- with Pnj(name_of_pnj) as pnj:
        - pnj.create_pnj(path_to_save, years_old, type(default=pnj), story_of_pnj(default=none)) # for create the pnj
        - pnj.modify_pnj(path_to_save, years_old, type(default=pnj), story_of_pnj(default=none)) # for modify information of the pnj

- with Player(name_of_player) as player:
        - player.create_player(path_to_save, type(mage, berzerker, etc), class(human, animal, elf, etc), hp, defense, damage(number of damage dealt to the enemy), inventory(default=yes), story(default=none))
        - player.modify_health/defense/dgt/breed/type(path_to_save, modified_value) # for modify data of Player
        - player.variable = use_health/defense/dgt/breed/type(path_to_save) # for stock data in variable for use this

- with Inventory(name_of_player) as item:
        - item.stock(path_to_save, name_of_dico) # for input data since a dictionary into the file of inventory
        - item.modify(path_to_save, name_of_data, new_value) # for change value of a data
        - random_item_name = item.use(path_to_save, name_of_data) # for use data with a variable
        - item.create_data_info(path_to_save, name_of_item, type_of_item(weapon, potion, etc), durability, dgt(default="none"), defense(default="none") # for create data of item
        - name_of_item's_info = item.use_info_item(path_to_save, type_of_item, name_of_item, info_to_import) # for save a info of item in variable
        - random_dico = item.use_full_info_item(path_to_save, type_of_item, name_of_item) # for save info of item in dico

- with Sound(music_path) as sound: # music_path is a path to access at file or directory of music
        - sound.play_music(loop(default=True)) # for launch music or sound and play in loop (experimental)
        - sound.gamedta.stop_music() # for stop actual music or sound (experimental)

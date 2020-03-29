# SJBot

This is an automated bot for StarJeweled (Bejeweled minigame in Starcraft) that can outperform the top players. Even the best human players can only achieve around 3000-3500 EPM, whereas this bot can consistently achieve 4500 EPM in an average game (as long as you don't lag too much and have decent framerate).

In order to build the project, you will need to `easy_install autopy3` and `pip install pyscreenshot` and 'pip install enum34' and 'pip install Pillow' as the program relies on these libraries. The bot works by periodically taking screenshots of the board and then using the average of the RGB values to accurately determine the color of each gem. It then looks for potential matches and calculates a score for each match based on the chain length, number of moves created, and several other metrics. It then determines the best subset of matches that do not conflict with each other and executes those.

If you want to use this and you are not already on 1080p or 1440p screen resolution (1920x1080 and 2560x1440 respectively), then you will need to modify `configuration.py` and adjust the values for the color calibration and screen positioning manually. If you look through the code in `main.py` you will see there are options to run the bot in calibration mode to get the average RGB values of all colors in a cell. You can use the printed results from calibration mode to find the default median RGB values to associate with every color.

**Uses Python 2.7

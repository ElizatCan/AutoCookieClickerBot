# AutoCookieClickerBot

This Python code uses the Selenium web automation library to control a Google Chrome browser and play a simple online game called "Cookie Clicker".

First, the necessary modules are imported, including Selenium's webdriver, Options, Service, and Keys, as well as Python's built-in time module.

The code then sets some options for the Chrome browser session, including adding the experimental option to detach the browser window from the script.

Next, the code starts a new Chrome browser session using the specified chrome_driver_path, which points to the location of the ChromeDriver executable file on the local system. The browser is directed to open the game page at http://orteil.dashnet.org/experiments/cookie/.

The script then finds the HTML element corresponding to the "cookie" object in the game, and gets the IDs for all of the upgrade items in the game store. These upgrade items are stored in a list called item_ids.

The main loop of the script then begins, which will repeatedly click the "cookie" object and buy the most expensive upgrade the player can afford. The loop runs until the game has been played for 5 minutes (as defined by the five_min variable).

On each iteration of the loop, the script clicks the "cookie" object and checks if 5 seconds have passed since the last upgrade purchase. If so, the script gets the prices of all the upgrades in the game store and creates a dictionary called cookie_upgrades with each upgrade's price as the key and its ID as the value.

The script then retrieves the player's current cookie count and creates a new dictionary called affordable_upgrades, which contains only the upgrades the player can afford. The most expensive upgrade the player can afford is identified by finding the maximum price in the affordable_upgrades dictionary.

The script then clicks the corresponding upgrade element and adds another 5 seconds until the next upgrade check. After 5 minutes have passed, the script prints the player's cookies per second rate and exits the loop.

Overall, this script demonstrates how Selenium can be used to automate web interactions, including playing simple online games like "Cookie Clicker".



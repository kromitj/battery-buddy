# battery-buddy

Battery management on both MacBooks and iPhones isn’t given; there isn’t any alert that tells you when you’ve been mis-treating the battery. My app will give dynamic, data-based, smart suggestions on whether you should be currently, charging( + ) or living-on-battery( - ).

	A macOs app, meant for MacBooks that records the battery 	data of the MacBook and records the ratio of the MacBook 		being juiced by battery and by wall.
	The main reason for the app is it will tell you when you are using your MacBook in a manner that will be detrimental to the battery. People will be reminded when they’ve been using wall power too long and also when they have’t discharged the battery recently(being plugged in to long).
 The Logic of the app will be coming up with schedules that set up the optimal discharge/charge cycle of the MacBook in the extended n amount of time. In other words, Based on the current battery data, and the amount of time your MacBook has been plugged in to the wall, and the average amount of time you spend on your MacBook per n time, I would suggest you keep your MacBook plugged in for 80% of your day, or 256 minutes. The program will then count each minute the macbook was plugged in the next day remind the user of their commitment and their progress. It’s kinda like a credit score on how you treat the battery. If you plug it in 99% of the time and never discharge the score will go down because there’s never any moment inside the battery so it starts to atrophy. It will also go down if it records you charging your MacBook at night then relying on the battery for 5 hours each day. This will negatively affect your credit score because the battery is being put under much stress and its capacity will fall off quickly if you do.

In A nut Shell.
	The app records how much you use your MacBook and how often you use your MacBook on battery charge. Based on these ratios it suggests future charging patterns that will result in the most optimum use of the battery.

Weighable attributes:

	time_charging_not_being_used(batt_percentage, cycles, capacity)
		
	time_chargin_being_used(batt_percentage, cycles, capacity)
		
	time_not_charging_being_used(batt_percentage, cycles, capacity)
		
	time_not_charging_not_being_used(batt_percentage, cycles, capacity)

Every minute BatteryBuddy records the following:
	recoredCurrentState(battery_data, past_battery_data)
		current_capacity = battery_data[:capacity]
		current_charge_perc = battery_data[:charge_perc]
		current_charge_mah = batter_data[:charge_mah]
		current_temp = battery_data[:temp]
		current_cycle_count = battery_data[:cycle_count]
		current_health = batter_data[:health]
		power_adapter_active = battery_data[:adapter]
		battery_useage = battery_data[:usage]
	end

First step is to get a program that takes and records battery data specific time intervals

At the begging of each day it gives an daily schelual of optimum charging

Machine Learning: The data from all users will be put into a centralized database and app will use the combined data to modify logic behind charging schedules. Example: based on a user that uses their MacBook unplugged this amount of time, similar users acheived best results from doing this…

The icon in the upper-right needs to be one-dimensional and super intuitive and easy. Example: dumb down actions to, charge or not-charge, the icon will eighter be: ( + ) or ( - ): where the app is advising you to ( + ) charge, or, run on battery ( - ). The end result should just be, User wondering if their treating the battery right, so they look at the icon of BattBuddy and see that it is a ( - ), they are currently charging their MacBook so they uplug it, because the app is saying that they run their MacBook on charge too much so they should let it discharge a bit. If the user is inclined to look into the issue deeper, they click on the icon and open the application, this gives in-depth data-visualation of how much they should charge or discharge the battery, and also all different aspects of charge states and others batt-data. This is where you can allow the user to dig deep into the data and see the patterns of their macbooks battery.
But in the end I want the icons to be the most common elements of engagement with my app. I want there to become a habitual action of looking at the battBuddy icon and modifying your charge. The change in icon should be flashy so you only notice it on feel the need to look at it when something changes, and the padding between the change of states should be high enough to debounce the rate at which somebody is told to change charge-state. What I mean is, Once somebody gets to a charging history that balances on charge or discharge, the program allows a positive charge state to built up before it suggests discharge. Basically its dealing with when your suggested to switch to an opposite state, once you switch, you will quickly encounter a switch to the previous state, which is annoying; charge, discharge, charge, discharge 

Design this with iOS and macOs in  mind. I mean, if you can make this work with iPhones, you would be taping in to a supply large market. BattBuddy scales, from the initial singular use with MacBooks, to the iphone. Both use lith-ion batts and with iPhones the home-screen icon could update to be either a + or -. 

This suggestion to charge/discharge should be weighable, meaning that is a User knows that the will be away from a wall connection for the majority of their MacBook use, they can modify the scale in a way that states that the optimum battery pattern is not possible. This is all about making the most of any situation, meaning, given these known un-optimum conditions what is the for the battery. For, even the person who spends 95% of their computer time unplugged, there is an optimum battery charge pattern. This could be hidden to the user by the app recording the ratio between charge_use and non_charge_use. 



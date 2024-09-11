# ChristmasCookieClickerGame

## Game Description

A Christmas-themed copy of Cookie Clicker.
The player clicks on a christmas cookie to generate christmas cookies, which can be used to upgrade the christmas cookie kitchen.

### Upgrade Types

1. **Click Power Upgrade** - Increases the number of christmas cookies generated per click by one.
2. **Auto-Clicker Unlock** - Unlocks the auto-clicker, which generates christmas cookies automatically. (One-time purchase)
3. **Auto-Clicker Speed Increase** - Increases the speed of the auto-clicker.
4. **Auto-Clicker Power Increase** - Increases the number of christmas cookies generated per auto-click.

### Events

1. **Burnt Christmas Cookies** - The player will lose a percentage of their cookies.
2. **Santa's Little Helper** - The player will gain a percentage of their cookies.
3. **Kitchen Robot Malfunction** - The auto-clicker will be disabled for a fixed period.
4. **Christmas Miracle** - The player will receive a temporary boost in cookies per click.

## Game Requirements

- All prices must be rounded to the nearest whole number.
- All upgrade prices must double after each purchase of the same type.
- Purchases cannot be made if the player does not have enough Christmas cookies.
- If an event results in a negative number of Christmas cookies, the player will have 0 cookies.
- Only one active event at a time (no event queue).
- The Christmas Miracle event only applies to manual cookie generation.

## Tool Requirements

- Visual Studio 2022 Community Edition
  - Workload: .NET Desktop Development
- GitHub and GitHub Desktop for version control

## Tech Stack Requirements

- WPF as the project type
- C# as the programming language

## Project file/folder structure

- **Folders**
	- `Assets` - Contains images, sounds , and other assets.
	- `Documentation` - Contains all notes, ideas, descriptions and other documentation.

- **Files**
	`MainWindow.xaml` - Contains the main game UI.	
	`MainWindow.xaml.cs` - Contains the main game logic.

## Functionality

- **Generate Cookies**: The player receives cookies equal to their current click power.
- **Purchase Click Power Upgrade**: Spend a fixed number of cookies to increase click power.
- **Purchase Auto-Clicker Unlock**: Spend a fixed number of cookies to unlock the auto-clicker (one-time purchase).
- **Purchase Auto-Clicker Speed Increase**: Spend a fixed number of cookies to increase the auto-clicker’s speed.
- **Purchase Auto-Clicker Power Increase**: Spend a fixed number of cookies to increase the auto-clicker’s power.
- **Handle Burnt Christmas Cookies**: The player loses a percentage of their cookies.
- **Handle Santa's Little Helper**: The player gains a percentage of their cookies.
- **Handle Kitchen Robot Malfunction**: The auto-clicker is disabled for a fixed period.
- **Handle Christmas Miracle**: The player receives a boost in cookies per click for a fixed period.
- **Randomly Select Event**: The game randomly selects an event to trigger.
- **Double Upgrade Price**: The price of the next upgrade of the same type is doubled.

## Guides

### UI - Christmas Cookie Clicker Game UI Setup Guide

This guide will walk you through setting up the new **Christmas Cookie Clicker** game user interface. Follow each step to recreate the UI using **XAML** elements.

## 1. Setting Up the Grid Layout

1. Begin by defining the structure of the UI using a **Grid** layout.
2. Create **5 columns**: two narrow margin columns on the sides and three wider columns in the center for the main content.
3. Define **7 rows**: one for margins at the top, one for the game title, five rows for the game content, and one for margins at the bottom.

## 2. Adding the Game Title

1. Place a **Label** in the second row, spanning across the central three columns, to display the game title, "Christmas Cookie Clicker".
2. Set the font size to **50** and make it bold to ensure the title is prominently displayed.
3. Center the title both horizontally and vertically.

## 3. Event Log Section

1. On the left side of the grid (columns 1, rows 2 to 3), create a **Border** to contain the event log section with a **Silver** border.
2. Inside the border, use a **StackPanel** to organize the content vertically.
3. At the top of the **StackPanel**, insert a **Label** with the text "Christmas events", using a bold and centered font.
4. Below the label, add a **ScrollViewer** for vertical scrolling. Inside it, place another **StackPanel** to dynamically list event log items.

## 4. Upgrade Log Section

1. Below the event log, create another **Border** in the left side of the grid (columns 1, rows 4 to 5) with a **Silver** border for the upgrade history.
2. Inside the **Border**, use a **StackPanel** to organize content vertically.
3. Add a **Label** titled "Upgrade history" at the top of the stack panel.
4. Below the label, add a **ScrollViewer** with a **StackPanel** inside to display purchased upgrades. Ensure vertical scrolling is enabled.

## 5. Main Game Area - Cookie Button and Info

1. In the central grid area (columns 2, rows 2 to 5), create the main game interaction area.
   
   - **Step 1:** Add a **StackPanel** with vertical orientation in row 2 to display information.
     - Add a **Label** to display the number of cookies (e.g., "0 CC"). Use the **RegularLabelStyle**.
     - Below that, add two **Labels** for the event title and timer (e.g., "No event" and "00:00:00"). Initially disabled.
   
   - **Step 2:** In row 3, add a **Button** with an image of a gingerbread man to represent the clickable cookie. 
     - Use the custom style **ChristmasCookieButtonStyle**.
     - Ensure the button fills rows 3 to 5, spanning vertically.

## 6. Stats Display Section

1. On the right side of the grid (columns 3, rows 2 to 3), create a **Border** with a **Silver** border to display player stats.
2. Inside the border, use a **Grid** with multiple rows (for different stats) and two columns (stat name and value).
3. Add a **Label** at the top titled "Christmas stats".
4. Below this, display various stats such as:
   - **Click power level**: Create two labels to show "Click power level" and its value (starting at 1).
   - **Auto click status**: Initially, this will display "Locked" and be disabled. Include an **AutoClickUnlockButton** for unlocking this feature.
   - **Auto click power level**: Initially set to 1 and disabled.
   - **Auto click speed level**: Initially set to 1 and disabled.

## 7. Purchaseable Upgrades Section

1. Directly below the stats display, in rows 4 and 5, create another **Border** for the upgrade options, with a **Silver** border.
2. Inside the border, use a **Grid** with two columns (upgrade name and price) and five rows (one per upgrade option).
3. Add a **Label** at the top titled "Christmas upgrades".
4. Below the title, list the following upgrades, each paired with a **Button** displaying the cost:
   - **Click power level 2**: A button to purchase this upgrade, initially costing "10 CC".
   - **Auto click unlock**: A button to unlock auto-click functionality, initially costing "1000 CC".
   - **Auto click power level 2**: A button for upgrading auto-click power, initially costing "250 CC", but disabled until the auto-click feature is unlocked.
   - **Auto click speed level 2**: A button for upgrading auto-click speed, initially costing "250 CC", but disabled until the auto-click feature is unlocked.

## 8. Style Customizations

1. Use centralized styles for **Labels** and **Buttons** to ensure consistent visual presentation.
   
   - For **Labels**, the styles include bold fonts, center alignment, and a consistent font size across the UI.
   - For the **Christmas Cookie Button**, the style removes borders and background, but adds hover effects like changing the background to white and switching the cursor to a hand when hovered.

## 9. Scrollable Sections

1. Ensure both the **Event Log** and **Upgrade Log** are wrapped in a **ScrollViewer** with vertical scrolling enabled, to allow users to view more events and upgrades as the game progresses.

By following these steps, you will recreate the new **Christmas Cookie Clicker** UI. Each section is properly aligned, and the style customizations ensure a polished and cohesive appearance. Every element is logically grouped for a smooth user experience.

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

## Tool Requirements

- Visual Studio 2022 Community Edition
  - Workload: .NET Desktop Development
- GitHub and GitHub Desktop for version control

## Tech Stack Requirements

- WPF as the project type
- C# as the programming language

## Game Requirements

- All prices must be rounded to the nearest whole number.
- All upgrade prices must double after each purchase of the same type.
- Purchases cannot be made if the player does not have enough Christmas cookies.
- If an event results in a negative number of Christmas cookies, the player will have 0 cookies.
- Only one active event at a time (no event queue).
- The Christmas Miracle event only applies to manual cookie generation.

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

## UI

- **Setup of the game’s grid layout**
  - `ColumnDefinitions`
  - `RowDefinitions`

- **Main Game Area**
  - `Button` to generate cookies
  - `Label` to display the number of cookies
  - `Label` to show the current event and possibly an event timer
  - Horizontal `Stackpanel` with buttons and price labels for upgrade purchases
  - Vertical `Stackpanel` inside a `ScrollView` to list purchased upgrades
  - Vertical `Stackpanel` inside a `ScrollView` to list combined upgrade effects
  - Vertical `Stackpanel` inside a `ScrollView` to list events

## Project file/folder structure

- **Folders**
	- `Assets` - Contains images, sounds , and other assets.
	- `Documentation` - Contains all notes, ideas, descriptions and other documentation.

- **Files**
	`MainWindow.xaml` - Contains the main game UI.	
	`MainWindow.xaml.cs` - Contains the main game logic.
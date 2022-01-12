# mycampus-calendar-rs

This is a small program to parse student schedules from MyCampus into `.ics` files, which can be imported into any calendar app (eg. Google Calendar, Outlook, Apple Calendar). This is working as of Winter 2022.

## Installation


[Install Rust](https://www.rust-lang.org/learn/get-started), then clone this repo.

## Usage

1. Log in to MyCampus and navigate to the Student Schedule page. Select the current term in the dropdown, then go to the Schedule Details tab. Click all of the arrows beside the course names so they're pointing **down** and the gray boxes are showing.
2. Press `ctrl + a` then `ctrl + c` to select and copy everything on the page. Don't select it manually or the parsing might not work properly.
3. Create a file called `data.txt` in this folder. Paste what you copied from MyCampus in this file, then save it.
4. Create a file called `exdate.txt` in this folder. Add any date ranges you want to exclude from the generated events here, in the format `yyyy-mm-dd - yyyy-mm-dd` (example: `2022-02-21 - 2022-02-27`). Put each range on its own line. If you only want to exclude one day, put it as both the first and second date (example: `2022-02-21 - 2022-02-21`).
5. Run the program using `cargo run`.
6. Import the generated `.ics` file(s) into a calendar program of your choice.
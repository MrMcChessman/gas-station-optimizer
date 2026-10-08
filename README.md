# gas-station-optimizer
Gathers daily-updating gas station pricing info around a specified address, and processes data into an easily viewable format for users to make an informed gas purchasing decision.

[Open a copy on Google Sheets](https://docs.google.com/spreadsheets/d/1QfGbEa5is4c-rPP0q9vdIrZ4piXZ24dqMHKO9edFhso/copy)

![Screenshot of Tool Output](assets/gas-station-optimizer_Colored_values.png)

**How it works:**
---
_outside sources_
- Station data sourced from [sitelocator.wexonline.com](sitelocator.wexonline.com)
- Apps Script Google Maps functions courtesy of [Amit Agarwal](https://www.labnol.org/about) and his personal work on [Labnol.org](https://www.labnol.org/google-maps-sheets-200817)

_data pipeline, ranking logic, comparison display, base-station checkboxes_
- Top station selected based on proximity to user, remainder of stations ordered based on gas price
- Cost savings/losses and time gained/lost vs top station displayed to user, allowing for an informed decision
- Hyperlink provided for instant Google Maps directions from current location to selected station

**How to use:**
1. Create a copy of the most recent version using the link above, or [here](https://docs.google.com/spreadsheets/d/1QfGbEa5is4c-rPP0q9vdIrZ4piXZ24dqMHKO9edFhso/copy).
2. Input current address into _D4_
3. Wait up to 15 seconds for data to fully load and process
4. View results in range H3:K16; compare savings, time, and other present information with a base result to select a station
5. Use the provided hyperlink for immediate Google Maps directions to chosen station from input address

_For greater precision:_
  - In D6, specify a town to only receive stations from that specific town
  - In B11:F13, use checkboxes to alter the base station if another option is preferred

Courtesy of [Amit Agarwal](https://www.labnol.org/about), Google Maps API access is available for a limited number of requests per Google account per day.  This tool can support ~5-10 calls per day at current efficiency.

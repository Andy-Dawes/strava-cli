# Strava command-line interface

Uses [Strava API](https://developers.strava.com/docs/reference/) to access Strava dataset.

## Usage

```bash
$ strava [OPTIONS] COMMAND [ARGS]
```

### Get Started

[Create application](https://www.strava.com/settings/api) and set the following environment variables before running `strava`:

```bash
export STRAVA_CLIENT_ID={YOUR_CLIENT_ID}
export STRAVA_CLIENT_SECRET={YOUR_CLIENT_SECRET}
```

Login to your Strava service (opens a web browser sending user to Strava login service):

```bash
$ strava login
```

For usage and help content, pass in the `--help` parameter, for example:

```bash
$ strava --help
```

### Available commands

Get recent, yearly, total stats:

```bash
➜ strava stats  

Type        Count  Distance    Moving time    Elevation gain
--------  -------  ----------  -------------  ----------------
🏃 recent        7  53.33 km    5h 6m          166 m
🏃 ytd         121  1048.15 km  95h 43m        4526 m
🏃 all         241  1761.13 km  164h 35m       7258 m

```

Get last 5 activities:

```bash
➜ strava activities -PP 5  
  Index  Start date                 Name             Elapsed time    Distance    Average speed
-------  -------------------------  ---------------  --------------  ----------  ---------------
      1  2018-12-27 17:58:49+01:00  🏃 Afternoon Run  45:19           8.02 km     05:15 /km
      2  2018-12-25 15:38:55+01:00  🏃 Bday Run       44:56           7.32 km     05:41 /km
      3  2018-12-23 14:29:50+01:00  🏃 Afternoon Run  48:14           6.55 km     06:17 /km
      4  2018-12-22 20:13:31+01:00  🏃 Evening Run    37:34           7.10 km     05:16 /km
      5  2018-12-16 16:39:56+01:00  🏃 Afternoon Run  41:54           6.31 km     05:43 /km
```

Get detailed activity information:

```bash
➜ strava activity -I 14
Name:                  🏃 30. Bieg Niepodległości
Description:           Oficjalny czas: 46:55
Start date:            2018-11-11 11:24:28+01:00
Elapsed time:          46:58
Distance:              10.02 km
Average speed:         04:41 /km
Total elevation gain:  52 m
Calories:              639.0
Device name:           Garmin Forerunner 645 Music
Gear:                  New Balance Zante v4 (443.65 km)
Split 1:               👟 04:44 /km ❤ 164 bpm ⬆ 7 m
Split 2:               👟 04:38 /km ❤ 168 bpm ➡ 0 m
Split 3:               👟 04:48 /km ❤ 164 bpm ⬆ 1 m
Split 4:               👟 04:49 /km ❤ 160 bpm ⬇ -3 m
Split 5:               👟 04:41 /km ❤ 161 bpm ⬇ -2 m
Split 6:               👟 04:37 /km ❤ 164 bpm ⬆ 2 m
Split 7:               👟 04:50 /km ❤ 165 bpm ⬆ 3 m
Split 8:               👟 04:39 /km ❤ 163 bpm ⬇ -1 m
Split 9:               👟 04:42 /km ❤ 165 bpm ➡ 0 m
Split 10:              👟 04:24 /km ❤ 171 bpm ⬇ -9 m
Split 11:              👟 04:44 /km ❤ 173 bpm ⬇ -1 m

```

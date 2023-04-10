# ProgressBarTimeLeft
This is a fork of a [Progress Bar add-on](https://github.com/carlos1172/ProgressBarTimeLeft) for [Anki](https://apps.ankiweb.net/).
This version keeps functionality the same but introduces the following quality of life improvements:
* The part that adds tracked values to the progress bar now takes about 50 lines of code (vs 400 in the original repo), while keeping all the functionality and adding a bit of customizability in terms of user settings. It also allows for easy reordering of the values in the progress bar.
* The timezone setting `tz` now can be set to `null` (new default value) to use the timezone of the machine on which Anki is run. This eliminates the need to establish your timezone in GMT. However, this option is still available if the user prefers to manually set the timezone.
* The default parameter values are changed to keep the progress bar neat and not overwhelm the user with stats. Should the user choose to have all stats visible, they can be enabled in `./config.json` as usual.
* Minor design adjustments to the progress bar to make it look a bit more modern.

## Configuration
Parameter values are set in `./config.json` and contain the following:
* `show_values`: Show stats in the progress bar. If `0`, only the progress percentage is shown. (default is `1`)
* `show_cards_done`: Show the number of completed cards in the current deck. (default is `1`)
* `show_cards_left`: Show the number of cards left in the current deck. (default is `1`)
* `show_cards_percent`: Show the percentages of completed/remaining cards in the current deck. (default is `1`)
* `show_time_per_card`: Show the average number of seconds per card in the current deck. (default is `0`)
* `show_time_spent`: Show the time spent in the current deck. (default is `1`)
* `show_time_remaining`: Show the time estimated to finish the current deck. (default is `1`)
* `show_time_finish`: Show the estimated time when the current deck will be finished. (default is `1`)
* `show_again_rate`: Show the percentage of repeated cards in the current deck. (default is `0`)
* `show_retention`: Show the retention rate in the current deck. (default is `0`)
* `show_super_mature_retention`: Show Super Mature Retention in the current deck. (default is `0`)
* `show_past_values`: Show average past values in parentheses. (default is `0`)
* `no_days`: Number of days to compute average past values and retention. (default is `7`)
* `lrn_steps`: Number of steps used in New/Lrn/Rev Weights calculations. (default is `2`)
* `show_debug`: Show New/Lrn/Rev Weights used for computations. (default is `0`)
* `tz`: Specify timezone in GMT for the ETA estimate. Set to `null` to use the device timezone. (default is `null`)

---
## Original Description
Hello, this is my first "add-on" (which isn't really by me since I just tweaked/merged Glutanimate's Progress Bar add-on with Carlos Duarte's More Decks Stats and Time Left add-on.). I basically got the progress bar to work on 2.1.49, as well as added statistics for cards left, percentage left, time (s) spent per card based on today's reviews, and time left based on how fast you've done today's reviews.   

I have not tested this on any other version besides 2.1.49-2.1.54, but I just wanted to share it since it took me a while to get this working and I'm very proud of it (and am hugely thankful to Glutanimate and Mr. Duarte).  

Installation: Double click the anki-addon file or install the add-on from https://ankiweb.net/shared/info/1097423555

P.S. This is my first time using GitHub and Anki-Web, so please be kind :(

Update see ankiwebs link for changelog

## Configuration
CHANGE ALL VALUES IN reviewer_progress_bar.py <br>
<br>
If True, write "True", otherwise leave it empty (e.g. "")<br>
<br>
Change the following in reviewer_progress_bar.py<br>
"includeNew": "True",<br>
"includeRev": "True",<br>
"includeLrn": "True",<br>
"includeNewAfterRevs": "True",<br>
"scrollingBarWhenEditing": "True",<br>
"invertTF": "",<br>
"forceForward": "",<br>
"dockArea": "Qt.TopDockWidgetArea"<br>
"orientationHV": "Qt.Horizontal"
"qtxt": "aliceblue",<br>
"qbg": "rgba(0, 0, 0, 0)",<br>
"qfg": "#3399cc",<br>
"qbr": "5",<br>
"maxWidth": "20",<br>
"orientationHV": "Qt.Horizontal",<br>
"tz": 8 #GMT+ CHANGE THIS TO YOUR GMT+_ (negative number if you're GMT-)<br>

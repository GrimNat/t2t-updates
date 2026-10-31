# What's new

## v3.4.1 (2026-10-31)
- Fixed the freezes: the painted map pictures were saved inside the map file (70 MB with the overworld's), and Mudlet rewrote that file every few minutes. They're laid as temporary pictures now, never saved, so the map file stays small (about 9 MB).
- On the overworld only the pictures around you are laid (3 or 4 instead of all 31), and a few are swapped in as you travel: far less memory, and the map redraws faster.
- Following long stretches of look-alike rooms (travelto across the Rohan Plains) takes less work: each room is checked once per step.

## v3.4.0 (2026-10-31)
- Rivers go on the map as you swim or row: each water room you reach that the map doesn't have yet is added one step from where you were, named by its title, colored blue and linked to its banks. 'mapwater' shows how many there are, 'mapwater off' stops it, 'mapwater undo' removes the last one made.
- Water rooms are locked: sp, goto and clicking the map still never take you through water (no drowning in a fight or with a heavy pack). Swimming and boating paths on request come later.
- Moves on the water are followed: 'swim <dir>', 'launch <dir>', plain directions in a boat, 'land <dir>' back ashore. If the map wasn't sure which bank you set out from, it says so instead of guessing (then 'here <roomID>' on the bank).
- No need for 'start mapping' on the water: if it's on when you swim or launch, it pauses (the stock mapper made one-way exits and copies of rooms there) and comes back on when you're on foot again.

## v3.3.0 (2026-10-31)
- A new way of following you on the map, made for The Two Towers. It counts every command and every step of a 'do' by the game's prompts, and finds each room by its name and its exits, so long runs of look-alike rooms (Rohan Plains, the Lebennin Road) no longer lose it.
- The map follows moves the game makes for you: travelto, following a leader, game aliases. Among look-alike rooms it keeps every possibility and shows its best guess; where nothing tells them apart (open plains) it waits at the last room it was sure of.
- Lothlorien: the game swaps a square's name between 'Lothlorien' and 'Near a guard flet', which threw mappers off. Both now count as the same room (on your Cerin Amroth walks the map was on the right square 497 times out of 504).
- The spiral staircase in the Barad-dur tower: 'A dimly lit stairway', 'An ominous stairway' and 'A dark stairway' swap too and now count as the same room.
- The drunk mug follows the game: every stage in 'score' (a bit tipsy, somewhat drunk, rather drunk, completely smashed, totally wasted, too drunk to remember your name), every step of sobering up, the headache, and sober again.
- Disguises show on your portrait: after 'disguise race ...' or 'disguise profession ...' it shows the disguise with a mask badge, and 'score' no longer mistakes the disguise for your real race.
- Room title colors are a hint only: another character with other colors still works, and you're reminded once to type 'mapsetup'.
- A command that moved you where the map has no exit (search brush, press indentations) offers [remember it] to add that exit.
- Swimming and boating are noticed: the map waits at the last land room and finds you again when you land (water rooms aren't on the map yet). Water titles without ( ), like the Ringlo rapids, are read now.
- 'spmode safe' walks one step at a time with our own walker; 'spstop' stops it.

## v3.2.0 (2026-10-31)
- Fast speedwalks, the T2T way: sp, goto and clicking the map send the whole path as one 'do' line, and the map keeps up room by room (special exits like 'enter' included: no more map stuck at the guildhall door). 'spmode safe' walks one step per room instead.
- The map keeps up with your own 'do a,b,c' lines and with game aliases too: when it didn't follow a move, it finds you among the nearby rooms by name and exits.
- Fixed: when the map lost track of you, the room it thought you were in could get the wrong color (the color of the room you were really in), and that was saved in the map. Now a room is only colored when the map agrees with the game.
- Changed: 'deletearea' needs an area number (on its own it used to delete area 1).
- New: 'mapsetup'. Room title colors are a game setting, so the mapper reads yours from the game's 'color' menu (it opens the menu, reads it and closes it for you). 'mapsetup show' shows them.
- Fast walks: when a step fails, the rest of the 'do' still runs in the game; the map now follows it from where you really are.
- Removed: the slow pulse of the HP/EP bars ('uitheme glow'). It restyled the bars about 13 times a second and could make Mudlet stutter; the bars now only change when your HP/EP color does.
- New: 'debug on' shows a grey line after every room: the room the game shows next to the room the map thinks you're in (ID, exits), and says when they disagree. It also says when the mapper won't count a command as a move (like 'enter' in a room the map has no 'enter' exit for). 'debug quiet' writes it only into the rec log, 'debug off' stops.

## v3.1.0 (2026-10-31)
- Updates from inside Mudlet: new versions and maps are offered in a pop-up when you log in ('omiupdate' checks now). This is the last time you install the packages by hand.
- Version number at the right end of the menu bar: click it for what's new and to check for updates.
- Smart exits learn where they lead: 'sx n enter', then just go n. The map follows you and links the room you land in; 'sx s out' on the other side links the way back. No more 'spev'.
- Session recorder (rec): every game line in colour, your commands and the rooms you pass go to omi_logs in your profile. Your login is never written. 'rec off' stops it until the next start.

## v3.0.0 (2026-10-30)
- Everything in one package, OmiT2T, plus OmiT2TPersonal (replaces the 7 old T2T packages).
- Menu bar at the top left with a Help pad: every game help file, read offline after one 'helpcrawl'.
- Touch friendly: 'uitouch on' makes the bar, buttons and text bigger.
- Fewer freezes: the painted map lays only the current area's pictures.

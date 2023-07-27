Method Raid Tools:
https://www.curseforge.com/wow/addons/method-raid-tools
/mrt

MRT Note Importer:
https://www.curseforge.com/wow/addons/mrtnoteimporter
/mrtni

Kaze ERT Timers:
https://wago.io/NL8PU79CK
/wa

Kaze ERT Bars:
https://wago.io/CiT6RbPDe
/wa

ERT/MRT Timers Icons
Showing icons depending on ERT/MRT notes
Inspired by buds ERT Timers
Mostly for usage with Viserio's Healing Cooldown Spreadsheet but has other advanced usages


Custom Options

Option
Settings
Description
Show Text	true
false	If you want to show the text next to the icon.
Show Spellname	true
false	If you want to show the spell name of the icon.
Warn Duration	Numeric	How many seconds before the trigger time you want it to appear.
Delay to hide	Numeric	How many seconds after you want the icon to remain on screen
Disable Icons When	Hidden or Disabled
Disabled
Never	Will show icons depending on your ERT/MRT note status.
Additional Matching Keywords	Text (comma seperated)	 This will show icons that matches the keywords even if you have selected "Only show icons with own name".
Ignore Keywords	Text (comma seperated)	This will ignore icons that contains the text.
Disable Shared Note	true
false	Does not read text from ERT/MRT shared note
Disable Personal Note
true
false	Does not read text from ERT/MRT personal note
Only show icons with own name	true
false	This will only show icons which text contains your name or matches the additional keywords



Guide (Beginner)
Format for timers
Timer
Description
{time:75}	 Timer with 75 seconds
{time:1:10}	 Timer with 1 minute and 10 seconds
{time:01:15}	 Timer with 1 minute and 15 seconds
{time:02:30,p2}	 Start on phase 2, works only with bigwigs or DBM
{time:00:30,SCC:347704:2}	 Start on 2nd cast of "Veil of Darkness" (347704). Format "event:spellID:counter".  
Events: SCC (SPELL_CAST_SUCCESS), SCS (SPELL_CAST_START), SAA (SPELL_AURA_APPLIED), SAR (SPELL_AURA_REMOVED)


Display
Seperate multiple "inputs" with double space
ERT/MRT
Description
{time:20}Kazeshinu	 Displays the text "Kazeshinu"
{time:20}Kazeshinu {spell:77761}	 Displays icon for  (77761) with text "Kazeshinu"
{time:20}Kazeshinu {spell:33891}  Kazeshinu {spell:740}	 (Double space) Displays 2 icons one with  and one with ﻿ both with the text Kazeshinu
{time:20}Kazeshinu {spell:33891} Kazeshinu {spell:740}	 (Single space) Displays 1 icon  with the text "Kazeshinu  Kazeshinu"
{time:20}|cfffe7b09Kazeshinu|r {spell:77761}	 Displays icon for ﻿ (77761)﻿ with text "Kazeshinu"
{time:20}Use roar - |cfffe7b09Kazeshinu|r {spell:77761}	 Displays icon for ﻿ (77761)﻿ with text "Kazeshinu"  
The text "Use roar" is ignored as texts can not include hyphens ( - )
{time:20}Use roar  - |cfffe7b09Kazeshinu|r {spell:77761}	 Displays text "Use roar" and Displays icon for ﻿ (77761)﻿ with text "Kazeshinu"  
"Use roar" ends with double space so its a seperate "input" from the hyphen ( - )



Examples
ERT/MRT
Description
{spell:358760} {time:00:16}|cD9CF002F7Dragging Chains|r - |cfffe7b09Kazeshinu|r {spell:77764}  	 Displays icon for  with text "Kazeshinu" with the timing 16 seconds from pull the text Dragging Chains and the first icon is ignored as it contains a hyphen ( - ) before a double space
{spell:351413} {time:00:29,SAR:348805:1}|cF40060D8Annihilating Glare 3|r - |cfffe7b09Kazeshinu|r {spell:77764}  	 Displays icon for  with text "Kazeshinu" with the timing 29 seconds after first time aura 348805 ("Stygian Darkshield" Eye of the Jailor immunity) gets removed
{spell:358760} {time:00:22,p3}|cF3FF7000Dragging Chains|r - |cfffe7b09Kazeshinu|r {spell:77764}  |cfffe7b09Other Druid|r {spell:77764}  	 Displays 2  icons after 22 seconds entering phase 3 (Requires DBM or bigwigs)


Guide (Advanced)

Trigger
ERT/MRT
Description
{time:ss}	 Just seconds
{time:mm:ss}	 Minutes and seconds
{time:mm.ss}	 Minutes and seconds seperated by dot
{time:mm:ss,condition}	 Conditions see next table



Conditions
Condition
Description
event:spellid:counter	 event = SCC | SCS | SAA | SAR  
spellid = ###  -- numeric id of spell  
counter = ### -- at what occurance 0 for every
p#	 p2 -- Triggers at start of p2 (Requires DBM or bigwigs)


Events
Event
WOW Event type
SCC	SPELL_CAST_SUCCESS
SCS	SPELL_CAST_START
SAA	SPELL_AURA_APPLIED
SAR	SPELL_AURA_REMOVED


Each line contains a trigger that starts a timer.  
Each line can contain multiple inputs they are seperated by double space.
Inputs with hyphens ( - ) is ignored
Each input can have one icon that is taken from the last occurance of {spell:###} other icons will appear in the text










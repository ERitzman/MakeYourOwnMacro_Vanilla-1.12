***MAKE YOUR OWN MACROS***
__**QUICK RUN DOWN OF HOW MACROS WORK:**__** 
( *this does not include SuperWoWMacros; which will be discussed at a later time* )

** # ** – anything following a *Hashtag* is a __MetaCommand__. These dictate how it will appear on your bar. (Examples: `#Show` and `#Showtooltip`)

** / ** – Anything following a *forward slash* is a __command__. The words used will dictate the type of action that will be carried out (Examples: `/say`, `/cast`, `/target`)

**[]** – Anything between these *brackets* are the __criteria__  that has to be met to dictate which action will be used. This is generally (but not always) in two parts, separated by a *Colon* (**:**). The part __before the Colon__  is an indicator of the type of criteria that must be met (Examples: `[Worn:]` `[Stance:]`
The part __after the Colon__ is the specific part of the criteria (Examples: `[Worn:Bow]` will check that the item equipped is a bow, where as `[Worn:Gun]` will work if the item equipped is a Gun or `[Stance:1]` and `[Stance:2]` for warrior stances *(more on that below)*.
There are a few Criteria that are not split into two parts (examples: `[harm]` which will work if you are able to harm the target or `[mounted]` will work if you are mounted)
Most Criteria can be __inversed__ by adding “*__no__*” in front of them (example: `[noharm]` will work on targets you cannot harm)
After the command (or Criteria if you are using them) you then put the action (example: Frost Nova can be either: `/cast Frost Nova` or `/cast [harm] Frost Nova`)

__STANCE/FORM CRITERIA: WHAT THE NUMBERS MEAN!__
`[Stance:0]` = No Stance
`[Stance:1]` = Battle Stance (warrior), Bear/Dire Bear Form (druid), Stealth (Rogue), Shadowform/Spirit of Redemption (Priest) or Ghost Wolf (Shaman)
`[Stance:2]` = Vanish (Rogue), Defensive Stance (warrior) or Aquatic Form (Druid)
`[Stance:3]` = Berserker Stance (Warrior), Cat Form (Druid)
`[Stance:4]` = Travel Form (druid)
`[Stance:5]` = Moonkin Form (druid)

( *__NOTE__: The words __`Stance`__ and __`Form`__ are interchangeable* )

__SOME EXAMPLE HANDY MACRO’S AND HOW THEY WORK__
Some of these may be class specific, but hopefully should show how they are written and thus easily modifiable to suit your own needs/class!

This one removes the need to change abilities for each type of ranged weapon, plus the skill icon changes to match the icon for the type of weapon you are using! Great for Warriors, Rogues and Hunters!
>``#showtooltip
> /cast [worn:Bows] Shoot Bow; [worn:Crossbows] Shoot Crossbow; [worn:Guns] Shoot Gun; [worn:Thrown] Throw`` 

“`#showtooltip`” Makes the icon show what will be cast/used when clicked (including cooldowns)
“`/cast`” This tells the game that it will need to use a skill based on the following criteria/indicators
“`[worn:-Weapon Type-]`” Will do the following action based on what type of item is equipped/worn
“`Shoot -Weapon Type-`” This is the action indicator that tells the game what ability to use

Here are a couple written for a Warrior:
This first one is very simple and great for Prot Warriors. IF you are in Defensive Stance, pressing it switches to Battle Stance, and if you are in Battle Stance it will switch you to Defensive Stance!
>``#showtooltip 
>/cast [stance:1] Defensive Stance; [stance:2] Battle Stance``

“`#showtooltip`” Makes the icon show what will be cast/used when clicked (including cooldowns)
“`/cast`” This tells the game that it will need to use a skill based on the following criteria/indicators
“`[stance:1/2]`” Will do the following action based on the stance you are in – 1 = Battle Stance, 2 = Defensive Stance and 3 = Berserker Stance
“`Battle/Defensive Stance`” This is the action indicator that tells the game what ability to use

This fits perfectly in with the second one, which does three different spells:
If you are out of combat, it will use Charge (which can ONLY be used in Battle Stance), and when you are in combat, it will use Execute while in Battle Stance or Taunt while in Defensive Stance! These two Macro’s together allow you to easily use certain Stance Specific skills without too much messing around.
> `` #showtooltip 
>/cast [nocombat] Charge 
>/cast [stance:1]Execute; [stance:2] Taunt``

“`#showtooltip`” Makes the icon show what will be cast/used when clicked (including cooldowns)
“`/cast`” This tells the game that it will need to use a skill based on the following criteria/indicators
“`[nocombat]`” Will do the following action only if you are not in combat (and if you are in combat, it will skip to the following line)
“`[stance:1/2]`” Will do the following action based on the stance you are in – 1 = Battle Stance, 2 = Defensive Stance and 3 = Berserker Stance
“`Charge/Execute/Taunt`” This is the action indicator that tells the game what ability to use based on which criteria has been met

Now here is one for druids - this one will take you out of any existing form and place you into Dire Bear Form (*remove the word Dire if not specced for Dire Bear to use normal Bear Form*) while simultaneously equipping your tank rings
> `#showtooltip Dire Bear Form /cancelform [stance:2][stance:3][stance:4] /cast Dire Bear Form /equipslot 11 Ring of Protection /equipslot 12 Naglering`
“`#showtooltip Dire Bear Form`” Makes the icon show Dire Bear Form, overriding all other tooltips used in the macro
“`/cancelform [stance:2][stance:3][stance:4]`” Cancels Any other form currently active
“`/cast Dire Bear Form`” Puts your Druid into Dire Bear Form
“`/equipslot 11/12 (ring names)`” these two lines will put rings into the two different ring slots (*not specifying the two slots will cause both rings to try go into the same slot) - the ring name should be changed to your own rings you use for tanking*

**__Summary__**

Hopefully this guide helps - it isn't intended to be a list of macros to copy and paste (although feel free to use any of the examples) but instead showing how they are written and how they work so you can make your own if you wish and nearly all the examples can easily be modified to suit multiple classes by simply changing ability and item names

In the end, Macros are all about trial and error and hopefully you will now have enough knowledge to not feel completely lost when you decide to try start writing your first macros 

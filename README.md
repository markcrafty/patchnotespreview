Beta Release 0.2.5: Step It Back Patch Notes

## DEV NOTE

Contact me on Twitter (@MarkCrafty) if something seems amiss.

## TL;DR FEATURES

Reverted battle UI overhaul.

1 new character:
Kowalczyk, the Alchemical Engineer.
„Ko-wall-check. Kowalczyk! You'll get it eventually.”
(Late submission to the old character creation contest by Diggy)

Cyrin redesign.

Vyn boss fight redesign.

Lots and lots of bug fixes.

## CORE ENGINE

Updated the credits.

Mostly reverted the previous battle UI overhaul. It was causing more problems than it fixed.

## GAMEPLAY

Speed has been reduced for all characters.
Not really a balance change, but more of a change to make speed more managable.
Inspired by Chrono Trigger, the base max is now 16 (Unless your name is Sel).

The turn order now moves out of the way when an information box opens.
Rather than saying "CURRENT" and "NEXT", the turn order now says "Current Turn" and "Next Turn".

Moved the party back now that they have space again.

I remembered why I originally removed enemy levels and have removed them again.

Increased the chance of escaping from battle from a base 5% to a base 25%.

## CHARACTERS

### Universal:

Casters have been renamed to Mages.
I honestly thought I already did this, since I've been calling them mages since I got back to development.

Added some short quotes that should pop up when checking a character's status outside of battle.

Undid the gauge related changes from last patch, since they were caused by the battle UI overhaul.

### New "Mage", Kowalczyk, the Alchemical Engineer:

Manafold (Passive):
A fun little invention, the Manafold extracts the residual mana from anything passed through it. For example, mosquito elementals.
Each turn, Kowalczyk regenerates 2% of his mana. Whenever an enemy dies, he instantly regenerates 14% of his mana.

Capacitance:
Discharges energy by jamming a mana crystal into an enemy, dealing 
(1x Strength + 1x Intellect) * (1 + 4^((a.mp / a.mmp)^2))) Arcane damage.

Magic Amplifier:
Arcane gain! Generate a feedback loop, granting an ally +50% Intellect, and +x% Arcane damage dealt, where x is Kowalczyk's mana.

Revitalize:
Converts some of Kowalczyk's mana into a weak heal, restoring 15% of 1x Intellect * current mana health.
This dispels Kowalczyk's active buffs.

Fuel Up:
Hey, he's not an alchemical engineer for nothing! Synthesize some alchemical fuel, pass it through the Manafold, and regenerate 24% of Kowalczyk's mana. This is a very labor intensive process and will require 3 turns.

Overload:
For 5 turns, Kowalczyk lets an ally's mana can flow past it's normal cap.
Cannot be used on Kowalczyk. Can be used once per battle.

### Camellia:

Reordered her skills to be more like Jade's.

Path of Mastery has been redesigned.
New design:
Each time Camellia continues a Combo, she restores 5% of her missing health. Whenever she finishes a Combo, her next attack will Critically Strike.

### Cyrin:

Cyrin has been redesigned.

New design:

Ice Spikes (Passive):
Cyrin's basic attacks apply stacks of Ice Spikes to enemies, up to 5 stacks per enemy. She also takes -20% Frost damage and is Immune to Frostburn.

Unleash Frost:
Tear all Ice Spikes from enemies, dealing 3x Intellect damage per spike. Grant Cyrin Unleashed Frost after use.

Frozen Lance:
Deal 5x Intellect damage to an enemy.
Unleashed: Critically Strike and apply 2 stacks of Ice Spikes.

Flurry:
Deal 2x Intellect damage to an enemy once, then random enemies 4 times.
Unleashed: Hit 3 more times, first hit Exhausts.

Howling Winds:
Exhaust all enemies.
Unleashed: And Frostburn them.

Cold Snap (Heroic):
Deal 6x Intellect damage to all enemies, Stun them, and apply 3 stacks of Ice Spikes to each.

### Farel:

Hardened Frame has been removed. Farel is now naturally Immune to Burn.

Hellfire has been redesigned.
New design and name, Pyrocheck:
Deal 3x Intellect damage to all enemies. Burn any that are weak to fire, and deal +3x damage to any that are resistent.

Boosters have been redesigned.
New design:
Farel sacrifices 20% Gauntlet Power to go first next turn.

### Hyria:

Illusionary Weaponry, Backfire, and Arcane Blast now cost 20 mana each (was 10 mana).

Fixed an error with Illusionary Weaponry and Backfire's code. Not sure if it did anything.

Aether Feast now checks for Hyria's mana, so she can no longer use it with less than the minimum.
Aether Feast now always performs the maximum possible version.
Aether Feast's mana range is now 10-30% (was 5-15%).
Aether Feast now deals +4x Intellect damage per value (was +3x).

Ambitious Incantation has been redesigned.
New design:
Hyria fully restores her mana, but takes 25% Recoil damage from her spells for 3 turn cycles.

### Jade:

Jade no longer has stance exclusive passives.
New passive, Tough as Nails:
Jade takes -20% damage from Elemental attacks, and receives +15% healing.

Sentry is no longer restricted to front row allies, and no longer has any form of cooldown.

### Luna:

Luna is now able to be controlled during The Black of Night.
The Black of Night now only lasts 5 turns (was 6).
Lunar shifting into Eclipse now displays The Black of Night's name.

### Phoenix:

Magma Reserve no longer triggers incorrectly while at full health.

Rune of Magmardon now properly grants Shields.

### Rayzon:

Ley Shield has been redesigned.
New design:
If Rayzon would lose more than 10% of his current health from an attack, he takes 35% less damage.

### Sel:

Replaced Charming Toxin with Reversal Toxin:
Target takes 20% Recoil damage from their actions for 3 actions.

### Uiharu:

Something was wrong with Reacting Spark's code.
I don't know if it caused any problems but I fixed it.

Beat Up's name has been changed to Ultrashock.
Ultrashock's minimum number of hits is now 3 (was 2).
Ultrashock now deals 2x Intellect damage per strike (was 1x Strength and 1x Intellect).
Ultrashock now deals Storm damage instead of Physical damage.
Ultrashock hits no longer count as basic attacks (it still generates 3 stacks of Static Shock per hit though).

### Xelth:

Xelth no longer needs to maintain the balance.

New passive, The Resilience:
Xelth is Immune to most CC, but takes +20% damage.
Xelth's allignment changes depending on his last basic attack target.

Sunder and Life Link are now available based on Xelth's alignment.

### Zivian:

Fixed a bug that caused Immortallity to never revive Zivian.

Epidemic now actually requires multiple targets, so you can't waste it.

Burrow is now dispelled upon Zivian's death.

## ENEMIES

Dryad Scout's Multishot can no longer hit the same target twice.

Golmeg's Glare now properly acts like a magic, multitarget attack.

Cultist's Fetid Ground now only has a 50% chance to poison, but now deals some initial damage.

Halberdier Mermaid's Twin Cleave has been renamed to Brutal Cleave, and now only strikes once.

Vyn's boss fight has been redesigned.
It might get redesigned again because I really don't like his design anymore.

Zeriph now only heals to full health after he reaches 30% for the first time. He heals again for less the second time, and cannot heal again past that.
Bloodsworn Pledge now only targets 1 Mage, and has had its cooldown reduced to 3 turns (from 5).

Updated Zeriph and Vyn's dialogue, again.

## LOCATIONS

The main Golden Way path now cuts through Leylight Hollow, instead of skirting its edges.

Removed the desert area from the Lake of Outcasts. It didn't make sense.

Instead added the Oasis, a dusty valley created by magic experiments.
The old Vynfall enemies and boss rush have been moved here.

# Global Configuration
## Problem
Imagine the following example, almost all the games that you play use the `E` key to access the inventory, cool, next to `WASD` and easy to access while you play. Then you open a game and suddenly the key is no more `E`, its now `TAB`.

Okay, things change, maybe this is a space game and the `Q` and `E` keys are used to rotation, but now you open another game and you find now that the inventory is opened by pressing `I`. That slowly becomes yet another little inconvenience in the player's life. I should start by saying that I don't like it, but there's nothing evil about it, its just different design decisions.

## Solution
But what if we made a solution to unify all the keys? Well, seens ambitious, and it surely is! But hear me out. If we use a global configuration scheme, and share the keybinds between games, it could be more confortable for the player, don't you think? Let me make it clear that this is a opt-in feature that developers can just ignore while using UE, but its there for the ones that want to test and see it.

Now if you set the inventory key to `TAB`, it will be saved as a global configuration, and all other games made in UE that read from the global configuration will use `TAB` for the inventory key, how awesome ins't it?

But theres more, this is not a strict rule, the player is also capable of choosing what keybinds will be local or global, that way the players that don't like it can opt-out of this feature.

## But Why?
The problem described earlier is just a minor annoyance, but imagine you have some sort of disability and uses a very special set of hardware to control the game, now things become harder and annoying, imagine yourself in this situation where you need to rebind all the keys everything you enter a new game. No one should be forced out of the fun more than one time!

I should say that sometimes your hardware lacks some keys and rebinding them is always a pain, for instance I have a 60% keyboard and made the huge mistake of not checking if there were arrow keys, now I'm stuck with this keyboard that make some 2d games a huge pain to play.

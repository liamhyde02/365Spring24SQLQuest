Example Flows #1:
**Player wants to equip an item and begin a quest**

Rain, the adventurer, comes into town seeking to begin a quest.
First, he must equip his trusty sword. He requests to see his inventory by calling GET /inventory/45 where 45 is his character ID.
Rain sees his health potions, armor, and most importantly he sees his trusty sword. 
That sword has an id of 8, so he calls POST /equip/45/8, which marks that sword in his inventory as equipped.

Now ready to undertake the newest quest, he requests to see the quest board by calling GET /quests.
Rain checks the list of quests being offered. A goblin eradication quest for 70 gold, a merchant escort request for a new helmet.
Rain wants that new helmet, so he calls POST /quests/45/86, where 86 is the quest_id number for that merchant escort request.
Now off Rain goes with his trusty sword equipped to help that merchant and earn himself a shiny new helmet.



Example Flows #2:
**Player completes a quest and wants to buy a potion from a shop**

Rain completes his quest and returns to town. He looks at the shop inventory by calling GET /shop, which returns a list of
available items. Rain decides he wants to buy 3 healing potions, so he fills out a POST request with "Healing Potion", 3 and
sends that into the shop. Rain receives 3 potions and is fully healthy for his next quest. 

Example Flows #3:
**Player creates a character, but immediately regrets the name they gave their character and seeks to change it**

A player by the name of Steve wants to create a new character, an adventurer by the name of Bloodfeather after his favorite band!
So Steve goes to the character creator and inputs the character's name Bloodfeather and calls POST /character.
This creates the character, and further API call /character/109/inventory (109 is Bloodfeather's character ID) will add the starting inventory.
Steve is about to finalize, when he gets a notification on his Bloodfeather facebook group.
The entire band has been exposed for hating SQL optimizations and random Taylor Swift trivia. This cannot stand. Steve can no longer support them.
He deletes his facebook group, but now realizes he does not want a character named after a band that hates swift queries and queries about Swift.
He goes to the rename form and inputs his character's new name, one that will bring justice to both.
Steve then calls /character/109/rename to officially rename his character.
Finally, he calls /charater/109/create to finalize his character into the world.
Watch out world, for the adventurer now known as Pucas Lierce has just been created.

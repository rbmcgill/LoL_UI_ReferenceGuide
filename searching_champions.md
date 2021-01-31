# Searching for Champions
<hr style="border:2px solid gray"> </hr>
## API Description
The find_champion is an API call that allows players to find a champion in the Champion page of the Collection tab. Players can search for a champion by name, role, or location of origin. A list of suggested champions displays based on the player’s search term. Search terms can be complete or partial words.

## API Requirements
- Champion search parameters in order:
  1. name
  2. role
  3. origin
- Add any matching search term to the list of champion suggestions
- Display the champion suggestions to the player


**Example:** If a player searches for “gang”, Gangplank displays.
![Gangplank search](Collection_Champions_Search.png)

**Code:**
**Call**

`find_champion.

champion_data = [
 {
 'name': 'ahri',
 'role': 'mid lane',
 'origin': 'vastaya'
 },
 {
 'name': 'teemo',
 'role': 'top lane',
 'origin': 'bandle city'
 },
 {
 'name':'gangplank',
 'role': 'top lane',
 'origin': 'bilgewater'
 },
 {
 'name': 'sona',
 'role': 'support',
 'origin': 'ionia'
 },
 {
 'name': 'miss fortune',
 'role': 'marksman',
 'origin': 'bilgewater'
 }
]
def find_champion(name=None, role=None, origin=None):
 champion_suggestions = []
 for champ in champion_data:
 if name:
 if champ['name'] == name:
 return [champ]
 if role:
 if champ['role'] != role:
 continue
 if origin:
 if champ['origin'] != origin:
 continue
 champion_suggestions.append(champ)
 return champion_suggestions`

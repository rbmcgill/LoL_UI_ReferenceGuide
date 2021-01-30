# Searching for Champions

The find_champion API allows players to find a champion.

A list of suggested champions displays based on the player’s search term.

Players can search for a champion by name, role, or location of origin.

Example: Of the champions contained in the example data below, if a player searches for “gang”, Gangplank displays.

Code:
Call

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

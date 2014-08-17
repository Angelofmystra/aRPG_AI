MUD AI

This is composed of a few parts:

Area Awareness System -- in a vain similar to the Quake 3 AI, this subsystem aims to understand the game world. It maps the world of rooms to a graph. It creates two graph representations: an adjacency matrix, and an adjacency list. 

Omniscient Hunter -- the ai always knows the players location, and is able to find the optimal path to him. This is effectively the A* algorithm that re-evaluates itself each time the player's location changes. The main question is whether the OH can see secret (hidden) doors. If it could, then an AI could inadvertently find and reveal them to players who are observant. If it cannot see secret doors, then players could use them to avoid Omniscient Hunters (either temporarily, if there are alternate routes, or permanently, if there arnt). Then we'd need to know how "patient" the Omniscient Hunter is - if the AI cant find a route (or fast route) to the player, how long would it wait for the player until it gives up? Also, would it be aware of water? Using a weighted graph, we could easily handle usually unnavigable water. Would each AI's weightings depend on whether it can traverse various terrains? It would need its own area specific weights.

Guard_basic_aggro -- a pretty unintelligent AI. It stays in an area. It does not move. It may aggro if monsters of a certain kind are attacked.



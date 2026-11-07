# MG5
## Devlog
1.NavMesh movement and physics-based movement are two different ways to control characters in a game.
NavMesh movement allows a character to find a path and move toward a destination while avoiding obstacles. It is useful for characters that need to navigate around an environment. For example, in The Sims, characters need to move around furniture and other objects to reach different locations.
Physics-based movement uses forces, gravity, velocity, and collisions to control how objects move. For example, in Angry Birds, the birds and other objects move based on physics, including gravity and collisions.
In my MG5 project, I used a NavMeshAgent for Pudu. When the player clicks on the terrain, Pudu moves toward the clicked location. The NavMesh helps Pudu find a walkable path through the environment instead of simply moving in a straight line.
I think NavMesh is more suitable for this project because Pudu needs to explore a terrain with trees, hills, and other obstacles.

2.In this activity, I worked on the BirdManager script to make the birds run away when Pudu gets close to them.
First, I fixed the for loop so that it can check every bird in the _birds array.
The correct loop is:

for (int i = 0; i < _birds.Length; i++)

The loop starts at index 0 because arrays in C# start counting from 0. The condition i < _birds.Length makes sure that every element in the array is checked without going outside its boundaries. i++ increases the index after each iteration.
Next, I used Vector3.Distance() to calculate the distance between each bird and the player (Pudu).
If the distance is less than or equal to _interactDistance, the BirdManager calls:
bird.RunAway(_player.position);
This tells the bird to run away from Pudu.
In my scene, I added three birds to the Birds array in the Inspector and connected Pudu to the Player field. Now, the script checks all three birds every frame. Any bird that comes within the interaction distance of Pudu will run away.
This activity helped me understand how arrays, for loops, and Vector3.Distance() work together to create interactions between game objects.

Through MG5, I learned how to create and edit terrain, paint terrain textures, add environmental details, and bake a NavMesh. I also learned how to use a NavMeshAgent to move a character based on the player's mouse clicks.
I had some errors while working on the scripts, especially with the for loop in BirdManager. After fixing the loop and checking the array references in the Inspector, the birds worked correctly.
Overall, this activity helped me understand how navigation, scripting, and environmental design work together in a 3D game.
## Open-Source Assets
- [Quirky animal 3D models](https://assetstore.unity.com/packages/3d/characters/animals/quirky-series-free-animals-pack-178235)
- [Mountain fantasy environment models](https://www.fab.com/listings/60487a72-3f20-4bb2-aa78-247ed1582656)

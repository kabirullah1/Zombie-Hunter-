# Zombie-Hunter
In this section we create a First Person Shooter with a zombie theme. We cover raycasting for shooting and the core mechanics you'd expect in an FPS.

## In This Section

In this section we create a First Person Shooter with a zombie theme. We cover raycasting for shooting and the core mechanics you'd expect in an FPS. 

## How To Build / Compile


### 1 Welcome To Zombie Hunter ##


## 2 Zombie Hunter Game Design ##

1. Discussion of the game overview screen and core features.
2. Reminder that we're using Unity 2019.1.

## 3 Adding First Person Controller ##

1. Download Unity Standard Assets.
2. Implement the First Person Controller with RigidBody.
Get and add the First Person Controller to our scene.

### 4 Make A Prototyping Sandbox ###

1. Use Unity's simple prototyping geometry to make a simple level.
2. There are different obstacles to test the expected functionality in the game.

Create a simple sandbox level for prototyping.

### 5 Using NavMeshAgent For AI ###

1. Add a placeholder enemy with NavMeshAgent component.
2. Bake our NavMesh.
3. Create EnemyAI.cs and add logic to move the enemy towards the player.

Use the NavMeshAgent component to drive the enemy towards the player.

Fix some issues with our first person controller.


### 7 Enemy AI - Chase Range ###

1. Make the enemy and player more obvious in their positions.
2. Create logic that tells the enemy to move to the target if the target is within the chase range.

Move the enemy to the target if the target is within range.


### 8 Using OnDrawGizmosSelected() ###

1. Use the Unity docs to figure out how to draw a gizmo which shows the chase range of our enemies.

Use gizmos to visualise chase range.


### 9 Enemy AI - Attack If Provoked ###

1. Structure our EnemyAI class so we have logic for the enemy being provoked.
2. Use the nav mesh stopping distance as part of our conditions for attacking or not.

Add to our enemy AI, causing it to attack if provoked.


### 10 Give That Player A Gun ###

1. Import a weapon and attach it to the player.
2. Add a reticle the the UI canvas.

Give the player a weapon asset.

3. Add a ray that is cast when the player clicks their shoots (clicks their mouse button).
4. Print to the console the thing that we hit.

Implement raycasting so we can shoot an invisible laser beam.


### 12 Enemy Health & Damage ###

1. Create a public method that reduces enemy's health.
2. Call that method from our weapon and pass in the weapon's specific damage amount.

Lay some smack down on an enemy (well, decrease its hit points).


### 13 Implement A Muzzle Flash ###

1. Create simple code to play our muzzle flash.
2. Create a particle system that looks somewhat like a muzzle flash.

Create a muzzle flash particle effect and play it when the player shoots.


### 14 Creating Shooting Hit Effect ###

1. Twiddle with one of the standard assets particle effects to get something we like.
2. Instantiate the hit impact at the point the raycast hits.

Instantiate a hit effect when we shoot something.


### 16 Creating A Simple Animation ###

1. Create a new animation that we add to idle state.
2. We can animate properties such as the transform of an object.

Add simple animations to our animator controller states.


### 17 Animator Transition Conditions ###


1. Set up a trigger and a bool parameter.
2. Cycle through our states by trigging our transition conditions.

Trigger different states based upon parameter conditions being met.


### 18 Trigger Animation In Code ###

1. Add code to trigger move state.
2. Implement attack state bool to set to true or false depending upon enemy AI logic.

Use code to trigger animation state changes.


### 19 Use Animation Events ###

1. Create EnemyAttack.cs and create a public method that can be called as an animation event.
2. Create simple animation for attack and add an animation event which calls our attack code.

Use animation events to create precise attack moments.


### 20 Create Player Health Class ###


1. Nifty challenge where you get to chose your difficulty level.
2. Have the enemy damage the player.

Complete our loop where the enemy can hit and damage the player.


### 21 Rotate To Face Target ###

1. Discuss briefly how Vectors work.
2. Rotate the enemy to face the player by using Quaternion.Slerp().

Be clear on to rotate an object so that it is facing another moving object.


### 22 Game Over User Interface ###


1. Create a Game Over canvas with buttons to reload game and quit.
2. Create a class which contains the methods with the functionality for our buttons.

Create a simple game over menu to ensure we can restart the game when the player dies.


### 23 Create A Death Handler ###

1. Disable and enable our game over menu screen.
2. Give the cursor back to the player.
3. Stop the game so that we aren't seeing weird cursor fighting issues.

Elegantly handle displaying and using the Game Over menu when the player dies.


### 24 Using BroadcastMessage ###

1. Our goal is to have the enemy provoked when shot.
2. We look at a couple of ways to do this, one of which being BroadcastMessage().

Use BroadcastMessage() to call any methods of a particular name on our Game Object.


### 25 Early Gameplay Loop ###

1. Tidy up our sandbox and make a bit of level flow.
2. Tune our Player and enemies so that the game feels the way we want.


### 26 Weapon System Overview ###

1. Examine Rick's prototype to look at the weapon switching, ammo system and ammo pickups.

Be clear on what we are about to undertake with our weapon system.


### 27 Weapon Zoom - Field Of View ###

1. Figure out what would give us a zoomed in effect.
2. Create a connection to our camera and variables for zoomed in and out FOV.
3. Create logic that toggles between zoomed in and zoomed out.

Clear on to use a camera's field of view to zoom in and out.


### 29 Basic Ammo Functionality ###

1. Create Ammo.cs and add 2 public methods to allow our weapon to communicate with our ammo.
2. Create logic so we can only shoot if we have more than 0 ammo and to decrease ammo each time we shoot.

Add basic ammo functionality where we decrease our ammo when shooting and can only shoot if we have enough ammo.


### 31 Weapon Differentiation ###


1. Create a delay between shots for our weapon.
2. Tune the damage, range, scope and shot delay for our three weapons.

Create a shooting delay and how to differentiate our 3 weapons.


### 32 Set Active Weapon ###

1. Create a foreach loop which loops through our weapons and sets them active or inactive.
2. Create the framework for the player to be able to select their weapon.

Create the framework for setting weapons active or inactive.


### 33 Player Input To Select Weapon ###

1. Create a way for the player to change weapons by pushing the keyboard numbers.
2. Create a way for players to change weapons by using the scroll wheel.

Give the player multiple ways to change weapons.


### 35 Different Weapon Different Ammo ###

1. Assign our weapon to be a particular ammo type.
2. Hook everything up so our weapons decrease ammo from a specific ammo slot.

Have specific weapons use specific types of ammo.


### 36 Quick Bug Fix ###

1. Identify why our weapon is staying zoomed.
2. Fix the issue.

Practice finding and fixing bugs.


### 37 Ammo Pickup ###

1. Create a game object which is triggered when the player runs through it and destroyed, printing a witty message to the console in the process.

Create a simple pickup framework that can only be triggered by the player.


### 38 Ammo Pickup  ###

1. Set the value and type of the pickup.
2. Create a public method to increase ammo amount.
3. Create prefab variants for each pickup type.

Increase specific types of ammo when we collect that an ammo pickup of that type.


### 39 Add A Zombie ###

1. Import enemy character asset.
2. Hook up new animations to our animator.
3. Add code to trigger enemy death and stop weird death-related behaviours.

Make your game 5 times more awesome by having an enemy who actually looks like an enemy.


### 40 Quick Zombie Attack Challenge ###

1. Figure out why our zombie is not hurting us.
2. Implement a fix to this problem.

Practice hunting down an issue and implementing a solution.


### 41 Flex Your Level Design Muscles ###

1. Create a new scene that will be a more organised level.
2. Sketch out a level design and import that into the scene to use as a reference diagram.

Create a level design diagram to use as a reference for the level creation.


### 42 Add Terrain & Trees ###

1. Add terrain and sculpt it, being sure to add elevation changes.
2. Add trees.
3. Add grass texture and mesh.

Make our forest look interesting by adding terrain and trees.


### 43 ProBuilder For Making Props ###

1. Instal ProBuilder.
2. Use ProBuilder to make shotgun shells.
3. Use ProBuilder to make bullets.

Get comfortable with ProBuilder by making props.


### 44 ProBuilder To Make Rooms ###

1. Install ProGrids.
2. Create the shell for our first room.
3. Create a separate game object that is the roof.

Comfortable using ProBuilder to make rooms.


### 45 ProBuilder To Make Levels ###

1. Use ProBuilder's Poly Shape Tool to trace around our entire level sketch.
2. Flip the normals of our level so we can see the walls on the inside.
3. Add elevation and link everything up.

Comfortable using ProBuilder to make levels.


### 46 Adding Textures With ProBuilder ###

1. Import some textures.
2. Use ProBuilder's Material Editor to add textures.
3. Use ProBuilder's UV Editor to tweak the look of the textures.

Comfortable using ProBuilder to add textures and materials.


### 47 We Need Some Lights ###

1. Create a light with an emissive material.
2. Place lights in our scene.

Able to place emissive lights in your scene.


### 48 Create A FlashLight ###

1. Create a flashlight that is attached to the player.
2. Decay the flashlight angle and intensity over time.

Create a decaying flashlight.


### 49 Create A Battery Pickup ###

1. Create 2 public methods on our flashlight which increase angle and intensity.
2. Create a battery pickup which calls the 2 public methods.

Create a battery pickup which restores the functionality of our flashlight.


### 50 Display Current Ammo UI ###

1. Tidy up, add enemies, rebake navmesh.
2. Add code and UI to display the player's ammo for each weapon cycled through.

Display the ammo for the currently wielded weapon.


### 51 Damage Received UI ###

1. Add some cool effect for when the player takes damage.
2. Trigger the UI effect by turning on and off the canvas.

Provide the player visual feedback for when they receive damage.

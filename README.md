# SECTION 7 Game Asset Pack

****

Part of the Complete Blender Creator course on Udemy, see [here](https://www.udemy.com/blendertutorial/?couponCode=GitHubSpecial) for a special GitHub offer. The full course is part of [this](https://www.kickstarter.com/projects/bentristem/how-to-create-3d-assets-using-blender-online-cours) Kickstarter campaign which was 1000% funded.

Click [here](https://www.udemy.com/blendertutorial/?couponCode=GitHubSpecial) to find out more about the course, and how we build these assets step-by-step.

These are just the files from the course, not the actual tutorial videos. At the time of writing this course has several hours of high-quality videos.

You're welcome to download, fork or do whatever else legal with all the files!

Enjoy yourselves.

Ben Tristem & Michael Bridges

*Below is a rough projection of the topics in this section and is a copy from previous Gothic Church Section*
*This will change as this section is fleshed out*

## Section Introduction

* You are going to make several models. 
* We’ll be making both high poly and low poly versions of out assets.
* We will emphasise how critical naming is when working with a larger project like this.
* You will be able to create your own mapping, with these we can make the illusion of detail.
* We’ll be constantly checking our model externally
* This will be focused mainly on an interior environment.

## Section Specification

* Create assets to be exported straight into an external program, like a game engine.
* Creating our own textures, and other maps from high detail models and apply them to a low poly version.
* Only modelling the interior of the Gothic Church.

* You can use this technique within Blender itself too for optimisation. 
* I am going to be testing my model externally as I go. I will use Unity to do this.

* I will be keeping my scene simple, primarily for teaching purposes! 
* I encourage you to add more detail, experiment and have fun. Wouldn’t the scene look much more interesting with a chess set in it.

## Planning Your Project
* Plan your project, define it’s scope and your goals- important to prevent scope slip!
* Gather your reference material, if possible explore real world locations to get a feeling. Scour the web for images for you references too.

### Building Blocks & Modular Thinking
* Think about ways of building that make parts reusable and modular… Think Lego.
* Realise this gives you quick iterations, and great prototyping potential from a few parts.
* If you are supplier of assets your level maker is going to love that they can redesign with your assets!

## An Overview of Source Control
* The what and why of Version Control Systems
* Choosing your Version Control System (VCS)
* What files to include / exclude
* Commit = save a local snapshot
* Reset = roll-back to a previous state
* Branch, Push and Large File Support later.

### Popular Version Control Systems
* Git
* Mercurial
* Perforce
* Subversion / TortoiseSVN
* Alienbrain (for art but of order $10,000)
* https://en.wikipedia.org/wiki/Comparison_of_version_control_software

### About SourceTree
* Free software by Atlassian
* Visual front-end for Git or Mercurial
* Mac and PC but Mac version is a little ahead
* Good when learning as easy to visualise.

## File Structure & Naming
* Understand that there is NO one way of setting up your filing system. 
* Have a personal style of filing, if you don’t like mine, use yours.
* Talk with your ‘team’ you will form guidelines from your own needs.

### Some Rigidty
*In a Team environment you will have guidelines or discuss with colleagues.
* Some other software might expect certain things to be stored and named in a certain way.

### Naming
* In a Team / larger project it is critical that you can find assets, materials, textures.
* Naming files well will help you and others.
* There are some naming conventions that we will use in this section.

### In Blender Organisation
* We are going to be making a much more complex scene than any previously made.
* Organise it as you go, not afterwards!
* Use description names, cube, cube.001 etc is not helpful to anyone!

## Level Of Detail (LOD)
* Focus on representations of the right size and shape, but JUST Block work models.
* This allows quick iteration of your models.
* Remember higher detail ofter requires more processing time too!

### LOD Numbers and Letters
* LOD 0 often refers to the highest detail model sometimes called the base model.
* To avoid confusion, we are going to use Letters!
* A represents the lowest polygon model, with B,C,D etc increasing in detail.

### Watch Your Time / LOD
* LOD and time taken at usually directly proportional to one another.
* When fleshing out a scene and prototyping you probably want quiet a few assets. 
* You can test models and your scene quickly.

### LOD vs. Time Taken Example
#### “LOD”
* A - B - C - D
#### Polygons*
* 200 - 2,000 - 20,000 - 200,000
#### Time Taken**
*30mins - 2 hours - 1 day - 1 Week+

*Every polygon counts!*

*Time includes other artwork too*

## Setting Up Our Repo & Committing
* Setup Up Our Repository.
* Register SourceTree.
* Learn how to exclude data from our repository.
* Stage our files.
* Make our first commit.

### How Many Repositories?
* You could use a repo per model that you create, this would give you the best level of control.
* You could track your whole project in a repo.
* It will depend on the complexity of your project and how much control you NEED.

### Excluding Data
* Allow faster commits at a smaller size and keeps the database simple and manageable.
* Avoid storing derived / generated data in the repository.
* Example here: will be our reference material.

### Committing
* You’ll need to save all the documents that constitute that commit first.
* Just like saving your working folder and zipping it up at that moment in time.

## Repetitive Tasks In Blender
* Learn how to manage repetitive tasks.
* Understand good uses for appending an Blend file into your scene.

## Using Our Building Blocks
* Set your commit message before working
* Start building your building.
* Notice a few issues and work out a way around them.

## Introduction To Datablocks
* Learn about Datablocks.
* Understand that knowing about them is about to become much more important.
* We have come into contact with data blocks lots but let now go and explore them directly.

### Datablock’s Characteristics 
* Must have unique names per type. 
* Can link to each other.
* Can link across blend files.
* Unused Datablocks are eventually removed.
* This is Where we have used Fake Users in the past to preserve that particular datablock.

### Sharing Datablocks Example
* The same texture on many materials.
* The same material on many meshes.
* The same particle system and so on.
* We will often share and then make the data block unique.

## Linking To An External Datablock
* Learn more about linking to another blend file.
* Link an object datablock.
* Understand that there is a datablock hierarchy.
* Keep an eye out for when you might loose data.

## Linking Blend Files: Making a Proxy
* Learn more about linking datablocks.
* Understand what is happening when you link.
* Realising when you need to use a Proxy.

### Make Proxy
* Creates a New object, that is a parent of the linked data.
* Allows transformation of an object.
* Can now Scale, Move, Rotate etc.
* Otherwise exactly the same as the linked file.
* The object datablock is linked to original and any dependant datablocks.

## Linking Blend Files: Making Local
* Learn why you want to make a linked datablock local.
* Understand we are starting to sever links by doing this.
* Learn about the various stages of making it local.
* Decide when would be a good time to localise a datablock.

### Advantages And Disadvantages
* Advantage: You will have more local control.
* External files moved, project can stay together.
* Disadvantage: Potentially more work involved.
* Any edits you make on the original affect all linked data blocks but not the ones made local.

### When Do you Localise?
* When the link is not required.
* When you want to make the asset unique in this particular file.
* When you want to make changes irrelevant to other potential projects.

### Make Local: Option 1
* Selected Objects: Clones the object Datablock to the new blend file.
* All other datablocks remain linked to the original file.
* This allows changing of anything in the object datablock.

### Make Local: Option 2
* Selected Objects and Data: Clones the object & data Datablock to the new blend file.
* This allows editing of the mesh data, breaking that link and making it a local file. 
* The materials & other datablocks remain linked to the original object.

### Make Local: Option 3
* Selected Objects, Data and Materials: Clones the object, data and materials Datablock.
* This allows editing of the object data & materials datablocks. 
* Breaks those links, making them local to this file.

### Make Local: Option 4
* All: As it sounds, this is pretty much the same as appending the object into the scene. It is now entirely local with no links to the original file.

## Walking And Flying Around The Model
* See how our scene looks and feels walking around it. Using the Fly / Walk Mode.
* Show you how to see the scene in Unity.
* Understand I am using Unity to keep the iterations quick and simple at this early stage.

###Unity Is Optional
* Anything external to Blender, you can watch to see how it works and is coming across.
* Better understanding of external programs.
* Join in, if you have Unity installed and are interested in learning more about this prototyping method.

## Better Camera Control
* Use a different way of moving the camera.
* See this gives you better control over what the camera is pointing at.
* Combine with fly mode for good control.
* Learn how to track a target.

## What Can You Export?
* Understand what will export
* Realise some elements of your models will not export or will once, or not properly.
* Depends on the target package.

### What Appears on Import
* Mesh data including UV Maps. 
* Armatures and animation data will appear too if supported in the target package.
* Textures may appear or simple the base diffuse colour.

### Reconstruction
* Textures often have to be reapplied.
* Shaders work differently in other packages.
* Materials would have to be remade.
* Particle systems are local to Blender.
* Test

## Re-linking Blend Files
* Make a commit!
* Understand the order you NEED to do things in if you wish to change a linked file or it’s datablocks.
* See what happens if you change a link.

### Moving or Renaming Blend Files
* Make a commit!
* COPY file(s) to new location.
* Rename the COPIED file(s) appropriately.
* Doing it it any other order will break links.
* Any links broken when saving will be lost forever!

### Moving or Renaming Datablocks
* Make a commit!
* COPY file(s)
* Open up Copy and make datablock adjustments.
* Link new file into scene.
* Make links to the new object, replacing the old.
* Delete / Archive Old Blend file.

## Profile Modelling By Extrusion
* Understand what a “profile modelling” is.
* Potentially speed up modelling by mirroring.
* Use a series of methods to produce a profile that we can use in our scene.
* Future: Use the same profile in different ways

### Profile Modelling
* A profile is the outline you get when you view something from a particular angle.
* Imagine slicing through your model.
* Realise we have used them in the past: Lamp Base was produces with curves and the Pin was geometry based.

### Methods Used
* We’re going to bump up our extrude speed
* We’re going to be using the bevel tool for construction and defining sharp edges.
* A subsurface modifier for making the surface.

## Profile Modelling Using Curves
* Create some alternative detail.
* Convert Mesh objects into a Curve objects.
* Use those 2 curves to create geometry, one controlling the profile, the other a path.
* See this is great for more accurate path following.

——
Videos in this section of the [full Udemy course](https://www.udemy.com/blendertutorial/?couponCode=GitHubSpecial)...

---

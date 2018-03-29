# CARDS MANAGEMENT PATTERNS

from original C2 wiki

## Index Card
An index card (also called a SystemCard) is a small rectangular piece of thin cardboard or thick paper, suitable for writing on, frequently ruled on one side or both. Popular sizes in North America include 3x5" (76x127mm) and 4x6" (102x152mm). In countries where metric paper is used (Germany in this case) probably the most common size is A7 (74x105mm), smaller ones (A8 = 52x74mm) are also used, as are bigger ones like A6 (105x148mm) or A5 (148x210mm).

Index cards can be used for many things:

    used in a PersonalAnalogDevice.
    used as CrcCards
    used as a DataBase http://www.absolutewrite.com/novels/index_cards.htm
    used for project management. The logistics for the Gulf War were managed on index cards. Read "Moving Mountains" by Lt. General George Pagonis.
    used as StoryCards 

## Write It On a Card
UserStory is a special case of a more general pattern, WriteItOnaCard. Here's general discussion, not in pattern form.

Got something to do? Write it on a card. Carry the card around till it gets done. Then throw the card away or put it in a box of things that are done.

Got lots of things to do? Take your cards and do CardTriage on them. Then pick the ones of most immediate value for doing now and do them. SitOnTheOtherCards.

Want to know how long it will take to get done? Take your cards and write a time estimate on each one. See about dividing them up among other members of your team, or other personalities if you have them. Lay them out on a schedule.

Need to be done by next Tuesday and have TooMuchToDo? Lay them out, put a pencil on the table where the deadline is, and do the math. Move the things you are going to do to the left of the pencil, move the ones you aren't going to do to the right, until you get the best possible schedule. Then SitOnTheOtherCards.

UserStory extends this life strategy with the usual rococo frills for which XP is famous. Business value, risk assessments, estimates, tasks, all that stuff. Software development needs all that stuff. Often all you need to do is WriteItOnaCard.

In particular, experience suggests that all the management and scheduling for a small-population project can be done this way. --RonJeffries

## StoryCards

I read all the various comments about user stories and sense there is a serious lack of consensus regarding just what a UserStory is. English speakers typically think of a story as some kind of narrative that describes a WHO, WHAT, and WHY scenario. So, from that perspective, it is doubtful to me that a story is going to be at the brief, functional level a programmer needs to develop code.

Therefore, I suggest that the USER STORY is indeed a narrative that a user tells from her own perspective. This story typically describes some kind of scenario or situation that the user finds herself in. The programmers must then work with the user to derive from that narrative the specific USER TASKS that the user must to perform with the software to successfully accomplish the story.

For example, here is a real USER STORY:

    A project manager needs to set up a web-based location where all the members of her team can access engineering drawings, models, research findings, meeting minutes, and schedules associated with their latest project. This will help the team stay in synch regarding the progress of the project. It will also prevent the current problem of storing data in different places that not everyone can access.

And here are USER TASKS we derive from the story: 1. Create a project on the web. 2. Create folders in the project. 3. Transfer files to those folders.

And if the user makes any mistakes regarding the name or location of a project, folder, or file, she must be able to: 1. Rename a project, folder, or file. 2. Move a folder or file. 3. Delete a project, folder, or file.

I think you can see that it is the user TASKS, NOT the STORY, that represent those chunks of functionality that can be estimated, prioritized, and then implemented by the software programmers. 

## COLOURS

In college I used cards to organize concepts for a particularly difficult paper. I tried colored cards (not enough colors) and dots on the cards (not easily categorized in a deck). I solved this by using colored markers, and coloring the top-right corner (about a 1cm x 1cm triangle), INCLUDING the card edge. You get as many colors as you want, plus you can see the colored corner when the cards are in a stack.

## CARDS RACK

Suppose you have a bunch of 3 x 5 (inch) cards that you want to 
 organize on a wall or similar vertical surface....


 Get a large piece of strong paper-like material. Make alternate 
 valley and mountain folds across the paper.  Make the mountain 
 folds 1 inch below the valley folds; the valley folds 2 inches below 
 the mountain folds. When you have finished folding, the paper 
 should appear pleated. Bind the edges with tape.


 Fasten to the wall. Stick your cards in the pockets. 


 A large Federal Express envelope is a good source of material for a 
 small rack. If you want to do an entire wall, try Dupont Tyvek 
 House Wrap. Buy it at Home Depot. It's similar to the FedEx 
 envelope material.


 I haven't made a large rack like this but I do have a couple of small 
 ones. I also have a one pocket version taped to the top of my 
 monitor to hold cards for immediate work in progress.



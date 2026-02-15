---
layout: past_project
title:  The Scotland Yard
type: past_project
nav_name: Scotland Yard

project_name: The Scotland Yard - Bachelor's Thesis
project_description: |
    My Bachelor's Thesis project, which focused on the Board Game Scotland Yard and its derivatives. The goal was to implement the board game as a video game for one player against the computer. To do this I had to implement strategies for the computer opponents to play against the player.

    The thesis goes over the rules and specifications of the game. The it discusses different goals and strategies for the various versions. Based on these, an architecture was designed to best fit the specifications. A main game core was built which makes sure all rules are followed and then the computer opponents were made.

    I used Avalonia (C#) for the GUI for the application, which proved fruitful as it made the application compatible both with Windows and Linux systems.

project_postmortem: |
    The opponent playing as the Seekers (Detectives) works quite well - it is actually quite difficult to win against them. The Fantom opponent is not as good. The algorithm I used clearly needed some more tinkering to be on par with its counterpart. Using a traditional solution (Monte-Carlo, Minimax search) probably would have been better. 

    Overall, I was happy with the algorithm I designed. I think it could be used in combination with Monte-Carlo to make more informed choices in branch selection.

    The actual application is good enough - works well on both Windows and Linux (as far as I was able to test it). The architecture behind it also allows using the "game engine" in any other framework (like Unity for example). 


---

The full text of the thesis is available <a href="https://dspace.cuni.cz/handle/20.500.11956/202587">here</a> and the repository <a href= "https://github.com/tengu-blue/Fantom-Games">here</a>.

The goal was to ideally cover all the extensions of the board game, but that proved to be way out of scope for the thesis. As such, the game's core is prepared for future extensions. 

The base game was fully implemented including the opponents. I made a custom search algorithm, inspired by DFS due to the sheer number of possible states the game could be in. Instead of implementing an algorithm like Monte Carlo search, I opted for my own solution to see if it would be viable. The core idea is trying to assign values to states based on how likely they are to lead to victory, based on information that is available to the players.

The game uses a mechanic of hidden movement, so the core idea behind the state evaluation is in predicting where the players could currently be.

I also made custom art for the game to avoid legal issues with using someone else's art. 

<div class="gallery">
<img src="scotland1.png" >

<img src="scotland2.png" >
</div>
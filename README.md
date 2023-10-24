# Fifa-20

## PROBLEM STATEMENT
1. To Prepare a complete data analysis report on the given data.

2. To Explore football skills and **cluster** football players based on their attributes.

3. To Explore the data and attempt all the below asked questions in a step by step manner:
- Prepare a rank ordered list of top 10 countries with most players. Which countries are producing the most footballers that play at this level.
- Plot the distribution of overall rating vs. age of players. Interpret what is the age after which a player stops improving.
- Which type of offensive players tends to get paid the most: the striker, the right-winger, or the left-winger?.

- ## BUSINESS CASE

This case aims at exploring the football skills and **clustering** football players based on their attributes.
The dataset provided includes the players data for the Career Mode from **FIFA 15 to FIFA 20**. The data allows multiple comparisons of the same players across the **last 6 versions of the videogame**.

Exploring the FIFA data can be done by: Historical comparisons between players, Ideal budget to create a competitive team and at which point the budget does not allow to buy significantly better players for the 11-men lineup. An extra is the same comparison with the Potential attribute for the lineup instead of the Overall attribute, in addition, Sample analysis of top n% players to see if some important attributes such as Agility or BallControl or Strength have been popular or not across the FIFA versions. The trend (year on year ) of attributes is also an important indication of how some attributes are necessary for players to win games (a version with more top 5% players with high BallControl stats would indicate that the game is more focused on the technique rather than the physical aspect). Since this case is aims at **clustering** football players based on their attributes we will be using **K-Means** to evaluate the data.


## DOMAIN ANALYSIS
- The data consists of players attributes for the FIFA period 15, 16, 17, 18, 19, and also FIFA 20
- it consists of 100+ attributes including;

  a. Player positions, with the role in the club and in the national team
  
  b. Player attributes with statistics as Attacking, Skills, Defense, Mentality, GK Skills, etc.
  
  c. Player personal data like Nationality, Club, DateOfBirth, Wage, Salary, etc.

##  Attributes used in the project are:
- 1. **Name, Age and Height**: these attributes are specific to each  player.  
- 2. **Overall**: (rated 1-99) this is the overall/general performance and value of the player. (this attribute may be used only in preprocessing and discussion stages because using it in modelling could lead to domination by this feature.)
- 3. **Potential**:(rated 1-99) this is the Maximum Overall rating expected to be reached by a player in the top of his career
- 4. **PreferredFoot**: (0- left, 1-right foot< label encoded) preference towards Right or Left foot. 
- 5. **WeakFoot**:(left for righties rated between 1 to 5) describes How well a player uses his weak foot 
- 6. **WorkRate**: (0 for low, 0.5 for medium and 1 for high < label encoded) this expresses the Degree of the effort the player puts in terms of attack and defense. This feature is divided into two new features as AttackWorkRate and DefenseWorkRate. 
- 7. **Position**:(positions rated between 1-99) Position of the players on the pitch which determines their roles and responsibilities in the team. Forward positions in the football and FIFA 19 can be grouped as:

   ***Strikers***-  they are positioned in front of forwards and wingers and very closed to the opposing goal. their ball control, shooting and finishing skills are expected to be well.
   types: **ST**:center striker,**RS**-right striker, **LS**-left striker
  
   ***Forward***-  they have to be good at passing, the Right forwards and left forwards are positioned at the right and left of the center forwards. 
      types: **CF**: center forward, **RF**: right forward, **LF**: left forward) 
 
   ***Winger***-  Wingers are positioned near the touchlines.They are expected to be good at dribbling, acceleration, passing and crossing.
      types: **RW**: right winger, **LW**: left winger.
        
    **NOTE: Positions  are used only in preprocessing and discussion stages**

The following Skills are rated between **1-99**
- 8.  **Crossing**:Cross is a long-range pass from wings to center.
- 9.  **Finishing**:Finishing in football refers to finish an attack by scoring a goal.
- 10. **HeadingAccuracy**: Player’s accuracy to pass or shoot by using his head.
- 11. **ShortPassing & LongPassing**: Player’s accuracy for short & long passes respectively.
- 12. **Dribbling**: Dribbling is carrying the ball without losing while moving in one particular direction.
- 13. **SprintSpeed**: this is the Speed rate of the player.
- 14. **Acceleration**: Shows how fast a player can reach his maximum sprint speed.
- 15. **FKAccuracy**: Player’s accuracy to score free kick goals.
- 16. **BallControl**:this is the Player’s ability to control the ball.
- 17. **Balance**: Player’s ability to remain steady while running, carrying and controlling the ball.
- 18. **ShotPower**: Player’s strength level of shooting the ball.
- 19. **Jumping**: the Player’s jumping skill.
- 20. **Penalties**: Player’s accuracy to score goals from penalty.
- 21. **Strength**: the Physical strength of the player.
- 22. **Agility**: Gracefulness and quickness of the player while controlling the ball.
- 23. **Reactions**: Acting speed of the player to what happens in his environment.
- 24. **Aggression**: Aggression level of the player while pushing, pulling and tackling.
- 25. **Positioning**: Player’s ability to place himself in the right position to receive the ball or score goals.
- 26. **Vision**: Player’s mental awareness about the other players in the team for passing.
- 27. **Volleys**: Player’s ability to perform volleys.
- 28. **LongShots**: Player’s accuracy of shoots from long distances.
- 29. **Stamina**: Player’s ability to sustain his stamina level during the match.Players with lower stamina get tired fast.
- 30. **Composure**: Player’s ability to control his calmness and frustration during the match.
- 31. **Curve**: Player’s ability to curve the ball while passing or shooting.
- 32. **Interceptions**: Player’s ability to intercept the ball while opposite team’s players are passing.
- 33. **StandingTackle & SlidingTackle**: Player’s ability to tackle the ball from the opposite player while standing & sliding. these both are defensive skills.
- 34. **Marking**: Player’s ability to prevent opposing team from taking the ball. It is a defensive skill.  


# Amateur-s-sports-liege
Amateur's sports liege database
</br></br>
:football: | :soccer: | :basketball: | :tennis: | :bowling: | :8ball: | :trophy:
</br>
</br>
**The database will be formed following tables:**</br>
- Team(tid, nickname, color)</br>
- Player(pid, pname, address, phone, rating, tid)</br>
- Coach(cid, cname, address, phone, status, tid)</br>
- Game(gdate, htid, vtid, hscore, vscore)</br>
- Points(pid, gdate, htid, pscore)</br>


>The system keeps information on the data status in the current season only
</br>

**The system also keeps information about:**</br>
-	Liege's teams</br>
-	Liege's players</br>
-	Liege's coaches</br>
-	Season's games</br>
-	Season's points for players of selected games</br>
</br>

**Primary keys:**
-	tid = Team identifier
-	pid = Player identifier
-	cid = coach identifier
-	gdate = date of game
-	htid = host's team identifier
-	vtid = visited team identifier
</br>

**Notes:**
-	Every coach has a status (0 or 1) which defines the seniority of each one (which 0 is a new coach the 1 is a senior coach)
-	Player identifier and Coach identifier are taking from the same value field (tid&cid)
-	Every Coach and Player are related to a Team and there is no team without a Coach
</br>



**Trigger Function:**</br>
When adding points to the Points table, the program will check if the player is belonging to a team who plays in the specific game. If not, the user will get an EROR message, and the insertion of points will not take place. If the player does belong to one of the teams playing in the specific game, the insertion will occur and the points for the specific team will be updated
</br>
</br>

**Queries:**
| Query number  | Values to print      | Query         |
| :---          | :---                 | :---          |
| - Q1D -       | pname                | Players that have a rating > 3 and plays in group number 2     |
| - Q2D -       | nickname, cname      | Coaches that coach a group with a blue uniform                 |
| - Q3D -       | nickname             | For every game, the nickname of the winning team                 |
| - Q4D -       | cname                | For every new coach(status=0), the amount of players in his team                 |
| - Q5D -       | pname, rating        | A player who played in at least 3 games and never got a score (points) < 10 in a game                                            |
| - Q6D -       | pname                | For every team, the mvp player (mvp player = player who got the highest total amount                                           of all the team's games)                 |
| - Q7D -       | tid, nickname, color | From teams who has never won a game, the team that accumulated the highest sum of                                              points in all of it games                 |


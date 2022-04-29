---
title: Football stats - predicting goals!
date: 2020-02-17 09:00:00
---
| ![screenshot](https://media-exp1.licdn.com/dms/image/C4E12AQHZmur3zSrZVw/article-cover_image-shrink_720_1280/0/1581970813301?e=2147483647&v=beta&t=5oCrbgnKPL1zXaa4SM7EtGhL8bR8fBoASLS5pmjlkDI) |
|:--:|
| <b>Image Credits "CR7 / Cristiano Ronaldo"​ by Thomas Yuen is licensed under CC BY-NC-ND 4.0</b>|

<h3> What is xG? </h3>

In this article, let's explore what is "expected goals" or xG. xG is one of the most widely used statistic to assess performances of attacking minded players and overall team performance. It, in true objective sense, calculates if the shot once leaves the foot will result into a goal. For the scope of this article, we will look at goals scored during build up play and goals scored on corners. The same calculation and consideration extends to other set pieces and penalties as well.

Simply put, xG is the statistical inference of a dataset composed of hundreds of thousands of shots. If, for a given set of circumstances, players score 9/10 times, then, for when a similar situation arises, xG for the shot taken at the time of shot taking is 0.9. xG, therefore, by definition, is a continuously evolving number. After every match, xG values may update ever so slightly.

<h3> How is xG computed? </h3>

At the core, xG depends on factors that can directly influence chance of scoring goal. For example, typical factors are:
1. Distance from goal
2. ngle
3. Body positioning
4. Number of players between the ball and the goal post
5. Positioning of the keeper
6. Header or through foot
7. Open play or set piece
8. The pass leading up to the goal was through ball or a long ball

There could be numerous other factors, such as, pitch conditions (how wet or dry), weather conditions, schedule leading up to the game (busy schedule vs relaxed),player's age, player's history (hot streak vs poor form) or even factors such as loading a strike facing the menacing Yellow Wall at Dortmund! What it does NOT consider is "WHO" scored. Thus, xG is player independent. It is not Messi getting in a situation and scoring 9 out of 10 times, but a random set of players scoring 9 out of 10 times in that situation.

There are several mathematical frameworks to compute xG. Each model works based off of certain assumptions and weighs some factors more over others. Two such widely used models are provided by StatsBomb (https://statsbomb.com/) and Opta (https://www.optasports.com/sports/football/). Data presented in this article is thanks to a great deal of effort by https://fbref.com/en/ and the xG data is made available courtesy to StatsBomb. 

| ![screenshot](https://media-exp1.licdn.com/dms/image/C4E12AQEC6DVWo79hcQ/article-inline_image-shrink_1500_2232/0/1581971760403?e=2147483647&v=beta&t=nFTh1TqpENuUtPDks4zURbS8us_hkZIY-pPj5tp5gP0) |
|:--:|
| <b>Figure 1. Histogram of difference between goals scored and xG for seasons ending in 2018, 19 and 20 across Premier League, La Liga, Bundesliga, Ligue 1 and Serie A</b>|

So, let's get the obvious question out of the way - how good is the xG approach at estimating average goal output? The model considered in this study is quite good! Figure 1 shows histogram with a strong peak near 0.

<h3> Thought experiments </h3>

Let's run a couple of though experiments. For the figures below, let us consider an attacker or a striker is in a goal scoring position, facing the goal. The opposition is denoted by orange color with goalkeeper as rectangle and defenders in orange circles. For simplicity we will consider 4 scenarios.

* Open play goal scoring

| ![screenshot](https://media-exp1.licdn.com/dms/image/C4E12AQEB0WJINA3NUg/article-inline_image-shrink_1000_1488/0/1581971824959?e=2147483647&v=beta&t=mzOyR6CyQ9qZ4RU_pOr_wSSRGDIn0SPLvGJDekN9UAc) |
|:--:|
| <b>Figure 2. Open play goal scoring scenarios</b>|

In scenario 1, let's assume, Sergio Aguero has ball at his feet and a gaping goal in front. He has 4 options. Option 4 is the shortest distance path and 1, the longest. Option 3 is aimed straight at the goalkeeper. Assuming limited constraints, one could say, 4 has the highest xG, also referred to as a 'sitter' and 3 has the lowest probability, while 1 and 2 are spread in between. But, if the keeper changes the positions, the xG would look different. Now in scenario 2, shot number 2 has the lowest probability and probability of 4 going in is even more give the distance between keeper and the post.

* Goal scored on corner kicks

| ![screenshot](https://media-exp1.licdn.com/dms/image/C4E12AQG74hWYqWcbqw/article-inline_image-shrink_1500_2232/0/1581971897904?e=2147483647&v=beta&t=-G3qASI-o0iTHsitEoIDJTss1fUv5T4Aw-PdVYNJC4A) |
|:--:|
| <b>Figure 3. Corner kick goal scoring scenarios</b>|

Let us assume the exact same setup between scenario 3 and 4. The only difference is how the ball is delivered to the attacker. In scenario 3, the ball lands on the head of Sergio and in 4, the ball lands at the feet of Sergio. It is easier for Sergio to score from feet than through the head since he can control power and direction more easily. Plus, for balls at feet, the point of contact is much lower and available goal area for attack is much larger. The math works the opposite for ball hitting the head and hence players have to work harder to get the ball over the line. Hence, xG would be higher in Scenario 4 than in 3.

<h3>What do I make out of the numbers?</h3>

We laid out the formulation of xG. It is pretty clear that xG, in most forms, does not depend on the players scoring. So if I am Thomas Tuchel, what does it mean to have the likes of Neymar and Mbappe?

If an attacker has low average xG, it could mean the attacker gets in awkward and goal-scoring-unfriendly positions
If the throughput is well below the xG, it could mean the attacker lacks finishing. xG does not consider the shot power or the spin. If an attacker is underperforming then it could be a sign of lack of finishing.
In some cases, poor goals to xG ratio could be down to pure luck! Let us say, a player joins La Liga and has to face Ter Stegen, Oblak and Courtois in the first three games, chances that he scores are quite low.
If the player is consistently outperforming the xG then it could mean that, the player does not represent the mean level of the population - or - he is just too good to be where he is! (Knock knock Real Madrid!)
Shall we take a look at Europe?

| ![screenshot](https://media-exp1.licdn.com/dms/image/C4E12AQF_dHMkMc0MAQ/article-inline_image-shrink_1500_2232/0/1581971934431?e=2147483647&v=beta&t=hBHnrK8paBTbIZZQJtvHhbYUjz9kTnJqDEJbe8bRclM) |
|:--:|
| <b>Figure 4. Goals scored vs xG for season 2017-18</b>|

Season 2017-18 was the season Mo Salah announced his re-arrival in Premier League and created a huge splash in the footballing world. He exceeded all expectations and broke a lot of records along the way towards becoming the hottest property in the footballing world. And yet, Messi not only outperformed him, he also outperformed the xG stat.

| ![screenshot](https://media-exp1.licdn.com/dms/image/C4E12AQG3eBFheMSorg/article-inline_image-shrink_1500_2232/0/1581971971972?e=2147483647&v=beta&t=f9LxoCshX2Uet5YOabRxYZP4yKoEJjMVzMg92_KCgZY) |
|:--:|
| <b>Figure 5. Goals scored vs xG for season 2018-19</b>|

Messi, consistent, exceptional or the better description would be consistently exceptional! Asides the usual suspects, Atalanta started producing some of the finest football in Europe and were almost scoring for fun! Atalanta's Duvan Zapata performed well above the expectations. Despite the dire state of affairs at Arsenal, Aubameyang was the one constant that ticked for them. By his standards, Ronaldo was quiet at Juventus, settling from his summer move. At his old fortress, things were just not right; Real Madrid struggled for form half of the season. Despite a star studded bench of young attacking options, Karim Benzema produced a strong showing and vastly outperformed his xG to get Real Madrid to a third place finish. 

| ![screenshot](https://media-exp1.licdn.com/dms/image/C4E12AQFiB1rRBIwZBQ/article-inline_image-shrink_1500_2232/0/1581972007450?e=2147483647&v=beta&t=BmDbKbv9nTe_BPWCZFXUO524msYcYnI-7KhEA1HoaEs) |
|:--:|
| <b>Figure 6. Goals scored vs xG for season 2019-20</b>|

The season has crossed the three quarters of a mark and has produced some sensational performances. But, talk about Lazio and Ciro Immobile! At the time of writing this article, Lazio sit 2nd in Serie A table, 1 point behind the mighty old lady. Immobile has continued his fine form from 2019 season well into 2020 and he has a staggering tally of 25 goals already! Timo Werner has been in sublime form; he is one player for whom the transfer talk never dies down, you can expect a summer move given how consistently he has delivered. Lukaku comes as a big surprise! After a rather quiet spell in Manchester, he has set San Siro lit and announced as the new king of Milan!

<h3>Moments of genius or bad luck!</h3>

Overall, comparing xG and the goal tally, does tell us a lot about a player. But, be careful while using xG shot-by-shot! xG is useful at an aggregate level and not at shot by shot evaluation.

| [![screenshot](https://img.youtube.com/vi/hTyAitl5Za8/0.jpg)](https://youtu.be/hTyAitl5Za8?t=82)|
|:--:|
| <b>Salah scoring from tight angle</b>|

Salah produced a moment of magic against Salzburg not too long ago. They were up by 1 and he does this. For any mathematical model to calculate xG on this shot, it would be stacked against all odds - 1) angle, 2) distance, 3) body position, 4) keeper and defenders. And yet, he scored with a magnificent finish! Well, if you have him on speed-dial, ask him to do it again and we will see how many times he can repeat that ;)

| [![screenshot](https://img.youtube.com/vi/IsGi_6BHpb4/0.jpg)](https://youtu.be/IsGi_6BHpb4?t=460)|
|:--:|
| <b>Bale scoring overhead</b>|

I debated between using Ronaldo's overhead vs Bale's overhead. Two seasons ago, Champions League produced not one but two sensational overhead kicks. The reason I went with Bale's is because of the number of potential blocks in the way. Bale had to - 1) position his body relative to the post, 2) pick his spot and put just enough power, 3) beat defenders. Call it talent or luck, but it was one heck of a goal.

| [![screenshot](https://img.youtube.com/vi/nRQRyrg7Xxw/0.jpg)](https://youtu.be/nRQRyrg7Xxw?t=6)|
|:--:|
| <b>Stankovic scoring from distance</b>|

Inter Milan the treble winning reigning champions of Europe came into this game with big hopes. As if Imposing San Siro wasn't tough enough challenge for Schalke, this happened 22 seconds in the game. Stankovic is 40-45 yards from the goal. In this situation the xG would be very very low. The player has to - 1) connect well, 2) aim it in the right direction, 3) generate enough power, 4) not hit any players (well, Neur being Neur here!). Against all odds, he makes it, and it's a worldie! It takes absolute genius in such moments to win the battle against probability.


| [![screenshot](https://img.youtube.com/vi/sS3zDPEwU_U/0.jpg)](https://youtu.be/sS3zDPEwU_U?t=59)|
|:--:|
| <b>Casillas winning the world cup for Spain</b>|

Perhaps the most important moment of his life, perhaps the single most crucial second that won Spain the 2010 world cup, perhaps that split second decision where that left foot magic just did not work. Arguably two of the best sides in the world had locked horns to break the deadlock. At 60th minute a golden opportunity showed where an overhead ball found, through some celestial magic, none other than, Arjen Robben facing out-wide goal but one Iker Casillas. All mathematical calculations would term this as a high probability goal scenario - one on one, ball at the feet and at control, player is not off balance. 9 out of 10 times Robben would have scored that goal. But it wasn't to be. But it was pure brilliance on Casillas' part that weighed in on the 10% chance and probably won them the world cup!

| [![screenshot](https://img.youtube.com/vi/e2E-5PyYjT0/0.jpg)](https://youtu.be/e2E-5PyYjT0)|
|:--:|
| <b>Torres missing a sitter</b>|

Pick any model. Calculate xG any way you want. Every model, every person looking at this moment would have said - that's a goal, 100%. But .....
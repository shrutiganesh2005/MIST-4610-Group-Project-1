# MIST-4610-Group-Project-1

Team Name: 
21479 Group 8

Group Members 
1. Yared Awoke
2. Shruti Ganesh
3. Yunus Lallo
4. Ayad Momin

Problem Description: 
As the owner/operator of Elite United FC, your soccer club competes in professional leagues at both national and international levels. The club not only emphasizes on-field performance but also places importance on fan engagement. A passionate fan base attends matches, purchases merchandise, and interacts through various channels. Elite United FC is a multifaceted organization with departments such as player management, coaching staff, medical and fitness, finance, marketing, ticketing, facilities management, scouting, youth development, and fan engagement.

Key aspects of our business that the MIST 4610 class students should consider when designing the relational database include:
1. **Scouting**: Tracks scouting activities and records, including information about scouts, the players they evaluate, and the resulting reports.
2. **Trainer**: Manages data about athletic trainers, including their qualifications and the players they are responsible for.
3. **Injury Reports**: Documents reports on player injuries, detailing the type of injury, the affected player, and treatment plans.
4. **Injury**: Catalogues specific injuries sustained by players, tracking details like injury type and rehabilitation progress.
5. **Players**: Contains information on players, including personal details, performance data, positions played, and health records.
6. **Youth Development**: Oversees information about the youth development program, detailing young athletes' progress and talent evaluations.
7. **Coaching Staff**: Records information on coaching personnel, their qualifications, and the teams or players they oversee.
8. **Facility**: Details the sports center's facilities, including maintenance schedules, bookings, and usage history.
9. **Marketing**: Manages marketing campaign data, including sponsorship details, campaign results, and audience reach.
10. **Fan Engagement**: Tracks fan interaction and engagement, documenting fan profiles, preferences, and feedback.
11. **Ticketing**: Manages ticket sales for events, detailing types of tickets sold, customer information, and seating arrangements.
12. **Finance**: Records financial data, including budgets, expenditures, revenues, and financial reports.
13. **Merchandise**: Manages inventory and sales of team merchandise, including item details, sales figures, and supplier information.

**Explanation of the Data Model:**

Our data model represents a hypothetical soccer club. Our soccer club is comprised of several components from the various players and coaching staff to the finances of ticketing and merchandise. First, we have the players entity which has relationships with several other entities. There is a one-to-many relationship  between players and coaching staff (many players under one coaching staff), players and scouting (many scouts for one player), players and trainers (many players for one trainer), and players and injury reports (many injury reports for one player). To account for this, the coaching staff ID and player ID are placed in the scouting attributes as foreign keys. There is also a one-to-one relationship between players and youth development: each player is associated with one youth player.  

Within these entities, there are also relationships simultaneously between each other. Coaching staff and scouting have a one to one relationship, trainer and injury have a one to many relationship (one trainer takes care of many injuries), injury reports have a one-to-many relationships with both players and injury (one player can have many injury reports and one injury has many injury reports).

Outside the player table, there are also the  marketing and finance entities. Marketing has a one to many relationship with both fan engagement and merchandise (many fans are attribted to one marketing campaign and many marketing campaigns are attributed to one merchandise category. To account for this, the merchandise ID is placed in the marketing attributes as a foreign key. Finance also has a one to many relationship with merchandise (there can be many items of merchandise under one financial transaction). Finance additionally has relationships with facility and ticketing, both being one to many as well. One facility can have several financial transactions while one financial transaction can have several tickets. 

**Data Model: **

<img width="884" alt="Screenshot 2024-04-02 at 5 38 41 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/db50490d-3501-4647-b81d-1852103e7048">

**Data Dictionary: **

<img width="814" alt="Screenshot 2024-04-02 at 5 42 42 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/63d4749f-30e1-40ad-85f2-e7fe6d29d228">
<img width="822" alt="Screenshot 2024-04-02 at 5 43 17 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/96f91e35-bf4e-46ae-8155-3dc6178f1917">
<img width="647" alt="Screenshot 2024-04-03 at 10 47 03 AM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/31d4b3f3-9d4c-429f-943c-f9c4eb07bebf">
<img width="841" alt="Screenshot 2024-04-02 at 5 43 31 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/bac1e4fe-a0d6-4d5f-88ae-bd9a3e7b07f1">
<img width="800" alt="Screenshot 2024-04-02 at 5 44 41 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/7b420a07-979b-4458-8cb2-ddcfe582a65b">
<img width="812" alt="Screenshot 2024-04-02 at 5 44 57 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/ad4f2dd5-a29c-4335-b567-883749ae0baa">
<img width="842" alt="Screenshot 2024-04-02 at 5 45 54 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/68e891e5-d64b-4f5a-bae7-31c0ea84fd30">
<img width="820" alt="Screenshot 2024-04-02 at 5 46 06 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/3c217f87-1912-4445-90b8-42a1c6b83455">
<img width="603" alt="Screenshot 2024-04-02 at 5 46 49 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/072cc3a1-91ce-4db4-a993-09f0f26ad430">
<img width="837" alt="Screenshot 2024-04-02 at 5 46 30 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/aed55510-85dd-44bc-92b4-a9e441c36c31">
<img width="671" alt="Screenshot 2024-04-03 at 10 47 43 AM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/185f8bed-016f-4ce0-9ea9-09be227a133a">
<img width="676" alt="Screenshot 2024-04-02 at 5 47 18 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/21687d51-2ef1-41cb-b694-ca4f31809979">
<img width="584" alt="Screenshot 2024-04-02 at 5 48 41 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/cc2fabb0-a620-4ab7-af12-ce0e11ad98bb">

**Queries:** 

<img width="643" alt="Screenshot 2024-04-04 at 3 41 08 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/7f28cb05-5247-477a-9c97-5325651b5fff">


Query 1  list the facilities with a capacity over 23,000 and maintenance schedule before 10 AM.<img width="754" alt="Screenshot 2024-04-03 at 10 51 29 AM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/e606de2c-9878-4eb6-b832-dc37630fb381">

This query recognizes which facilities have a capacity over a specific value and maintenance schedule before a specific time. This is important for the club to know in order to schedule specific games/events based on how many people the location can hold and whether or not the maintenance will interfere with the event. 

Query 2 list the average age of players at each Development Stage. <img width="1038" alt="Screenshot 2024-04-03 at 10 52 05 AM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/8f6dded0-6a46-4fc7-84b1-d932766ce3c7">

This query focuses on youth development and the average age based on development progress (competitive, fundamentals, development, advanced training, professional prep). This is important for the club to know in order to gauge maturity and ability for each group of players. This is also important for documentation purposes and keeping track of age and demographics for each group of youths. 

Query 3 list the average number of players training with each trainer, grouped by the scheduled training times. <img width="1069" alt="Screenshot 2024-04-03 at 10 52 41 AM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/c9bc05a5-113d-409b-acd1-fd5d66d648e7">

The query shows the average number of players training with each player and organizes them on what time their trainer is scheduled for. This is important for the club to recognize in order to schedule new incoming players to a specific trainer based on who has a fewer number of average players training or to schedule players who can only be trained at a specific time. 

Query 4 Write a query to list the percentage of players that were out 2 or more months with injury
<img width="1075" alt="Screenshot 2024-04-04 at 3 31 34 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/2115b239-95db-470b-b05f-34c5be065a8b">

This query lists how many players were out for 2 or more months with injury. This allows the club to keep track of how many players out of the total number are not able to play. This information is vital to be aware of because there is a possibility of other entities including finance and youth development to be impacted from the lack of players.

Query 5 Write a query that shows the number of German Defenders on the team
![Screenshot 2024-04-04 152611](https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/163186348/35d5aa71-421a-43dc-8df6-4e2cb6dd0625)

This query lists out the number of players on the club who are of German nationality and play the Defender position. This allows us to maintain an easy transfer record of international players. It also gives insight on the scouting possibilities based on league and postion. 

Query 6 List out the financial amounts for Q1 (the first three months of the year) by the  financial type and match date
![Screenshot 2024-04-03 191435](https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/163186348/0f502f19-84bd-442c-b45a-0f2e49294ad2)

This query is important specifically for the finance portion of the soccer club keeping track of finances and fees based on match date. In order to successfully keep track of financial reports, this query allows the club to organize finances based on amount, date, description, and facility. Keeping track of finances is vital to ensure financial stability for the club as well as budgeting and planning for the future.

Query 7 List the players Nationality in descending (Z-A) order who get trained by Alden Arkow.
![Screenshot (38)](https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/165838944/9b7bd999-fd4e-4f8e-89e5-617e984c4fcb)

This query lists players nationality in a specific order for organization purposes based on who gets trained by a specific trainer, Aldow Arkow. This organization is important for a soccer club to ensure adaptability and cultural understanding. Additionally, organizing the nationality of players based on a single trainer allows the club to make informed decisions regarding player recruitment. 

Query 8 List the number of fans that each marketing campaign brought in, grouped by their membership status, and only include membership statuses where the number of fans is greater than 5.
![Screenshot 2024-04-04 002846](https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/163186348/fd61e5d1-813d-45e9-ae3c-d59817af0a28)

This query lists how many fans each marketing campaign helped to bring in and organized them based on membership status with fans greater than a specific number. This is extremely important for the club, specifically the marketing team, to recognize which campaigns were the most successful in bringing in a larger fanbase. This information can be utilized for future campaigns in which will be the most successful for the club. 

Query 9 Write a query that lists out the names of coaches and scouts in ascending (A-Z) order based only on who are not associated with any players.

<img width="800" alt="Screenshot 2024-04-04 at 3 16 47 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/114629015/36fe242a-4bfd-448b-a896-c209aeabf951">

This query lists out names of the coaches and scouting coaches in a specific order based on who work with no players. This is important for the club in various ways, specifically for planning purposes. If there are any incoming players, they can be assigned to a specific coach not currently assigned to any players. This also lets the team know which scouting coaches have yet to do their job of finding and recruiting new talent.

Query 10 Calculate the sales revenue and its percentage share of the club's total financial turnover for merchandise items where the vendor is either Nike or Puma.
<img width="956" alt="Screenshot 2024-04-04 at 3 39 31 PM" src="https://github.com/shrutiganesh2005/MIST-4610-Group-Project-1/assets/131741591/6cdcfa4e-2e0a-4afe-880c-b35291668cc8">


This query calculates the total sales revenue for merchandise items, grouping them by the inventory categories: Nike and Puma. This is important in helping the marketing team plan promotions and the finance team prioritize profits based on inventory. If sales for Nike and Puma items are specifically strong,the company focus will be on these two categories. 

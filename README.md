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

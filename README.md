# Helpline scheduler
Code written in Python 3 finds the best possible schedule for volunteers while incorporating constrains and special requirements using **[CP-SAT Solver](https://developers.google.com/optimization/cp/cp_solver)**.

### The problem
Arranging volunteers for a helpline service. There are two types of work done on the same day:
- Phone shift: every day of month.
- Chat shift: Mondays and Wednesdays.

### Constraints:
- Each volunteer gives a list of days they are available.
- Each volunteer has to have 4 days between their shifts.
- One volunteer only does chat because of hearing problems.
- Most volunteers only do phone because they are not qualified for chat.
- Some volunteers do both chat and phone.

### Priorities:
1. Have minimum one volunteer for each day.
2. Fill chat shifts.
3. Have a second volunteer even on phone days.

### Possible special requirements by volunteers:
 - Maximum amount of days for weekend shifts.
 - Wants their shifts to be on separate weeks.
 - Does both chat and phone but prefers chat.
 - Welcomes observer volunteer to work on the same day.
 - Wants to work alone.
 - Cannot work alone.
 - Wants shifts on different weeks.
 - Does not want to work with some other people.

### Objective:
 Maximize filled shifts.

## Sample output:

>2019 April   -   Distance: 2

>Volunteer 1: 13. phone
Volunteer 1: 30. phone
Volunteer 2: 6. phone
Volunteer 2: 12. phone
Volunteer 2: 23. phone
Volunteer 2: 28. phone
Volunteer 3: 22. phone
Volunteer 3: 29. phone
Volunteer 4: 19. phone
Volunteer 4: 27. phone
Volunteer 5: 25. phone
Volunteer 6: 8. phone
Volunteer 6: 15. phone
Volunteer 7: 18. phone
Volunteer 7: 26. phone
Volunteer 8: 3. chat
Volunteer 8: 14. phone
Volunteer 9: 1. phone
Volunteer 9: 10. phone
Volunteer 9: 21. phone
Volunteer 10: 5. phone
Volunteer 10: 16. phone
Volunteer 11: 3. phone
Volunteer 11: 8. chat
Volunteer 12: 4. phone
Volunteer 12: 11. phone
Volunteer 13: 7. phone
Volunteer 13: 15. chat
Volunteer 13: 20. phone
Volunteer 14: 10. chat
Volunteer 14: 22. chat
Volunteer 14: 29. chat
Volunteer 15: 9. phone
Volunteer 15: 17. phone
Volunteer 16: 2. phone
Volunteer 16: 24. phone
Volunteer 17: 6. observer
Volunteer 17: 14. observer
Volunteer 17: 19. observer
Volunteer 17: 26. observer

Remaining capacities: None

Day|  P  C  O
___|___________
 1.|  9  _
 2.| 16    
 3.| 11  8
 4.| 12    
 5.| 10    
 6.|  2    17
 7.| 13    
 8.|  6 11
 9.| 15    
10.|  9 14
11.| 12    
12.|  2    
13.|  1    
14.|  8    17
15.|  6 13
16.| 10    
17.| 15  _
18.|  7    
19.|  4    17
20.| 13    
21.|  9    
22.|  3 14
23.|  2    
24.| 16  _
25.|  5    
26.|  7    17
27.|  4    
28.|  2    
29.|  3 14
30.|  1    

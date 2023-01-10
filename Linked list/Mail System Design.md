Input: N = 10, Q = 7query = {1, 2, 1, 5, 1, 7, 1, 9, 2, 5, 2, 7, 4, 5}Output: UNREAD - 1 3 4 6 8 10READ - 2 9 5TRASH - 7


Initial:
UNREAD section: 1 2 3 4 5 6 7 8 9 10
READ section : EMPTY
TRASH section : Empty
Query 1 : 1 2
UNREAD section: 1 3 4 5 6 7 8 9 10
READ section : 2
TRASH section : Empty
Query 2 : 1 5
UNREAD section: 1 3 4 6 7 8 9 10
READ section : 2 5
TRASH section : Empty
Query 3 : 1 7
UNREAD section: 1 3 4 6 8 9 10
READ section : 2 5 7
TRASH section : Empty
Query 4 : 1 9
UNREAD section: 1 3 4 6 8 10
READ section : 2 5 7 9
TRASH section : Empty
Query 5 : 2 5
UNREAD section: 1 3 4 6 8 10
READ section : 2 7 9
TRASH section : 5
Query 6 : 2 7
UNREAD section: 1 3 4 6 8 10
READ section : 2 9
TRASH section : 5 7
Query 7 : 4 5
UNREAD section: 1 3 4 6 8 10
READ section : 2 9 5
TRASH section : 7

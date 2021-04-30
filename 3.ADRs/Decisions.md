# Decisions #
1. Users will be maintained as is in the original DB. This is to avoid password migration as the passwords are stored as oneway hash.
2. Ticket creation and Ticket assignment is the first problem to be solved.
3. Knowledge base alone will be migrated to AWS Storage serive to start with.
4. Consutants need to travel to customer site and fix the problem. So, Geo service becomes important.
5. Business is local/global is not mentioned. So, it is assumed to be global / will grow global.
6. DB may be moved to the cloud following lift and shift.
7. Initially daily report will be generated to reconcile number of filed tickets, no of assigned tickets
8. Observability of the system is important - alerting mechanism is going to be added.
9. ELK vs Graphana 



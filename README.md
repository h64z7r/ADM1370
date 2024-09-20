java c
ADM1370 Applications of Information Technology for Business
Assignment 3 – Microsoft Access
Database: a collection of data, or information, that is specially organized for rapid search and retrieval by a computer. Databases are structured to facilitate the storage, retrieval, modification, and deletion of data in conjunction with various data-processing operations. A database management system (DBMS) extracts information from the database in response to queries. 
ASSIGNMENT OBJECTIVES 
The objective of this assignment   is to get   you   familiarized   with   the   basics   of   designing   a   database   in   a   simple RDBMS application such as   MS Access. As   an   introductory   assignment,   each   requirement   is   elaborated through   a series of guided steps.   In addition to   advancing your   knowledge   of   relational   databases,   a   complementary objective   is to foster your analytical thinking and   logical   reasoning skills.
SUBMISSION   INSTRUCTIONS 
1.         This assignment   is due   by   11:59   PM on Saturday, April   6,   2024.
2.         This assignment   is to   be completed   individually and   must   adhere   to the   University’s   policy   on   Academic   Integrity.
3.         The assignment submission   must   be:
• One   (1) electronic   .ZIP file,
•             Contain   only   files   pertinent to   this   assignment,   and
•             Have   files   that   follow   the   naming   and   file   format   conventions   specified   below.
•             Make   sure   to   download   and   open   your   submission   from   Brightspace   after   you   have   submitted   to
ensure the files are as expected. Any   files that   cannot   be   opened   (e.g.   the   file   extension   was   removed   or altered) will   receive a   grade   of   zero.
4.         The following files and file   naming are   required   (including   underscores):
•             ADM1370_W24_A03_StudentID.zip   (contains   your   submission files)
•             ADM1370_W24_A03_StudentID_Academic   (PDF or   MS Word   file)
•             ADM1370_W24_A03_StudentID_Database   (Access file)
•             ADM1370_W24_A03_StudentID_Report   (both   PDF and   MS Word   files)
5.          Include your signed   Declaration of Academic   Integrity   (see   next   page).
6.          Failure to   properly   name your files, submit   in the correct   file   formats,   or   omitting   your   Academic   Integrity   statement will   result   in deductions,   up to and   including   receiving a   mark   of   zero on   the   assignment.
ASSIGNMENT SCENARIO 
Icarus   Flights   (IF)   is attempting to   modernize their   information systems to   better   manage their operations. As part of their   modernization   project, they   have tasked you with developing a   prototype   database   application   that they will then   provide to   developers and/or suppliers when   obtaining   an   enterprise-grade   system. 
IF   maintains a fleet of different aircraft   that   fly   passengers   across   its   regional   routes.   Each   aircraft   has   various seat configurations,   referred to   as seat   maps, that   include different types   and   numbers   of   seats;   for   example, larger jet airplanes will   have   Premium   Class,   Business Class, and   Economy   Class seats while   turboprop   airplanes   normally only   have   Economy   Class seats.
When a   passenger wishes to travel with the airline,   they   will   book   a   seat   on   a   particular   flight   and   will   be   issued   a ticket. The ticket will state which flight   it   is for,   which   seat   on   the   airplane   they   will   sit   in,   and   how   much   they      paid for the ticket. As the airline   prioritizes   passenger experience, they   avoid   double-booking   seats   on   a   flight, ensuring only one   passenger   is ever assigned to   a   particular   seat for   a   flight.
When   being given   requirements for the   prototype, a conceptual   model was   provided, along   with the   required   tables and fields on the   following   pages.
To   prepare the   database for   IF, you will   need to   perform   the following   actions:
create    populate tables,
link tables together through   lookups and   relationships,
create queries to   display   results,
create forms for data   entry,
create   reports for tables and   queries,
create a   navigation   menu for the database.
Each of these are described throughout the   rest of the   document.
PART 1 - CREATING TABLES 
Start Microsoft Access and create a Blank Database.
Step 1.1 - Create the AIRPLANE Table 
1. Create a new table using the Design View (Create => Table Design) command.
2. In the Field Name column, enter all the attributes as shown in the AIRPLANE table definition. Make sure the Data Type pertaining to each field is of the correct type.
3. Use the “Description (Optional)” column in the Design View to describe the type of information that goes in each of those fields (e.g. for the plane_Model field, state that the field captures the plane’s manufacturer’s model number)
4. Make sure that the plane_Tail field is designated as the primary key for this table. To set a field as your primary key, you can right click the field name and select Primary Key. Indicate this is the primary key field in the field description.
5. Save this table by clicking on the save icon on the top-left corner. You will be prompted for a name. Name the table “AIRPLANE”.
Now that you have at least one database object created, you save your database file using the notation specified under SUBMISSION INSTRUCTIONS. Make sure to save your database file regularly so that you do not lose any work. Whenever you are finished working on your file, make sure that it has been saved and stored somewhere that you can open or download from at a later time.
Step 1.2 - Create the SEAT, PASSENGER, and FLIGHT Tables 
1. For the SEAT, PASSENGER, and FLIGHT tables, repeat the steps from Step 1.1, referring to the appropriate table definitions and assigning the correct primary keys.
Step 1.3 - Populate AIRPLANE, SEAT, PASSENGER, and FLIGHT Tables
1.      Populate the AIRPLANE, SEAT, PASSENGER, and FLIGHT tables   before   proceeding to the   next step.   Sample   data   has   been   provided   in a separate spreadsheet   published on   Brightspace for the AIRPLANE, SEAT,   and FLIGHT tables.   For the PASSENGER table, create   10   passenger   records with   made-up   information for testing, with one of them having your name and university email.   Note that   you   will   need to   populate   airplanes   before you can   populate seats. 
Step 1.4 - Create the TICKET Table 
1.          You will   now   need to   create the TICKET table   by   repeating the   prior steps while   referring to   the   TICKET   table definition and the following   instructions.   Name your table as   TICKET 代 写ADM1370 Applications of Information Technology for Business Assignment 3 – Microsoft AccessStatistics
代做程序编程语言  when   saving.
2.          Make sure the ticket_No field   is set   to   the AutoNumber and   designate   this   field   as   the   primary   key.
3.         The seat_ID, pax_ID, and flight_No fields   in this table   require special   attention   as these   will   be   the   foreign   keys   used to form   relationships   between the tables. You will   need to   use the Lookup Wizard to   configure         these foreign   key fields as outlined   below:
3.1.    In the   Design View of the TICKET table,   create   a field   named seat_ID.   For   the   Data   Type,   select Lookup Wizard from the drop-down options.
3.2.    In the   Lookup Wizard   popup, select “   I want   the   lookup field   to   get   the   values   from   another   table   or   query” and   click Next.
3.3.    Choose the SEAT table from the   list   of tables   and   click Next.
3.4.    Select the seat_ID, seat_No, seat_Type, and plane_Tail fields   as your   Selected   Fields   and   click   Next.
3.5.    Uncheck the Hide Key Column checkbox   and   resize the   lookup   columns   so   the field   headers   are   visible. Click Next.
3.6.    Select seat_ID as the field value for   storage   in the TICKET table   and   click Next.   3.7.    Confirm the   name of the   new field   is “seat ID” and   click Finish.
Following the   prior sequence of steps should   produce   a   new   field   in the TICKET table   such   that   every   time   a   new   record   is   being added, a drop-down   menu appears   with   information   being fetched   from   the   SEAT
table. Once a seat on   a   plane   is   selected,   its   seat_ID will   appear   as   the   field   value.
3.8.    Repeat the steps above to   create   the pax_ID and flight_No fields   in   the TICKET table.   These   fields
should   be   based on   lookups from the TICKETS table.   For   pax_ID:   display   pax_ID,   pax_Full_Name, and
pax_Tier   in the   dropdown   but only store   pax_ID.   For flight_No:   display   all fields   in the   FLIGHT table   but   only store   flight_No.
4.         After creating all your fields, you can   change the   order   in   which   the   fields   appear   in   the   table.   You   can   do   so   by opening the table   in   Design View and dragging   the   fields   up   or   down.   Re-arrange   the   table   fields
according to the order they appear   in the TICKET table definition.
By   using the   Lookup Wizard   in the TICKET table, we   have already started   to   create   relationships   among   the PASSENGER, FLIGHT, and SEAT tables.   Next, we will verify   and   refine these   relationships.
Step 1.5 - Populate the TICKET Table 
1. Add   10   different different to your   newly   created TICKET   table,   making   up   the   dates.   Create   multiple   tickets   where you are the   passenger.
PART   2:    DEFINING TABLE   RELATIONSHIPS 
The   next step   is to connect the   tables:
1.          Open the Relationships view   (Database Tools =>   Relationships)
2.          If you followed the steps   in the   previous   part, the tables   should   have   lines   connecting   them   to   represent   their   relationships.   Rearrange the   boxes so that the diagram   resembles the   conceptual   model   provided         earlier   in this document.   If   not all   relationships were formed when   creating   the tables,   use   the “Edit
Relationships command   under the “Relationships   Design” tab to create them.
3.          Notice that the   relationship   lines   between the tables do   not   indicate the cardinality   (e.g.   one-to-many,
many-to-one, etc.) of the   relationships yet. To fix this,   in the “   Edit   Relationships” dialog   box,   check   the   box   next to “Enforce Referential Integrity” .
4.          Save the   relationships   by clicking on the save   icon   in the   toolbar.
PART   3:    FORMULATING   QUERIES 
Step 3.1 – Platinum Status Query 
Create a query that can   be   used to list all passengers with platinum status and   their   information.
1.          Create a   new   query   using the Design View (Create => Query Design).
2.          Select the PASSENGER table, then select all fields within   the   table   except   for   First   Name   and   Last   Name.
3.          Under the pax_Tier field, specify the criteria to   only   show   records   where   the   field   is   equal   to “Platinum”
4.          Save this query as “   1_Platinum_Query”
5.          Run the   query to   ensure   data   is   being correctly   pulled and   presented.   If   no   data   appears,   review   the   previous steps, and ensure you   have at   least   one   passenger   with   platinum   status.
Step 3.2 – Booked Seats Query 
Create a query that can   be   used to   search for   booked   seats   on   a   specific   flight.
1.          Create a   new   query   using the Design View (Create => Query Design).
2.          Select the FLIGHT, TICKET, and SEAT tables, then select the   following   fields:
•            FLIGHT.flight_NO
•            FLIGHT.flight_Depature
•            FLIGHT.flight_Arrival
•            FLIGHT.flight_Origin
•            FLIGHT.flight_Destination
•            Seat.seat_No
•            Seat.seat_Type
3.          Under the flight_No field, specify a   parameter   based   criteria   with   the   statement “Enter   Flight   #”
4.            Save   this   query   as “2_Booked_Seats”
5.          Run the   query   and   provide a flight   number for one   of the   flights   in   the FLIGHT table.   Ensure   that   data   appears and that the correct fields   are visible.
Step 3.3 – Flight Statistics Query 
Create a query that   lists all   passenger   bookings   by   plane   model   and seat   type,   represented   by   the   number   of   tickets   booked and average cost   per ticket.
1.          Create a   new   query   using the Design View (Create →Query Design) and select   all   three tables.
2.         The query should   project the following the   fields:
•          AIRPLANE.plane_Model
•            SEAT.seat_Type
•          TICKET.ticket_NO
•          TICKET.ticket_Price
3.          Enable the “Totals” function   under the “Query   Design” tab to allow   for   calculign   the   number   of tickets
booked and the average cost   per ticket. This will   reveal   a   new “Total:”   row   in   the   query   designer.   Select   the correct transformation for each column, and   apply   an alias   to   show   the   result   as “Tickets   Booked”   and   “Average   Cost   of   Ticket”   . 
4.            Save   this   query   as “3_Flight_Statistics”
5.          Run the   query to   ensure   data   is   being correctly   pulled and   presented.   If   no   data   appears,   review   the   previous steps, and ensure you   have at   least   one   ticket   in   the   database.







         
加QQ：99515681  WX：codinghelp

# FCC-timestamp-microservices
It's a solution to the challenge of the FCC Backend Development and API Timestamp Microservices Project.

It has 3 main specification; 

1. Give "api/2015-12-25" -> get unix and utc time; 
2. Give "api/1479663089000" -> get  unix and utc time; 
3. Give "api/1479663blablabla" -> get error: "Invalid Date" with json response.  

You need to set the date correctly according to its type UNIX or traditional date. That's the whole point!  

Please pay attention to the conditional variable assignment part on line 29.

In addition, checking the validity of the date variable is a bit tricky.  If the parameter is invalid Date format (date instanceof Date) returns FALSE but isNaN(date.getTime()) returns TRUE. Therefore, it is necessary to add an exclamation point at the beginning of this expression on line 31.  

Less is more! Have a nice day!

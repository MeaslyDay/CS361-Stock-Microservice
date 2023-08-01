# CS361-Stock-Microservice
--------------------------------
# Request stock information
Make a request using local host and port = 65432. The request will contain the stock symbols of companies and the time period for the values and pertinent information of those stocks. To make a request pass an array with two strings, the first is the string of stock symbols and the second is the time period over which the stock information is displayed. The time period has a default value of "1mo" meaning one month, if you pass an array with only one string then the service will set the time period to one month.
# A call would look like this: 
socket.send_pyobj([stocks, period]) where send_pyobj sends an object, in this case an array, to the socket at port 65432, and where stocks is this string("aaPl MSFT [insert any symbol regardless of capitalization), and where period is this string("3mo") meaning three months. The "[number]mo" part of period can be replaced with "[number]d" for days and "[number]wk" for weeks.

# Recieving stock information
Receive information about the stocks using local host and port = 65432. The information will be a pandas object(simular to a csv file) which is displayed as a table with columns being stock values and quantity, and rows being the days that data was taken. The data received is the close and open value of the stock along with the days the data was taken.

![UML diagram](https://github.com/MeaslyDay/CS361-Stock-Microservice/UML.png?raw=true)

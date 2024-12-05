In my previous job, I worked on a web application for retailers that allowed employees to call customers through the website, track customer statistics, and manage employee working hours.

My main responsibility was building an Middleware server that acted as a bridge between the Kazoo server and other services in the system. It fetched call details and statistics from Kazoo and returned them to our services for better tracking and reporting.

Additionally, I worked on the employee statistics interface using ReactJS. My task was to fix logic errors in the interface, such as ensuring the correct calculation of employee working hours based on data from Kazoo.


1. Can you explain the architecture of the intermediary server you built?
-> The intermediary server I built was designed to fetch data from the Kazoo server and send it to other services in our system. I built it using Java with Spring Boot, and we stored some data in MySQL for easy access. To improve performance, I also used Redis for caching frequently accessed data.


2. Can you give an example of a specific logic error you fixed in the employee statistics interface?
-> One specific issue I worked on was fixing the calculation of employee working hours. The problem occurred because the hours were not being correctly calculated based on the data from the Kazoo server. It was important that the system considered the start and end times of the calls, and in some cases, the hours were being doubled or missed.

I debugged the issue by reviewing the data coming from Kazoo and comparing it with how it was being processed in the front-end logic. After identifying the mistake, I fixed the calculations and tested it to ensure the working hours were accurate. This helped improve the accuracy of employee reports and allowed managers to track working hours more effectively.


3. What challenges did you face when integrating the Kazoo server with your application?
	-> One of the main challenges I faced was that our server was an intermediary, and there were many different services in the system that needed to interact with it. To ensure smooth integration, I had to communicate with the teams working on these other services to understand their workflows and how they would use the data coming from the Kazoo server.
	This required a lot of coordination and discussions to make sure the data was processed and delivered in the right format. I also had to address any issues that came up during these interactions

	-> I worked part-time at my previous company for about a year
#Spring Sendgrid Example 

1. Edit parameters in MailController.java
..* From - sendgrid email that you are registered with 
..* Subject - The email's subject line
.. *Content - The email's content, Replace "Hello Email!" with whatever you want
.. *sg - Your unique sendgrid API key

2. In the top level of your project directory run ./gradlew build
3. Once it finishes building run ./gradlew bootRun and then wait for the application to start
	- Make sure that you see /send get mapped ( Mapped "{[/send]}" onto public void send.MailController.send(java.lang.String) throws java.io.IOException)
4. Test the application
	- The /send endpoint takes in a required parameter which is toEmail so pass whatever email it is that you want to send to
	ex. http://localhost:8080/send?toEmail=email@email.com
5. Verify that you have received an email

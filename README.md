# Python-1
python mailer
#smtplib is the module used by python to send emails through SMTP.
#The ssl module is used to access the Operating System Socket.
port = 465
#This port will be required later.

We now need to get the sender’s email together with his or her password. Store them in variables that will be used in making an SMTP request.
the code will be as follows 
import ssl, smtplib
port = 465
email = input("Enter your email: ")
password = input("Enter your password: ")


Next we need to get some required fields to send an email. An email is composed of the receiver’s address, a subject line and the body. We will input all this.

recipient = input("Enter the email address to send the email to: ")
subject = input("What is the subject of the email: ")
text = input("Type your email here: ")
message = "Subject: {}\n\n{}".format(subject, text)

context = ssl.create_default_context()

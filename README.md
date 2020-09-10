# Inoitsu-analyzer

Cortex analyzer that search Inoitsu for a compromised email address. (without the need of API key!)

If the email is compromised then it returns:
- Compromised: true
- Total breaches
- Most recent breach
- Breached data 
- Critical data
- Exposure rating: The comparative data exposure and risk rating assigned to this email address.

Inoitsu analyzer can helps when investigating suspicious mails received either from known/unknown sender. (Helps you ensure that the sender's email address is not compromised)

## Setting up the analyzer

~~~
git clone https://github.com/jonathan6661/Inoitsu-analyzer.git
cd cd Inoitsu-analyzer/Inoitsu
pip3 install -r requirements
~~~
After installing the requirements you need to add Inoitsu folder to /Cortex-Analyzers/analyzers/ folder.
~~~
cp -R Path_where_you_dowloaded_Inoitsu/Inoitsu-analyzer/Inoitsu Path_to_Cortex-Analyzers/Cortex-Analyzers/analyzers/
~~~

## Setting up Inoitsu analyzer on Cortex

Log into cortex with an account with the proper privilege level then navigate to >Organization>Analyzers and click on Refresh analyzers button.

![refresh](https://user-images.githubusercontent.com/37407314/92717066-8e1a1600-f357-11ea-8942-75ec2b97dedf.PNG)

Now as the analyzer has been added successfully to Cortex, you need to enable it.

![enable analyzer](https://user-images.githubusercontent.com/37407314/92718622-f4079d00-f359-11ea-8124-0ee9ca565661.PNG)

### Testing Inoitsu analyzer (Cortex)

Navigate to Analyzers then run Inoitsu analyzer.

![run analyzer](https://user-images.githubusercontent.com/37407314/92719258-ce2ec800-f35a-11ea-9f82-f4ed9f4ab01e.PNG)

Let's test Inoitsu analyzer with a compromized email.

![report](https://user-images.githubusercontent.com/37407314/92719758-8d837e80-f35b-11ea-8120-014a389955cd.PNG)

Let's test Inoitsu analyzer with an uncompromised email.

![uncompromised](https://user-images.githubusercontent.com/37407314/92720556-a9d3eb00-f35c-11ea-8157-911d85149ae4.PNG)

## Setting up Inoitsu analyzer templates on TheHive
  
Log into TheHIVE with an account with the proper privilege level then navigate to >USER>Report templates and make ctrl+f + Inoitsu

![report template](https://user-images.githubusercontent.com/37407314/92721417-fc61d700-f35d-11ea-9505-f2994ef7aee8.PNG)

As shown, no template exists for Inoitsu Analyzer.

### Adding templates to TheHive

Add both short and long templates to Inoitsu analyzer

![short](https://user-images.githubusercontent.com/37407314/92721964-cbce6d00-f35e-11ea-978b-6a602617e7e5.PNG)

![long](https://user-images.githubusercontent.com/37407314/92722405-7b0b4400-f35f-11ea-9176-c09d9c8ea02e.PNG)

### Testing Inoitsu analyzer (TheHive)

In the observables section add emails to test.

Then select the emails that you want to analyze, select Inoitsu and click on Run selected analyzers.

![thehive iocs](https://user-images.githubusercontent.com/37407314/92724230-2d440b00-f362-11ea-8115-21c91bf27d2d.PNG)

![response](https://user-images.githubusercontent.com/37407314/92725358-f2db6d80-f363-11ea-8e59-697e579a75aa.PNG)

To view the report of the compromised email, click on Inoitsu:Compromised="True"

![analyzer report](https://user-images.githubusercontent.com/37407314/92727316-d3920f80-f366-11ea-9e29-d2c21d286277.PNG)

To view the report of the compromised email, click on Inoitsu:Compromised="False"

![analyzer report 2](https://user-images.githubusercontent.com/37407314/92727203-a5accb00-f366-11ea-875a-da30f01b6c4d.PNG)




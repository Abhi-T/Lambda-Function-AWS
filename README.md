# Lambda-Function-AWS
Lambda-Function-AWS

this is a Basic example of how we can use AWS Lambda functionality to create our APIs.

Steps-

1> Create a new function in AWS Lambda as choose the runtime evnironmen as Python 3.8 (as per your code).

2>Now from your local machine, create the deployment package. Here the deployment package is nothing but your code with all the required libraries.
In this example, i have created a python file with name Basic-Example-1.py and inside this file there is a basic function to test a URL using request library. This is a very basic function which will hit a weather API and returns https 200 if the URL returns something.

3>In our Example, we have used only one python library "requests" so only this lib we need to install/include in our package

4> Navigate to your code folder and open command prompt.

5> Now use Pip functionality to install requests library to your code folder
pip install requests -t .

6>Above Command will install the lib in your code folder. Now you have to zip the complete package.

7>This zip folder will include your python code and all the libraries (in our case only 1 lib we used)

8> Upload this zip to the AWS lambda. All you code files will open in lambda interpreter just like pycharm or Visual studio.

9>Last step is to reconfigure your AWS lambda handler to invoke your api. That means configure the exact path of the functino which needs to be invoked.
In our case, it is Basic-Example-1/test1

10> Save the changes and hit test. You should see success logs.

11> Now if you want to expose this function as an http or REST API, you have to create a trigger.

12> From lambda designer view, select new trigger or create trigger option.

13> Select API gateway from the option and select http. Security as Open/None.

14>Once you save the changes, you should see an http url in lambda console which can be used to trigger your function.



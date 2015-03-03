# SendGrid

##Sendgrid Email as a Service

Sendgrid is the world's largest email infrastructure as a service provider focused on deliverability, scalability, and reliability. 

**If you are going to use PHP**

To try the sample Sendgrid application, change directory to ```bluemix-sendgrid-php-sample``` and then deploy to Bluemix by executing the following commands:

```
cf login
cf create-service sendgrid free mySendgrid
cf push
```

After the commands complete successfully, look for the console output specifying the application URL. It should look something like: 

```
usage: 128M x 1 instances
urls: sendgrid-random-word.mybluemix.net
```

Next execute the following commands from your console, to specify custom to/from email addresses using Bluemix environment variables. 

```
cf set-env sendgrid TO_EMAIL bluemix@mailinator.com
cf set-env sendgrid FROM_EMAIL foo@bar.com
cf restage sendgrid
```

Open your favorite browser using the URL ending with mybluemix.net (such as sendgrid-random-word.mybluemix.net in the example above) from the console output to access the application. 

**To install pre-requisites for a local deployment**

Via [Composer](https://getcomposer.org/)

``` bash
$ composer install
```

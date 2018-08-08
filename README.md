# Django_Project_Shibli
I am going to create a chat bot and then deploy it to the web. This project is all about installing and finalizing it.
Installing:
python --version


Install virtualenv and virtualenvwrapper
virtualenv and virtualenvwrapper provide a dedicated environment for each Django project you create. While not mandatory, this is considered a best practice and will save you time in the future when you’re ready to deploy your project. Simply type:

pip install virtualenvwrapper-win
Then create a virtual environment for your project:

mkvirtualenv myproject
The virtual environment will be activated automatically and you’ll see “(myproject)” next to the command prompt to designate that. If you start a new command prompt, you’ll need to activate the environment again using:

workon myproject

Install Django
Django can be installed easily using pip within your virtual environment.

In the command prompt, ensure your virtual environment is active, and execute the following command:

pip install django
This will download and install the latest Django release.

After the installation has completed, you can verify your Django installation by executing django-admin --version in the command prompt.

See Get your database running for information on database installation with Django.

Common pitfalls¶
If django-admin only displays the help text no matter what arguments it is given, there is probably a problem with the file association in Windows. Check if there is more than one environment variable set for running Python scripts in PATH. This usually occurs when there is more than one Python version installed.

If you are connecting to the internet behind a proxy, there might be problem in running the command pip install django. Set the environment variables for proxy configuration in the command prompt as follows:

set http_proxy=http://username:password@proxyserver:proxyport
set https_proxy=https://username:password@proxyserver:proxyport

*****doc****
https://docs.djangoproject.com/en/2.0/intro/tutorial01/

**************

Creating an admin user¶
First we’ll need to create a user who can login to the admin site. Run the following command:

$ python manage.py createsuperuser
Enter your desired username and press enter.

Username: admin
You will then be prompted for your desired email address:

Email address: admin@example.com
The final step is to enter your password. You will be asked to enter your password twice, the second time as a confirmation of the first.

Password: **********
Password (again): *********
Superuser created successfully.
Start the development server¶
The Django admin site is activated by default. Let’s start the development server and explore it.

If the server is not running start it like so:

$ python manage.py runserver
Now, open a Web browser and go to “/admin/” on your local domain – e.g., http://127.0.0.1:8000/admin/. You should see the admin’s login screen:

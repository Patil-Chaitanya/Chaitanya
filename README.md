Chaitanya RASA BOT
Rasa Deployment
Deploying Rasa Bot over Google Cloud Platform using Docker.

Prerequisites:
RASA
Anaconda Prompt
Visual Studio Code
Instructions:
For installing Depencies on Windows:
RASA Installation
If python is installed in your system, then pip comes in handy. So simple steps are:

Install virtualenv using
pip install virtualenv

Now in which ever directory you are, this line below will create a virtualenv there
virtualenv myenv

And here also you can name it anything instead of myenv.

Now if you are same directory then type,
myenv\Scripts\activate

Upgrade pip (Please use this command in administrator mode)
pip install --upgrade pip

Install RASA
pip install rasa==2.5.0

NOTE : Please check Python version should be 3.7 or greater and pip should be installed previously

If the rasa installation gives error, try this solution

MySQL Installation
We first need to install MySQL Workbench community edition for windows

We can download MySQL Workbench from here

MySQL Workbench requires Microsoft Visual C++ Redistributable packages. If its not previously installed, install it using following link

NOTE : Please select root as username and 12345 as password while installing MySQL Workbench.

RASA MySQL dependencies installation
To download MySQL Python run the following command :

pip install mysql-connector-python

Install PyMySQL

pip install PyMySQL

Install Pandas

pip install pandas

Install SQLAlchemy

pip install SQLAlchemy

Installation Complete
Get files
To download the RASA files from github run the following command

git clone https://github.com/athenasaurav/Chaitanya.git

Move inside directory

cd Chaitanya

Create Intial Database
Run the following command in an Anaconda prompt

python create_database.py

Note : Please run this file only once.

Open a new Anaconda Prompt

rasa train

RUN Chatbot
Open one Ananconda prompt and move into Chaitanya folder

rasa run -m models --enable-api --cors “*” --debug

Open another Ananconda prompt and move into Chaitanya folder

rasa run actions

Chat with Bot
Click on index.html in the folder to open in browser and start chatting

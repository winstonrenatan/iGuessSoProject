# iGuessSoProject
The iGuessSo program aims to predict what object user are thinking of base on the attributes that is answered. On this software, one could add their own object and determine what attributes an object has. Attribute also can be added later on to enhance clearity or specify an object. If user are not satisfied with current object or attributes, user can easily delete the unwanted object or attribute. The goal is to have the exact object as what the user think of, so the software may ask all the attributes in the database. However, this software also can guess an object eventhough the given attributes are not detailed/exactly the same as long as it is included in their attributes description. Besides adding the object and attributes one by one, user can also have an excel file and have it imported to the databse of this software. Thus with all the features this software has, it is still far away from being a great predictor like the one we might have seen before the genie Akinator which uses Limule program published by Elokence.com. <br>

## Authors
- Ferinzhy Halik 01082170035
- Liang Cai	01082170044
- Matius Ebenhaezer	01082170012
- Noach Nathanael Tjahjadi 01082170008
- Sebastian Aldi 01082170015
- Winston Renatan	01082170030<br>
Informatics Universtias Pelita Harapan

## REQUIREMENT
- Python
- Openpyxl<br>
If you have Python, you maybe have run the software given or didn’t know if you gave installed the openpyxl before. In case there is an error as shown on Figure 1 when you run the software, that means you need to install the openpyxl. The installation process is quite simple: open the command prompt then type in “pip install openpyxl” without quotes as shown on Figure 2 and wait for the installation to finish. To make sure that things go right, we can check in by type in “python” then “import openpyxl” if the command prompt shows somewhat like Figure 3, then it is ready.<br>
![ErrorImport](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/openpyxl%20error.PNG) <br>
Figure 1: error on importing openpyxl <br>
![InstallOpenPyXl](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/install%20openpyxl.PNG) <br>
Figure 2: install openpyxl <br>
![ReCheck](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/check%20openpyxl.PNG) <br>
Figure 3: recheck the success of installation <br>

## INSTALLATION/RUNNING INSTRUCTION
-	Default installation and running:
1.	Download and extract the file “iGuessSo Software.zip”.
2.	Place the files on the folder where you install openpyxl.
3.	Open the file “main.py” on your favorite IDE (Integrated Development Environment) then compile and run it, I personally use Visual Studio Code. For Visual Studio Code see Figure 4, all we need to do is right click anywhere on the window and click on “Run Python File in Terminal”.<br>
![CompileAndRun](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/compile%20and%20run.png)<br>
Figure 4: compile and run the software<br>
4.	After the program successfully run, it will automatically build up file as on Figure 5. Don’t worry nothing bad will happen as it will be explain later on.<br>
![DATFile](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/creating%20dat%20file.PNG)<br>
Figure 5: DAT file type appeared<br>

-	Installation and running using provided data:
1.	Download and extract the file “iGuessSo Software.zip”.
2.	Place the files on the folder where you install openpyxl.
3.	Open the file “awa2_reader.py” on your favorite IDE then compile and run it. It wont output a thing, but it will form a DAT file type as mentioned above.
4.	Compile and run the “main.py” file. Here you can directly play the game by pressing unlike the default one.

## EXPLANATION
The zip file itself contain three files: main.py, awa2_reader.py, and awa2.xlsx. These items have their own function which will be described as the following. awa2.xlsx contains name of objects in this term animals with each of their attributes attach to them. The function of awa2_reader.py is to connect the excel format file to the python file (main.py). This awa2_reader.py functions to import the data in the excel files to the entity.dat and attribute.dat. So that the data can be played on the iGuessSo software.<br>
After adding the object or attribute data, all the information will be stored in the DAT file mentioned before. DAT file is a generic data file created by a specific application. It may contain data in binary or text format (text-based DAT files can be viewed in a text editor). DAT files are typically accessed only by the application that created them.  So, according to the definition provided from FileInfo, it is correct that it is created and accessed by the application that made it, in our case its main.py or the iGuessSo.<br>
Upon adding the attributes, it will be put on an array which is attribute_list with its initialization as an empty array. So, the attribute_list = [attribute1, attribute2, attribute3, …]. While there is also another array which is entity_list = [entity1, entity2, entity3, …]. These entity consist of name of an object and an array which holds what attributes the object have. For example entity1 will consist of objectA, [attribute1, attribute3, …].<br>
Those array will then be file out put (piped) to be save as a file which in our case is the DAT file mentioned before. With the python pickle module is used for serializing and de-serializing a python object structure. Any object in python can be pickled so that it can be saved on disk.  So that it can be used to load the DAT file and accessed in the iGuessSo software.<br>
There are some features that can be accessed by the user: Guess (or play), Add an object, Add an attribute, Delete Object(s), Delete Attribute(s), Quit as what is shown on Figure 6. This game can expand as long as the user keep adding new object and attribute which is not limited for one cateogry (fruit, car, animals, etc.). But through the adding object and attribute feature, user can add up any category or categories they want to the game. As mentioned before, if you have chosen to install and run using the provided data, you can directly Guess or play the game. If there is no object nor attribute data, the software will prevent user to start guessing as presented on Figure 7 then if the user forgot to add the attribute another error message will be displayed on Figure 8. There are two options to start, either add object continued with attribute or other way around.<br>
![MainMenu](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/main%20menu%20display.PNG)<br>
Figure 6: main menu display<br>
![ErrorObject](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/error%20no%20object.PNG)<br>
Figure 7: error message on guess without object data<br>
![ErrorAttribute](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/error%20no%20attribute.PNG)<br>
Figure 8: error message on guess without attribute data<br>

### Adding Object Followed with Attribute
First, we need to add the objects we want to create using the “Add an object” button then type in the name of the object as shown on Figure 9 then continue by clicking the “Add Object” button. Next, what we need to do is by adding the attribute on “Add an attribute” button on the main menu. We then need to fill up the name of the attribute then choose what objects have that attribute we create as on Figure 10 by ticking the checkboxes.<br>
![ObjWOAtt](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/add%20obj%20without%20att.PNG)<br>
Figure 9: add object without attribute<br>
![AttChoosObj](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/add%20att%20with%20obj.PNG)<br>
Figure 10: add attribute and choose the object(s)

### Adding Attribute Followed with Object
First, we need to add the attribute we want to create using the “Add an attribute” button then type in the name of the attribute as shown on Figure 11 then continue by clicking the “Add Attribute” button. Next, what we need to do is by adding the objects to be guessed on “Add an object” button on the main menu. We then need to fill up the name of the object then choose what attributes that it fulfill on the checkboxes given as show on Figure 12.<br>
![AttWOObj](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/add%20attribute%20without%20obj.PNG)<br>
Figure 11: add attribute without object given<br>
![ObjChooseAtt](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/add%20obj%20with%20attribute.PNG)<br>
Figure 12: add object and select its attributes<br>

After trying to add few objects and attributes, maybe we would like to change or delete the data from the list. It is made possible with the “Delete Object(s)” and “Delete Attribute(s)” features at the main menu. These features can be used to delete multiple things from the list in one deletion by ticking the checkboxes. This features is shown on Figure 13 for deleting objects and Figure 14 for deleting the attributes on the list. As a reminder both file is non-volatile which means that it is not erased or emptied when the software is closed or quit. This means if the user keep filling the object and attribute it can expand to bigger scope.<br>
![DelObj](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/delete%20obj.PNG)<br>
Figure 13: delete object(s)<br>
![DelAtt](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/delete%20att.PNG)<br>
Figure 14: delete attribute(s)<br>

## SAMPLE INPUT/OUTPUT
So, in this case there are several objects which are: Bajaj (traditional Indonesian transportation), Apple, Pumpkin, and Grape. Below is the object and its attribute along. Here, we will try to have the specific answer for an object and one is having the prediction (the one that may be right) according to the user input.<br>

|Object     |Attribute(s)              |
|-----------|--------------------------|
|Bajaj      |car, red, big             |
|Apple      |fruit, red, small         |
|Pumpkin    |fruit, orange, small      |
|Grape      |fruit, purple, small      |

1.	First, we will try to have the answer as Grape. Having NO as the answer of every questions except for: “Is the object fruit?”, “Is the object purple?”, and “Is the object small?”. This would produce the result Grape as it has the specific attributes as we choose. The display would look like the Figure 15. <br>
![ResultTestOne](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/case2b.PNG)<br>
Figure 15: result on test one<br>
2.	Second, we will try to have no answer for this part. We will just answer YES for “Is the object fruit?” and answer NO for the rest of the question. This will result the software to find “fruit” attribute on every object which results as Figure 16. As the user input is not the exact similar to the attributes hold by an object it is said to be resembles.<br>
![ResultTestTwo](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/case3b.PNG)<br>
Figure 16: result on test two<br>

## EXTRAS
As what have been mentioned above, it is really possible to expand this software as big as possible. To ensure that everything goes well, we can see the case that are provided here. The situation is where a user have done adding all the objects they want and assign the attributes to each object, but there is an object that is missed. It is quite simple in handling this type of problem. User can choose the “Add an object” menu and directly tick the attributes for the object, shown on Figure 17. Which work the other way around with attributes that is shown on Figure 18.<br>
There are also error handling to prevent double object or double attribute as shown on Figure 19 and Figure 20. This handling is quite useful especially when the data gets to big and hard to detect.<br>
![AddMissedObj](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/case1a.PNG)<br>
Figure 17: adding missed object and select its attributes<br>
![AddMissedAtt](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/case1b.PNG)<br>
Figure 18: adding missed attribute and assign it to objects<br>
![HandlingDoubleObj](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/case%20double%20obj.PNG)<br>
Figure 19: error handling on double object<br>
![HandlingDoubleAtt](https://github.com/winstonrenatan/iGuessSoProject/blob/master/PicturesOfSoftware/case%20double%20att.PNG)<br>
Figure 20: error handling on double attribute<br>

## LESSON LEARNED
Through this project we learn a lot of new things and expand ourselves a lot more. We can learn to manage our time especially when we need to meet in discussing this project. There is also the need of adaptation in our team, because not every single person have the same schedule and task to do. A lot more, we study to manage our projects beside this one, because there are also another project that we should maintain and finish. We also try to communicate efficiently so that one could understand the meaning of it easily. This project also enhance our learning technically in python and develop our understanding more in new things that we learn. Our experience in teamwork also increase so that in real life we can engage with other people in the team we are placed in. We also need to trust in other people, especially in our coding that is quite long. We cannot do it by ourselves, thus we need to give some function/method to be done by other people and we trust in them that it will be done in a good way and have the good result. As what is stated, we also need to correct and give advice for one another as the function/method we think is good may have flaw in others perspective and vice-versa. We think that this project is really useful in developing ourselves more.

## References and Acknowledgements
- Akinator. Elokence.com Developers. 2007. Retrieved from https://en.akinator.com/content/6/everything-you-ve-always-wanted-to-know-about-akinator on 15 April 2019.
- “How to Download and Install Python 3.6 on Windows 10”. ProgrammingKnowledge. 21 November 2015. Retrieved from https://youtu.be/dX2-V2BocqQ on 15 April 2019.
- “.DAT File Extension”. FileInfo Contributor. 22 September 2017. Retrieved from https://fileinfo.com/extension/dat on 15 April 2019.
- “Understanding Python Pickling with example”. Abdulniyaspm (Geeks for Geeks Contributor). Retrieved from https://www.geeksforgeeks.org/understanding-python-pickling-example/ on 16 April 2019.


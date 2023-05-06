Download Link: https://assignmentchef.com/product/solved-eecs-1015-lab-5-lists-dictionaries-and-tuples
<br>



<ol start="2">

 <li><strong>LAB 5 – TASK/INSTRUCTIONS</strong></li>

 <li><strong>Lab 5 – Manipulate data involving user names and cities</strong></li>

</ol>

<strong>STARTING CODE LINKS</strong>

This lab starts with skeleton code that you can find here: <a href="https://trinket.io/python/f24922d729">https://trinket.io/python/f24922d729</a>  Or on the self-grading platform here: <a href="https://www.eecs.yorku.ca/~stateclock/python/lab5/">https://www.eecs.yorku.ca/~stateclock/python/lab5/</a>

The starting code defines global variables bound to tuples and a dictionary as follows:

names = (“Masha”, “Kevin”, “Ruigang”, “Vlad”, “Ramesh”, 

“Aditi”, “Caroline”, “Panos”, “Chuck”, “Grani”,           “Rutha”, “Stan”, “Qiong”, “Alexi”, “Carlos”) cities = (“Toronto”, “Ottawa”, “Hamilton”) testDict = {“Richard”:”Toronto”, “Jia-Tao”:”Toronto”, “Justin”:”Ottawa”, “Lars”:”Ottawa”}

You need to define and implement the following functions:

getRandomItem(parameter: a list or tuple) -&gt; returns an item from the list or tuple

This function will randomly select an item from the list or tuple passed as an argument.

For example, if you call getRandomItem(names), then it would return one of the items from the tuple names.

createNameDictionary(parameters: none) -&gt; returns a dictionary

This function will create a new dictionary.

This function uses the global variables: names and cities (shown above)

This function returns a dictionary where each name in the names tuple is a key in the dictionary.

The key’s value is randomly selected from he cities tuple using the getRandomItem() function.

Essentially the function creates a dictionary of names, where each name is randomly assigned to a city.

Your function will return this dictionary.

fromCity(parameters: dictionary, string) -&gt; returns a list

This function takes a dictionary and a string with a city name.

The function will return a <strong><em>list</em></strong> of all the names in the dictionary who are from that specified city.

For example: fromCity(testDict, “Toronto”) would return a list [‘Richard’, ‘Jia-Tao’] removePeopleFrom(parameters: dictionary, string) -&gt; no return, but modifies dictionary

This function takes a dictionary and a string. The string is a city name.

This function will <strong><em>delete</em></strong> all items in the dictionary whose value is equal to the string.

For example: removePeopleFrom(testDict, “Toronto) would modify the testDict to be {“Justin”:”Ottawa”, “Lars”:”Ottawa”}

printNameDict(parameters: dictionary, tuple of strings) -&gt; nothing

This function takes a dictionary and a tuple of strings. The tuple items are the city names.

This function will loop through the tuple of cities and print out the name of the people who live in that city.

The peoples names will be numbered.  For example: printNameDict(testDict, (“Toronto”, “Ottawa”)) prints: People from Toronto:

<ol>

 <li>Richard</li>

 <li>Jia-Tao</li>

</ol>

People from Ottawa:

<ol>

 <li>Justin</li>

 <li>Lars</li>

</ol>

<strong>                                                            </strong><strong>continue on next page </strong>

If the dictionary does not have a person from a city, it should print *None*

For example, printNameDict(testDict, (“Toronto”, “Ottawa”, “Hamilton”)) prints: People from Toronto:

<ol>

 <li>Richard</li>

 <li>Jia-Tao</li>

</ol>

People from Ottawa:

<ol>

 <li>Justin</li>

 <li>Lars</li>

</ol>

People from Hamilton      *None*

main(parameters: none) -&gt; no return

Your main function will be used to test the functionality above.

Main will have two parts.  Part 1 will be used to test the functions one by one (except createNameDictionary), using the testDict variable.

Part 2 will apply the function to a larger dictionary created by your function createNameDictionary().  Ideally, if you can get part 1 to work properly, part 2 will work as long as your createNamedDictionary() function is correct.

<strong>Main part 1 works as follows: </strong>

<ul>

 <li>Test the getRandomItem() function with argument global variable: cities</li>

 <li>Test the fromCity() function with arguments testDict and “Toronto”, then testDict and “Ottawa”</li>

 <li>Test printNameDict() function with arguments testDict and tuple (“Toronto”, “Ottawa”)</li>

 <li>Test removePeopleFrom() function with arguments testDict and “Ottawa”    To verify, call printNameDict() again</li>

</ul>




<strong>Main part 2 works as follows: </strong>

<ul>

 <li>create a new dictionary using the createNameDictionary() function</li>

 <li>call printNameDict with this new dictionary and the cities tuple (3) For each city (Toronto, Ottawa, and Hamilton)      call the fromCity() function and print the returned lists</li>

</ul>

(4) Use the removePeopleFrom() function to remove all the people from Hamilton and Toronto from the dictionary (5) call printNameDict to show the people have been removed

EXAMPLE OUTPUT OF LAB 5

Part 1 – Testing functions with `testDict’

Testing getRandomItem() function (‘Toronto’, ‘Ottawa’, ‘Hamilton’) item = Toronto Testing fromCity() function

[‘Richard’, ‘Jia-Tao’]

[‘Justin’, ‘Lars’]

Testing printNameDict() function

People from Toronto:

<ol>

 <li>Richard</li>

 <li>Jia-Tao People from Ottawa:</li>

 <li>Justin</li>

 <li>Lars</li>

</ol>

Testing removePeopleFrom() function

People from Toronto:

<ol>

 <li>Richard</li>

 <li>Jia-Tao People from Ottawa: *None*</li>

</ol>

<strong>Part 1</strong>

<ul>

 <li>Test the getRandomItem() function with argument global variable: cities</li>

 <li>Test the fromCity() function with arguments testDict and “Toronto”, then testDict and “Ottawa”</li>

 <li>Test printNameDict() function with arguments testDict and tuple (“Toronto”, “Ottawa”)</li>

 <li>Test removePeopleFrom() function with arguments testDict and “Ottawa”</li>

</ul>

– To verify, call printNameDict() again

<ol>

 <li>Panos 2. Grani</li>

 <li>Alexi People from Ottawa:</li>

 <li>Masha</li>

 <li>Kevin 3. Vlad</li>

 <li>Aditi</li>

 <li>Caroline</li>

 <li>Stan People from Hamilton:</li>

 <li>Ruigang</li>

 <li>Ramesh</li>

 <li>Chuck 4. Rutha</li>

 <li>Qiong</li>

 <li>Carlos Toronto List:</li>

</ol>

[‘Panos’, ‘Grani’, ‘Alexi’] Hamilton List:

Ottawa List:

*None* People from Ottawa:

<ol>

 <li>Masha</li>

 <li>Kevin</li>

 <li>Stan People from Hamilton: *None*</li>

</ol>








